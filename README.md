# Declaración de la Renta - España (IRPF 2025)

> **Ejercicio fiscal 2025** · Campaña: 2 de abril – 30 de junio de 2026

Skill para Claude / Cowork que asiste al contribuyente español en la revisión y optimización de su declaración del Impuesto sobre la Renta de las Personas Físicas (IRPF), ejercicio 2025.

---

## DESCARGO DE RESPONSABILIDAD

**ESTE SOFTWARE SE PROPORCIONA "TAL CUAL", SIN GARANTÍA DE NINGÚN TIPO.**

Este skill es una herramienta de orientación fiscal de carácter informativo. **NO constituye asesoramiento fiscal, contable ni jurídico profesional.** No sustituye en ningún caso la consulta con un asesor fiscal colegiado, gestor administrativo o abogado tributarista.

**El usuario es el único responsable** de las decisiones fiscales que tome basándose en la información proporcionada por este skill. Ni el autor ni los colaboradores asumen responsabilidad alguna por errores, omisiones, pérdidas económicas, sanciones administrativas o cualquier otro perjuicio derivado directa o indirectamente del uso de esta herramienta.

La normativa fiscal española es compleja y cambia con frecuencia. Las deducciones están sujetas a condiciones, límites de renta, incompatibilidades y requisitos documentales que pueden variar y que este skill no siempre puede verificar completamente.

**Uso recomendado:** Este skill está pensado como herramienta complementaria. Un caso de uso ideal es verificar que una declaración ya preparada por un gestor profesional incluye todas las deducciones posibles. Puede servir como "checklist" para no dejarse nada, pero la decisión final y la responsabilidad de la declaración siempre recaen en el contribuyente y, en su caso, en su asesor.

**En caso de duda, consulta siempre con un profesional cualificado.**

---

## Qué es este skill

Es un conjunto de archivos de referencia fiscal y un flujo de trabajo guiado que permite a Claude:

1. Recibir y analizar el borrador de la AEAT (PDF o datos manuales)
2. Confirmar datos personales, familiares y de residencia
3. Formular preguntas dirigidas para descubrir posibles deducciones no incluidas
4. Cruzar la información con la normativa estatal y autonómica vigente
5. Presentar un informe con deducciones adicionales identificadas y ahorro estimado

---

## Estructura del proyecto

```
declaracion-renta-espana/
|
|-- SKILL.md                          # Skill principal (flujo de trabajo)
|-- README.md                         # Este archivo
|-- LICENSE                           # Licencia GPLv3
|-- .gitignore                        # Archivos excluidos de git
|
|-- references/
|   |-- nacional.md                   # Normativa IRPF estatal 2025 completa
|   |-- casos-especiales.md           # Ley Beckham, cripto, no residentes, etc.
|   |
|   |-- regiones/
|       |-- indice-regiones.md        # Tabla resumen de todas las CCAA
|       |-- preguntas-descubrimiento.md  # Cuestionario por categorías
|       |-- andalucia.md
|       |-- aragon.md
|       |-- asturias.md
|       |-- baleares.md
|       |-- canarias.md
|       |-- cantabria.md
|       |-- castilla-la-mancha.md
|       |-- castilla-y-leon.md
|       |-- cataluna.md
|       |-- extremadura.md
|       |-- galicia.md
|       |-- madrid.md
|       |-- murcia.md
|       |-- la-rioja.md
|       |-- comunidad-valenciana.md
|       |-- ceuta.md
|       |-- melilla.md
```

---

## Cómo instalar el skill

### Opción 1: Copiar la carpeta manualmente

1. Descarga o clona este repositorio
2. Copia la carpeta completa `declaracion-renta-espana/` dentro de tu directorio de skills de Claude:
   - En Cowork: dentro de la carpeta `.claude/skills/` de tu proyecto
   - En Claude Code: dentro de `.claude/skills/` en la raíz de tu proyecto

### Opción 2: Clonar directamente en el directorio de skills

```bash
cd tu-proyecto/.claude/skills/
git clone https://github.com/joseconti/declaracion-renta-espana-2025.git declaracion-renta-espana
```

---

## Cómo usar el skill

Una vez instalado, el skill se activa automáticamente cuando mencionas temas relacionados con la declaración de la renta en España. Por ejemplo:

- "Quiero revisar mi declaración de la renta"
- "He subido mi borrador de la AEAT, puedes revisarlo?"
- "¿Qué deducciones puedo aplicar en Madrid?"
- "Mi gestor ha preparado mi declaración, puedes comprobar si falta alguna deducción?"
- "Tengo criptomonedas, cómo las declaro?"
- "Me he mudado a España, puedo acogerme a la Ley Beckham?"

### Flujo típico de uso

1. **Sube tu borrador** (PDF de Renta WEB) o facilita tus datos manualmente
2. **Confirma tu comunidad autónoma** de residencia y situación personal
3. **Responde a las preguntas** que Claude te irá formulando por temáticas
4. **Recibe un informe** con:
   - Deducciones que ya aplicas correctamente
   - Deducciones adicionales identificadas con ahorro estimado
   - Recomendación sobre tributación individual vs conjunta
   - Puntos que requieren verificación profesional

---

## Cobertura geográfica

### Comunidades autónomas de régimen común (todas cubiertas)

Andalucía, Aragón, Principado de Asturias, Illes Balears, Canarias, Cantabria, Castilla-La Mancha, Castilla y León, Cataluña, Extremadura, Galicia, Comunidad de Madrid, Región de Murcia, La Rioja, Comunitat Valenciana.

### Ciudades autónomas (cubiertas)

Ceuta y Melilla (régimen especial con deducción del 60%).

### Régimen foral (NO cubierto)

Navarra y País Vasco (Alava, Bizkaia, Gipuzkoa) tienen haciendas forales propias con un IRPF diferente al estatal. Sus contribuyentes NO presentan la declaración ante la AEAT sino ante sus respectivas Haciendas Forales. Este skill NO cubre dichos territorios.

---

## Casos especiales cubiertos

- Régimen de impatriados (Ley Beckham / art. 93 LIRPF)
- Tributación de criptomonedas (trading, staking, lending, airdrops, mining)
- Modelo 721 (cripto en el extranjero > 50.000 EUR)
- Modelo 720 (bienes en el extranjero > 50.000 EUR)
- No residentes con rentas en España
- Exit tax (impuesto de salida)
- Exención por trabajos en el extranjero (art. 7.p)
- Ganancias patrimoniales complejas (inmuebles, coeficientes de abatimiento)
- Nómadas digitales (Ley de Startups)
- Régimen de atribución de rentas

---

## Fuentes oficiales utilizadas

Toda la información fiscal contenida en este skill procede exclusivamente de fuentes oficiales:

### Agencia Estatal de Administración Tributaria (AEAT)

- [Manual Práctico de Renta 2025 - Parte 1](https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html)
- [Manual Práctico de Renta 2025 - Parte 2: Deducciones Autonómicas](https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100/deducciones-autonomicas.html)
- [Guía de Deducciones Autonómicas del IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html)
- [Deducciones generales y autonómicas aplicables en 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/introduccion/deducciones-generales-autonomicas-aplicables.html)
- [Gravamen estatal IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-general/gravamen-estatal.html)
- [Gravamen ahorro estatal IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-ahorro/gravamen-estatal.html)
- [Mínimo personal y familiar 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c14-adecuacion-impuesto-circunstancias-personales/cuadro-resumen-minimo-personal-familiar.html)
- [Régimen especial impatriados (Ley Beckham)](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/manual-tributacion-no-residentes/regimenes-opcionales/regimen-especial-impatriados.html)
- [Monedas virtuales - Tributación IRPF](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2024/c11-ganancias-perdidas-patrimoniales/monedas-virtuales/compra-venta-monedas-virtuales-tributacion-inversor.html)
- [Campaña de Renta 2025](https://sede.agenciatributaria.gob.es/Sede/Renta.html)
- [IRPF Deducciones autonómicas](https://sede.agenciatributaria.gob.es/Sede/vivienda-otros-inmuebles/irpf-deducciones-autonomicas.html)
- [Deducción rentas Ceuta/Melilla](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/deduccion-rentas-obtenidas-ceuta-melilla.html)

### Boletín Oficial del Estado (BOE)

- [Orden HAC/277/2026 - Modelos declaración Renta 2025](https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041)
- [Ley 28/2022 - Ley de Startups (nómadas digitales)](https://www.boe.es/buscar/act.php?id=BOE-A-2022-21739)
- [Orden HAC/242/2025 - Modelos declaración Renta 2024](https://www.boe.es/buscar/act.php?id=BOE-A-2025-5049)

### Portales tributarios autonómicos consultados

- Junta de Andalucía - Tributos
- Portal Tributario de Castilla-La Mancha
- Junta de Castilla y León - Tributos

---

## Limitaciones conocidas

- **No cubre régimen foral** (Navarra, País Vasco). Estos territorios tienen normativa fiscal propia.
- **Cuantías parciales en algunas CCAA.** Cuando no ha sido posible obtener la cuantía exacta de una deducción de la fuente oficial, se indica "Consultar normativa autonómica vigente". Se recomienda contrastar con la fuente enlazada.
- **No calcula el impuesto.** Este skill identifica deducciones y orienta, pero no genera la autoliquidación.
- **No accede a los sistemas de la AEAT.** No puede consultar datos fiscales reales del contribuyente; trabaja con la información que el usuario le facilita.
- **Ejercicio 2025 únicamente.** La normativa de ejercicios anteriores puede diferir.
- **Canarias requiere revisión manual.** Muchas deducciones canarias no aparecen automáticamente en el borrador de la AEAT.

---

## Contribuir

Las contribuciones son bienvenidas, especialmente:

- Correcciones de datos fiscales con referencia a la fuente oficial
- Actualizaciones cuando cambie la normativa
- Ampliación de cuantías en deducciones autonómicas marcadas como "Consultar"
- Inclusión de territorios forales (Navarra, País Vasco)
- Traducciones (catalán, euskera, gallego, valenciano)

Para contribuir, abre un issue o pull request. Toda aportación debe incluir la fuente oficial que respalde el dato.

---

## Licencia

Este proyecto está licenciado bajo la **GNU General Public License v3.0 (GPLv3)**.

Consulta el archivo [LICENSE](LICENSE) para los términos completos.

En resumen: puedes usar, modificar y distribuir este software libremente, siempre que cualquier obra derivada se distribuya también bajo GPLv3 y se mantenga el aviso de copyright y el descargo de responsabilidad.

---

## Autor

José Conti - [plugins.joseconti.com](https://plugins.joseconti.com)

---

## Aviso legal final

Este software se distribuye con la esperanza de que sea útil, pero **SIN NINGUNA GARANTÍA**; ni siquiera la garantía implícita de COMERCIABILIDAD o IDONEIDAD PARA UN PROPÓSITO PARTICULAR. Consulta la GNU General Public License v3.0 para más detalles.

La información fiscal contenida puede no estar actualizada o ser inexacta. **Consulta siempre con un profesional antes de tomar decisiones fiscales.** El uso de este skill no crea ninguna relación de asesoramiento profesional entre el autor y el usuario.
