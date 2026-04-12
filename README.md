# Declaracion de la Renta - Espana (IRPF 2025)

Skill para Claude / Cowork que asiste al contribuyente espanol en la revision y optimizacion de su declaracion del Impuesto sobre la Renta de las Personas Fisicas (IRPF), ejercicio 2025.

**Ejercicio fiscal:** 2025 (del 1 de enero al 31 de diciembre de 2025)
**Campana de presentacion:** del 2 de abril al 30 de junio de 2026
**Domiciliacion bancaria del pago:** hasta el 25 de junio de 2026

---

## DESCARGO DE RESPONSABILIDAD

**ESTE SOFTWARE SE PROPORCIONA "TAL CUAL", SIN GARANTIA DE NINGUN TIPO.**

Este skill es una herramienta de orientacion fiscal de caracter informativo. **NO constituye asesoramiento fiscal, contable ni juridico profesional.** No sustituye en ningun caso la consulta con un asesor fiscal colegiado, gestor administrativo o abogado tributarista.

**El usuario es el unico responsable** de las decisiones fiscales que tome basandose en la informacion proporcionada por este skill. Ni el autor ni los colaboradores asumen responsabilidad alguna por errores, omisiones, perdidas economicas, sanciones administrativas o cualquier otro perjuicio derivado directa o indirectamente del uso de esta herramienta.

La normativa fiscal espanola es compleja y cambia con frecuencia. Las deducciones estan sujetas a condiciones, limites de renta, incompatibilidades y requisitos documentales que pueden variar y que este skill no siempre puede verificar completamente.

**Uso recomendado:** Este skill esta pensado como herramienta complementaria. Un caso de uso ideal es verificar que una declaracion ya preparada por un gestor profesional incluye todas las deducciones posibles. Puede servir como "checklist" para no dejarse nada, pero la decision final y la responsabilidad de la declaracion siempre recaen en el contribuyente y, en su caso, en su asesor.

**En caso de duda, consulta siempre con un profesional cualificado.**

---

## Que contiene este skill y por que es tan extenso

El IRPF espanol es uno de los impuestos mas complejos de Europa. No es un impuesto unico: es un sistema de escalas, minimos, reducciones, deducciones estatales y deducciones autonomicas que interactuan entre si, con condiciones y limites diferentes segun la situacion personal, familiar, geografica y economica de cada contribuyente.

Para dar una idea del volumen de informacion que maneja este skill:

**Normativa estatal (references/nacional.md):** contiene las escalas de gravamen general (6 tramos del 9,50% al 24,50%) y del ahorro (5 tramos del 9,50% al 15,00%), los minimos personales y familiares (contribuyente, descendientes, ascendientes, discapacidad), las formulas de reduccion por rendimientos del trabajo (con 3 tramos y formulas como 7.302 - [1,75 x (RNT - 14.852)]), los gastos deducibles, las rentas exentas, las reducciones de base imponible, 11 categorias de deducciones estatales con sus porcentajes y bases maximas, las reglas de tributacion conjunta vs individual, y los plazos y formas de presentacion.

**Deducciones autonomicas (references/regiones/):** cada comunidad autonoma tiene competencia para establecer sus propias deducciones de la cuota. Este skill incluye un archivo por cada una de las 15 CCAA de regimen comun mas Ceuta y Melilla, con un total de mas de 350 deducciones autonomicas documentadas. La Comunitat Valenciana tiene 41 deducciones propias, Canarias 29, Region de Murcia 28, Asturias 27, Castilla-La Mancha 27, La Rioja 26, Galicia 25, Illes Balears 24 y asi sucesivamente. Cada deduccion tiene sus propios porcentajes, limites, requisitos de renta, condiciones de edad, situacion familiar, incompatibilidades con otras deducciones, y en muchos casos requisitos documentales especificos.

**Casos especiales (references/casos-especiales.md):** regimenes fiscales no habituales como la Ley Beckham (con su escala propia del 24%/47% para trabajo y del 19%-28% para ahorro), la tributacion de criptomonedas (metodo FIFO, casillas especificas, modelos 721/172/173), el exit tax, la exencion del articulo 7.p para trabajo en el extranjero, el regimen de nomadas digitales, y las ganancias patrimoniales complejas con coeficientes de abatimiento.

**Fuente principal:** Toda esta informacion procede del Manual Practico de Renta 2025 publicado por la AEAT, un documento oficial de 1.903 paginas dividido en dos tomos PDF (1.270 paginas de normativa general + 633 paginas de deducciones autonomicas). Este skill condensa, estructura y organiza esas 1.903 paginas en archivos de referencia que Claude puede consultar de forma eficiente durante la conversacion con el contribuyente.

---

## Que es este skill

Es un conjunto de archivos de referencia fiscal y un flujo de trabajo guiado que permite a Claude:

1. Recibir y analizar el borrador de la AEAT (PDF o datos manuales)
2. Confirmar datos personales, familiares y de residencia
3. Formular preguntas dirigidas para descubrir posibles deducciones no incluidas
4. Cruzar la informacion con la normativa estatal y autonomica vigente
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
|       |-- preguntas-descubrimiento.md  # Cuestionario por categorias
|       |-- andalucia.md              # 17 deducciones
|       |-- aragon.md                 # 19 deducciones
|       |-- asturias.md               # 27 deducciones
|       |-- baleares.md               # 24 deducciones
|       |-- canarias.md               # 29 deducciones
|       |-- cantabria.md              # 21 deducciones
|       |-- castilla-la-mancha.md     # 27 deducciones
|       |-- castilla-y-leon.md        # 18 deducciones
|       |-- cataluna.md               # 13 deducciones
|       |-- extremadura.md            # 19 deducciones
|       |-- galicia.md                # 25 deducciones
|       |-- madrid.md                 # 23 deducciones
|       |-- murcia.md                 # 28 deducciones
|       |-- la-rioja.md               # 26 deducciones
|       |-- comunidad-valenciana.md   # 41 deducciones
|       |-- ceuta.md                  # Regimen especial (60%)
|       |-- melilla.md                # Regimen especial (60%)
```

---

## Como instalar el skill

### Opcion 1: Copiar la carpeta manualmente

1. Descarga o clona este repositorio
2. Copia la carpeta completa `declaracion-renta-espana/` dentro de tu directorio de skills de Claude:
   - En Cowork: dentro de la carpeta `.claude/skills/` de tu proyecto
   - En Claude Code: dentro de `.claude/skills/` en la raiz de tu proyecto

### Opcion 2: Clonar directamente en el directorio de skills

```bash
cd tu-proyecto/.claude/skills/
git clone https://github.com/joseconti/declaracion-renta-espana-2025.git declaracion-renta-espana
```

---

## Como usar el skill

Una vez instalado, el skill se activa automaticamente cuando mencionas temas relacionados con la declaracion de la renta en Espana. Por ejemplo:

- "Quiero revisar mi declaracion de la renta"
- "He subido mi borrador de la AEAT, puedes revisarlo?"
- "Que deducciones puedo aplicar en Madrid?"
- "Mi gestor ha preparado mi declaracion, puedes comprobar si falta alguna deduccion?"
- "Tengo criptomonedas, como las declaro?"
- "Me he mudado a Espana, puedo acogerme a la Ley Beckham?"

### Flujo tipico de uso

1. **Sube tu borrador** (PDF de Renta WEB) o facilita tus datos manualmente
2. **Confirma tu comunidad autonoma** de residencia y situacion personal
3. **Responde a las preguntas** que Claude te ira formulando por tematicas
4. **Recibe un informe** con:
   - Deducciones que ya aplicas correctamente
   - Deducciones adicionales identificadas con ahorro estimado
   - Recomendacion sobre tributacion individual vs conjunta
   - Puntos que requieren verificacion profesional

---

## Cobertura geografica

### Comunidades autonomas de regimen comun (todas cubiertas)

Andalucia, Aragon, Principado de Asturias, Illes Balears, Canarias, Cantabria, Castilla-La Mancha, Castilla y Leon, Cataluna, Extremadura, Galicia, Comunidad de Madrid, Region de Murcia, La Rioja, Comunitat Valenciana.

### Ciudades autonomas (cubiertas)

Ceuta y Melilla (regimen especial con deduccion del 60%).

### Regimen foral (NO cubierto)

Navarra y Pais Vasco (Alava, Bizkaia, Gipuzkoa) tienen haciendas forales propias con un IRPF diferente al estatal. Sus contribuyentes NO presentan la declaracion ante la AEAT sino ante sus respectivas Haciendas Forales. Este skill NO cubre dichos territorios.

---

## Casos especiales cubiertos

- Regimen de impatriados (Ley Beckham / art. 93 LIRPF), con escala propia de trabajo (24%/47%) y ahorro progresivo (19%-28%)
- Tributacion de criptomonedas (trading, staking, lending, airdrops, mining, metodo FIFO, casillas 1804/0027)
- Modelo 721 (cripto en el extranjero > 50.000 EUR)
- Modelo 720 (bienes en el extranjero > 50.000 EUR)
- No residentes con rentas en Espana (IRNR)
- Exit tax (impuesto de salida para residentes de 10+ anos)
- Exencion por trabajos en el extranjero (art. 7.p, hasta 60.100 EUR)
- Ganancias patrimoniales complejas (inmuebles, coeficientes de abatimiento, regimen transitorio pre-1994)
- Nomadas digitales (Ley 28/2022 de Startups)
- Regimen de atribucion de rentas (comunidades de bienes, herencias yacentes)
- Reduccion especial por rendimientos artisticos (novedad 2025, hasta 150.000 EUR)

---

## Novedades del ejercicio 2025

Este skill incorpora los cambios normativos introducidos para el ejercicio 2025:

- Incremento de la reduccion por rendimientos del trabajo: de 6.498 a 7.302 EUR, con 3 tramos en lugar de 2
- Elevacion del tipo maximo del ahorro: del 28% al 30% (tramo superior de 300.000 EUR en adelante)
- Nueva reduccion por rendimientos del trabajo artistico: 30% sobre rendimientos literarios, artisticos o cientificos que superen el 130% de la media de los 3 ejercicios anteriores
- Deducciones autonomicas nuevas o modificadas en varias CCAA (indicadas con "Novedad 2025" en cada archivo regional)
- Deduccion especial por DANA en la Comunitat Valenciana (octubre 2024)

---

## Anexos de municipios: deducciones por despoblamiento y zonas rurales

Una de las fuentes de ahorro fiscal mas desconocidas en Espana son las deducciones autonomicas vinculadas a municipios en riesgo de despoblamiento, municipios pequenos o zonas rurales. Muchas comunidades autonomas ofrecen deducciones significativas (de varios cientos a miles de euros) a contribuyentes que residen en estos municipios, pero la mayoria de la gente no sabe que su pueblo esta en la lista.

Por eso este skill incluye **anexos de municipios** en los archivos regionales correspondientes. Cuando el contribuyente indica su municipio de residencia, el skill cruza ese dato con las listas de municipios elegibles y le informa de las deducciones a las que tiene derecho.

### CCAA con deducciones vinculadas a municipios concretos

**La Rioja** es la CCAA con las listas mas detalladas. El archivo `la-rioja.md` incluye dos anexos completos con los nombres de todos los municipios elegibles:
- Anexo 1: 184 municipios con derecho a deducciones de pequenos municipios (vivienda, guarderia, hijos 0-3 anos, Internet y suministros para jovenes emancipados, alquiler para menores de 36 anos)
- Anexo 2: 193 municipios con derecho a deduccion por segunda vivienda en el medio rural

**Aragon:** deduccion de 600 euros por residencia en asentamientos clasificados como Rango X. La lista de asentamientos la publica el Gobierno de Aragon (ver anexo en `aragon.md`).

**Cantabria:** 5 deducciones diferentes (alquiler, guarderia, traslado, estudios, residencia habitual) para contribuyentes en municipios afectados por riesgo de despoblamiento, definidos por la Orden PRE/1/2025 (ver anexo en `cantabria.md`).

**Extremadura:** deduccion por residir en municipios o entidades locales menores con poblacion inferior a 3.000 habitantes. No requiere lista cerrada: se aplica a cualquier municipio que cumpla el criterio de poblacion segun el padron del INE (ver anexo en `extremadura.md`).

**Comunidad de Madrid:** deducciones por cambio de residencia y por adquisicion de vivienda habitual en municipios en riesgo de despoblacion, definidos por normativa autonomica (ver anexo en `madrid.md`).

**Comunitat Valenciana:** deduccion por residir habitualmente en un municipio en riesgo de despoblamiento, segun la clasificacion de la Generalitat a traves de la Agenda Valenciana Antidespoblament - AVANT (ver anexo en `comunidad-valenciana.md`).

Otras CCAA (Castilla-La Mancha, Castilla y Leon, Galicia, Asturias) tambien tienen deducciones para zonas rurales o despobladas, documentadas en sus respectivos archivos regionales.

**El skill pregunta siempre por el nombre exacto del municipio de residencia** y lo cruza con estos anexos. Si el contribuyente vive en un pueblo que esta en alguna de estas listas, el skill le informara de las deducciones adicionales a las que tiene derecho.

---

## Fuentes oficiales

Toda la informacion fiscal de este skill procede exclusivamente de fuentes oficiales. La fuente principal y mas completa es el Manual Practico de Renta 2025 de la AEAT, un documento de 1.903 paginas que la Agencia Tributaria publica cada ejercicio con la normativa consolidada.

### Fuente principal: Manual Practico de Renta 2025 (AEAT)

- [Manual Practico de Renta 2025 - Parte 1: Normativa general (PDF, 1.270 paginas)](https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025/ManualRenta2025Parte1_es_es.pdf)
- [Manual Practico de Renta 2025 - Parte 2: Deducciones autonomicas (PDF, 633 paginas)](https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025-Deducciones-autonomicas/ManualRenta2025Parte2_eu_es.pdf)
- [Manual Practico de Renta 2025 - Indice general (web)](https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html)
- [Manual Practico de Renta 2025 - Indice Deducciones autonomicas (web)](https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100/deducciones-autonomicas.html)

### Agencia Estatal de Administracion Tributaria (AEAT) - Otras fuentes

- [Guia de Deducciones Autonomicas del IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html)
- [Deducciones generales y autonomicas aplicables en 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/introduccion/deducciones-generales-autonomicas-aplicables.html)
- [Gravamen estatal IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-general/gravamen-estatal.html)
- [Gravamen ahorro estatal IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-ahorro/gravamen-estatal.html)
- [Minimo personal y familiar 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c14-adecuacion-impuesto-circunstancias-personales/cuadro-resumen-minimo-personal-familiar.html)
- [Regimen especial impatriados (Ley Beckham)](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/manual-tributacion-no-residentes/regimenes-opcionales/regimen-especial-impatriados.html)
- [Monedas virtuales - Tributacion IRPF](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2024/c11-ganancias-perdidas-patrimoniales/monedas-virtuales/compra-venta-monedas-virtuales-tributacion-inversor.html)
- [Campana de Renta 2025](https://sede.agenciatributaria.gob.es/Sede/Renta.html)
- [Deduccion rentas Ceuta/Melilla](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/deduccion-rentas-obtenidas-ceuta-melilla.html)
- [Pagina general de manuales practicos](https://sede.agenciatributaria.gob.es/Sede/manuales-practicos.html)

### Boletin Oficial del Estado (BOE)

- [Orden HAC/277/2026 - Modelos declaracion Renta 2025](https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041)
- [Ley 28/2022 - Ley de Startups (nomadas digitales)](https://www.boe.es/buscar/act.php?id=BOE-A-2022-21739)
- [Orden HAC/242/2025 - Modelos declaracion Renta 2024](https://www.boe.es/buscar/act.php?id=BOE-A-2025-5049)

---

## Cifras del skill

- 1.903 paginas del Manual Practico de la AEAT condensadas y estructuradas
- 15 comunidades autonomas de regimen comun cubiertas
- 2 ciudades autonomas (Ceuta y Melilla) con regimen especial
- Mas de 350 deducciones autonomicas documentadas con porcentajes, limites y requisitos
- 11 categorias de deducciones estatales
- 8 regimenes y casos especiales (Beckham, cripto, no residentes, etc.)
- 56 preguntas de descubrimiento organizadas en 6 categorias
- 6 tramos de la escala general estatal + 5 tramos de la escala del ahorro
- Minimos personales y familiares por edad, parentesco y discapacidad

---

## Limitaciones conocidas

- **No cubre regimen foral** (Navarra, Pais Vasco). Estos territorios tienen normativa fiscal propia.
- **No calcula el impuesto.** Este skill identifica deducciones y orienta, pero no genera la autoliquidacion.
- **No accede a los sistemas de la AEAT.** No puede consultar datos fiscales reales del contribuyente; trabaja con la informacion que el usuario le facilita.
- **Ejercicio 2025 unicamente.** La normativa de ejercicios anteriores puede diferir.
- **Canarias requiere revision manual.** Muchas deducciones canarias no aparecen automaticamente en el borrador de la AEAT.
- **Cuantias aproximadas en algunos casos.** Aunque la fuente principal es el PDF oficial de 1.903 paginas de la AEAT, algunas deducciones autonomicas tienen formulas y condiciones muy complejas. Cuando no ha sido posible condensar todos los matices, se indica que se consulte la fuente oficial.

---

## Contribuir

Las contribuciones son bienvenidas, especialmente:

- Correcciones de datos fiscales con referencia a la fuente oficial (pagina del PDF o URL de la AEAT)
- Actualizaciones cuando cambie la normativa
- Ampliacion de cuantias en deducciones autonomicas que falten detalle
- Inclusion de territorios forales (Navarra, Pais Vasco)
- Traducciones (catalan, euskera, gallego, valenciano)

Para contribuir, abre un issue o pull request. Toda aportacion debe incluir la fuente oficial que respalde el dato.

---

## Licencia

Este proyecto esta licenciado bajo la **GNU General Public License v3.0 (GPLv3)**.

Consulta el archivo [LICENSE](LICENSE) para los terminos completos.

En resumen: puedes usar, modificar y distribuir este software libremente, siempre que cualquier obra derivada se distribuya tambien bajo GPLv3 y se mantenga el aviso de copyright y el descargo de responsabilidad.

---

## Autor

Jose Conti - [joseconti.com](https://joseconti.com)

---

## Aviso legal final

Este software se distribuye con la esperanza de que sea util, pero **SIN NINGUNA GARANTIA**; ni siquiera la garantia implicita de COMERCIABILIDAD o IDONEIDAD PARA UN PROPOSITO PARTICULAR. Consulta la GNU General Public License v3.0 para mas detalles.

La informacion fiscal contenida puede no estar actualizada o ser inexacta. **Consulta siempre con un profesional antes de tomar decisiones fiscales.** El uso de este skill no crea ninguna relacion de asesoramiento profesional entre el autor y el usuario.
