# Declaración de la Renta - España (IRPF 2025)

Skill para Claude / Cowork que asiste al contribuyente español en la revisión, optimización o preparación desde cero de su declaración del Impuesto sobre la Renta de las Personas Físicas (IRPF), ejercicio 2025. Soporta tres modos de trabajo: revisión de borradores existentes, preparación completa a partir de documentación en bruto (nóminas, certificados bancarios, facturas de autónomo, etc.), e híbrido (borrador + datos adicionales).

**Ejercicio fiscal:** 2025 (del 1 de enero al 31 de diciembre de 2025)
**Campaña de presentación:** del 8 de abril al 30 de junio de 2026
**Domiciliación bancaria del pago:** hasta el 25 de junio de 2026
**Segundo plazo (40%):** hasta el 5 de noviembre de 2026

---

## DESCARGO DE RESPONSABILIDAD

**ESTE SOFTWARE SE PROPORCIONA "TAL CUAL", SIN GARANTÍA DE NINGÚN TIPO.**

Este skill es una herramienta de orientación fiscal de carácter informativo. **NO constituye asesoramiento fiscal, contable ni jurídico profesional.** No sustituye en ningún caso la consulta con un asesor fiscal colegiado, gestor administrativo o abogado tributarista.

**El usuario es el único responsable** de las decisiones fiscales que tome basándose en la información proporcionada por este skill. Ni el autor ni los colaboradores asumen responsabilidad alguna por errores, omisiones, pérdidas económicas, sanciones administrativas o cualquier otro perjuicio derivado directa o indirectamente del uso de esta herramienta.

La normativa fiscal española es compleja y cambia con frecuencia. Las deducciones están sujetas a condiciones, límites de renta, incompatibilidades y requisitos documentales que pueden variar y que este skill no siempre puede verificar completamente.

**Uso recomendado:** Este skill está pensado como herramienta complementaria. Un caso de uso ideal es verificar que una declaración ya preparada por un gestor profesional incluye todas las deducciones posibles. Puede servir como "checklist" para no dejarse nada, pero la decisión final y la responsabilidad de la declaración siempre recaen en el contribuyente y, en su caso, en su asesor.

**En caso de duda, consulta siempre con un profesional cualificado.**

---

## Qué contiene este skill y por qué es tan extenso

El IRPF español es uno de los impuestos más complejos de Europa. No es un impuesto único: es un sistema de escalas, mínimos, reducciones, deducciones estatales y deducciones autonómicas que interactúan entre sí, con condiciones y límites diferentes según la situación personal, familiar, geográfica y económica de cada contribuyente.

Para dar una idea del volumen de información que maneja este skill:

**Normativa estatal (references/nacional.md):** contiene la residencia fiscal (regla de los 183 dias, centro de intereses economicos, presuncion por familia), la individualizacion de rentas (gananciales vs separacion de bienes, art. 11 LIRPF), las escalas de gravamen general (6 tramos del 9,50% al 24,50%) y del ahorro (5 tramos del 9,50% al 15,00%), los minimos personales y familiares (contribuyente, descendientes, ascendientes, discapacidad), las formulas de reduccion por rendimientos del trabajo (con 3 tramos y formulas como 7.302 - [1,75 x (RNT - 14.852)]), los gastos deducibles, las rentas exentas, las reducciones de base imponible, 11 categorias de deducciones estatales con sus porcentajes y bases maximas, la tributacion conjunta vs individual con estrategia detallada de decision (cuando conviene cada opcion, parejas de hecho), y las obligaciones formales completas (8 modelos de declaracion, 5 formas de presentacion incluyendo Renta Directa, medios de identificacion, fraccionamiento 60/40 con fechas, autoliquidacion rectificativa, conservacion documental).

**Deducciones autonómicas (references/regiones/):** cada comunidad autónoma tiene competencia para establecer sus propias deducciones de la cuota. Este skill incluye un archivo por cada una de las 15 CCAA de régimen común más Ceuta y Melilla, con un total de más de 350 deducciones autonómicas documentadas. La Comunitat Valenciana tiene 41 deducciones propias, Canarias 29, Región de Murcia 28, Asturias 27, Castilla-La Mancha 27, La Rioja 26, Galicia 25, Illes Balears 24 y así sucesivamente. Cada deducción tiene sus propios porcentajes, límites, requisitos de renta, condiciones de edad, situación familiar, incompatibilidades con otras deducciones, y en muchos casos requisitos documentales específicos.

**Casos especiales (references/casos-especiales.md):** regimenes fiscales no habituales como la Ley Beckham (con su escala propia del 24%/47% para trabajo y del 19%-30% para ahorro), la tributacion de criptomonedas (metodo FIFO, casillas especificas, modelos 721/172/173), el exit tax, la exencion del articulo 7.p para trabajo en el extranjero, el regimen de nomadas digitales (comparativa detallada con Beckham clasica, visa de nomada digital con requisitos y duracion, exclusion de autonomos), la atribucion de rentas (comunidades de bienes, herencias yacentes, Modelo 184, ejemplos practicos), y las ganancias patrimoniales complejas con coeficientes de abatimiento.

**Territorios forales (references/regiones/navarra.md, alava.md, bizkaia.md, gipuzkoa.md):** Navarra y las tres provincias vascas (Álava, Bizkaia, Gipuzkoa) tienen un IRPF completamente independiente del estatal, con sus propias escalas de gravamen, mínimos personales y familiares, reducciones y deducciones. Cada archivo foral es un sistema fiscal completo en sí mismo. Por ejemplo, Navarra tiene 11 tramos del 13% al 52% (frente a los 6 tramos estatales), y las tres provincias vascas comparten una estructura de 7-8 tramos del 23% al 49% pero con deducciones propias cada una.

**Actividades económicas (references/autonomos.md):** referencia completa para contribuyentes autónomos y profesionales. Incluye los 3 regímenes disponibles (Estimación Directa Simplificada hasta 600.000 EUR, Estimación Directa Normal, y Módulos hasta 250.000 EUR), un catálogo de 24 categorías de gastos deducibles con criterios y límites, la tabla simplificada de amortización (12 grupos de activos), los gastos de difícil justificación (7%, hasta 2.000 EUR), las retenciones por tipo de actividad (10 tipos), los pagos fraccionados trimestrales (modelos 130 y 131 con fórmulas de cálculo), y la conciliación anual con la cuota diferencial del IRPF.

**Modo preparación (references/modo-preparacion.md):** flujo de trabajo genérico para calcular la declaración desde cero cuando el contribuyente no tiene borrador. Define 9 bloques de datos a recoger (identidad, trabajo, capital financiero, inmuebles, autónomo, ganancias, retenciones, donaciones, deducciones), instrucciones para normalizar documentos heterogéneos (PDF, Excel, CSV, imágenes escaneadas, texto pegado), el proceso de consolidación y cálculo, y el entregable final ("paquete Renta WEB") con las casillas principales y una checklist de verificación profesional.

**Fuentes:** Toda esta información procede exclusivamente de documentación oficial. La fuente principal para el régimen común es el Manual Práctico de Renta 2025 de la AEAT (1.903 páginas en dos tomos PDF). Para los territorios forales, se han procesado los manuales oficiales de las cuatro haciendas forales (1.311 páginas adicionales: Navarra 308p, Álava 243p, Gipuzkoa 214p, Bizkaia 546p). En total, **3.214 páginas de documentación oficial** condensadas y estructuradas en archivos de referencia que Claude puede consultar durante la conversación con el contribuyente.

---

## Qué es este skill

Es un conjunto de archivos de referencia fiscal y un flujo de trabajo guiado que permite a Claude trabajar en tres modos:

**Modo Revisión:** El contribuyente tiene un borrador (AEAT o Hacienda Foral) y quiere revisarlo.
1. Recibir y analizar el borrador (PDF o datos manuales)
2. Confirmar datos personales, familiares y de residencia (incluyendo detección automática de régimen foral)
3. Formular preguntas dirigidas para descubrir posibles deducciones no incluidas
4. Cruzar la información con la normativa estatal, autonómica o foral vigente
5. Presentar un informe con deducciones adicionales identificadas y ahorro estimado

**Modo Preparación:** El contribuyente NO tiene borrador y quiere calcular su declaración desde cero.
1. Recibir documentación en bruto (nóminas, certificados bancarios, facturas, etc.) en formatos heterogéneos (PDF, Excel, CSV, imágenes, texto)
2. Normalizar y consolidar datos en bloques temáticos (trabajo, inmuebles, inversiones, actividad económica, etc.)
3. Calcular rendimientos netos, base imponible, cuotas y deducciones aplicando la normativa vigente
4. Presentar un "paquete Renta WEB" con las casillas principales, resultado (a ingresar/devolver) y checklist de verificación

**Modo Híbrido:** El contribuyente tiene borrador pero le faltan datos (ingresos de autónomo, ventas no comunicadas, etc.). Combina ambos flujos.

**Nota sobre territorios forales:** Si el contribuyente reside en Navarra, Álava, Bizkaia o Gipuzkoa, el skill detecta automáticamente que se trata de un régimen foral y adapta el flujo: utiliza las escalas, mínimos y deducciones del territorio foral correspondiente en lugar de la normativa estatal.

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
|   |-- nacional.md                   # Normativa IRPF estatal 2025 completa (~1.200 lineas)
|   |-- casos-especiales.md           # Ley Beckham, cripto, no residentes, nomadas digitales, atribucion de rentas
|   |-- autonomos.md                  # Actividades economicas: EDS/EDN/Modulos, gastos, pagos fraccionados
|   |-- modo-preparacion.md           # Flujo de preparacion desde cero (modo B)
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
|       |--                           #
|       |-- # --- Territorios forales (IRPF propio independiente) ---
|       |-- navarra.md                # IRPF foral 2025 completo (13%-52%, 11 tramos)
|       |-- alava.md                  # IRPF foral 2025 completo (23%-49%, 7 tramos)
|       |-- bizkaia.md                # IRPF foral 2024 (23%-49%, 8 tramos) *pendiente 2025
|       |-- gipuzkoa.md               # IRPF foral 2025 completo (23%-49%, 8 tramos)
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
git clone https://github.com/joseconti/declaracion-renta-espana.git declaracion-renta-espana
```

---

## Cómo usar el skill

Una vez instalado, el skill se activa automáticamente cuando mencionas temas relacionados con la declaración de la renta en España. Por ejemplo:

- "Quiero revisar mi declaración de la renta"
- "He subido mi borrador de la AEAT, ¿puedes revisarlo?"
- "¿Qué deducciones puedo aplicar en Madrid?"
- "Mi gestor ha preparado mi declaración, ¿puedes comprobar si falta alguna deducción?"
- "Tengo criptomonedas, ¿cómo las declaro?"
- "Me he mudado a España, ¿puedo acogerme a la Ley Beckham?"
- "Vivo en Gipuzkoa, ¿qué deducciones me corresponden?"
- "Soy de Navarra, ¿cómo funciona mi IRPF foral?"
- "Quiero preparar mi renta desde cero, tengo mis nóminas y certificados"
- "Soy autónomo y quiero calcular mi declaración"
- "Tengo el borrador pero me faltan los ingresos de autónomo"

### Flujo típico de uso

1. **Sube tu borrador** (PDF de Renta WEB de la AEAT o de tu Hacienda Foral) o facilita tus datos manualmente
2. **Confirma tu comunidad autónoma o territorio foral** de residencia y situación personal
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

### Territorios forales (cubiertos)

Navarra y País Vasco (Álava, Bizkaia, Gipuzkoa) tienen haciendas forales propias con un IRPF completamente independiente del estatal. Sus contribuyentes NO presentan la declaración ante la AEAT sino ante sus respectivas Haciendas Forales. Este skill incluye archivos de referencia completos para los 4 territorios forales, con sus propias escalas, mínimos, reducciones y deducciones.

- **Navarra:** IRPF foral 2025, escala general 13%-52% (11 tramos), escala ahorro 20%-28% (6 tramos). Fuente: Manual Práctico IRPF 2025 de Hacienda Foral de Navarra (308 páginas).
- **Álava/Araba:** IRPF foral 2025, escala general 23%-49% (7 tramos), escala ahorro 20%-25% (5 tramos). Fuente: Manual Práctico IRPF 2025 de la Diputación Foral de Álava (243 páginas).
- **Gipuzkoa:** IRPF foral 2025, escala general 23%-49% (8 tramos), escala ahorro 20%-25% (5 tramos). Fuente: Manual Práctico IRPF 2025 de la Diputación Foral de Gipuzkoa (214 páginas).
- **Bizkaia:** IRPF foral 2024 (manual 2025 no publicado al cierre de este skill), escala general 23%-49% (8 tramos), escala ahorro 20%-25% (5 tramos). Fuente: Manual Práctico IRPF 2024 de la Diputación Foral de Bizkaia (546 páginas).

---

## Casos especiales cubiertos

- Régimen de impatriados (Ley Beckham / art. 93 LIRPF), con escala propia de trabajo (24%/47%) y ahorro progresivo (19%-28%)
- Tributación de criptomonedas (trading, staking, lending, airdrops, mining, método FIFO, casillas 1804/0027)
- Modelo 721 (cripto en el extranjero > 50.000 EUR)
- Modelo 720 (bienes en el extranjero > 50.000 EUR)
- No residentes con rentas en España (IRNR)
- Exit tax (impuesto de salida para residentes de 10+ años)
- Exención por trabajos en el extranjero (art. 7.p, hasta 60.100 EUR)
- Ganancias patrimoniales complejas (inmuebles, coeficientes de abatimiento, régimen transitorio pre-1994)
- Nomadas digitales (Ley 28/2022 de Startups): comparativa detallada con Beckham clasica, visa con requisitos, exclusion de autonomos
- Regimen de atribucion de rentas (comunidades de bienes, herencias yacentes, sociedades civiles): Modelo 184, ejemplo practico de CB inmobiliaria, venta de inmuebles en CB
- Reducción especial por rendimientos artísticos (novedad 2025, hasta 150.000 EUR)

---

## Novedades del ejercicio 2025

Este skill incorpora los cambios normativos introducidos para el ejercicio 2025:

- Incremento de la reducción por rendimientos del trabajo: de 6.498 a 7.302 EUR, con 3 tramos en lugar de 2
- Elevación del tipo máximo del ahorro: del 28% al 30% (tramo superior de 300.000 EUR en adelante)
- Nueva reducción por rendimientos del trabajo artístico: 30% sobre rendimientos literarios, artísticos o científicos que superen el 130% de la media de los 3 ejercicios anteriores
- Deducciones autonómicas nuevas o modificadas en varias CCAA (indicadas con "Novedad 2025" en cada archivo regional)
- Deducción especial por DANA en la Comunitat Valenciana (octubre 2024)

---

## Anexos de municipios: deducciones por despoblamiento y zonas rurales

Una de las fuentes de ahorro fiscal más desconocidas en España son las deducciones autonómicas vinculadas a municipios en riesgo de despoblamiento, municipios pequeños o zonas rurales. Muchas comunidades autónomas ofrecen deducciones significativas (de varios cientos a miles de euros) a contribuyentes que residen en estos municipios, pero la mayoría de la gente no sabe que su pueblo está en la lista.

Por eso este skill incluye **anexos de municipios** en los archivos regionales correspondientes. Cuando el contribuyente indica su municipio de residencia, el skill cruza ese dato con las listas de municipios elegibles y le informa de las deducciones a las que tiene derecho.

### CCAA con deducciones vinculadas a municipios concretos

**La Rioja** es la CCAA con las listas más detalladas. El archivo `la-rioja.md` incluye dos anexos completos con los nombres de todos los municipios elegibles:
- Anexo 1: 184 municipios con derecho a deducciones de pequeños municipios (vivienda, guardería, hijos 0-3 años, Internet y suministros para jóvenes emancipados, alquiler para menores de 36 años)
- Anexo 2: 193 municipios con derecho a deducción por segunda vivienda en el medio rural

**Aragón:** deducción de 600 euros por residencia en asentamientos clasificados como Rango X. La lista de asentamientos la publica el Gobierno de Aragón (ver anexo en `aragon.md`).

**Cantabria:** 5 deducciones diferentes (alquiler, guardería, traslado, estudios, residencia habitual) para contribuyentes en municipios afectados por riesgo de despoblamiento, definidos por la Orden PRE/1/2025 (ver anexo en `cantabria.md`).

**Extremadura:** deducción por residir en municipios o entidades locales menores con población inferior a 3.000 habitantes. No requiere lista cerrada: se aplica a cualquier municipio que cumpla el criterio de población según el padrón del INE (ver anexo en `extremadura.md`).

**Comunidad de Madrid:** deducciones por cambio de residencia y por adquisición de vivienda habitual en municipios en riesgo de despoblación, definidos por normativa autonómica (ver anexo en `madrid.md`).

**Comunitat Valenciana:** deducción por residir habitualmente en un municipio en riesgo de despoblamiento, según la clasificación de la Generalitat a través de la Agenda Valenciana Antidespoblament - AVANT (ver anexo en `comunidad-valenciana.md`).

Otras CCAA (Castilla-La Mancha, Castilla y León, Galicia, Asturias) también tienen deducciones para zonas rurales o despobladas, documentadas en sus respectivos archivos regionales.

**El skill pregunta siempre por el nombre exacto del municipio de residencia** y lo cruza con estos anexos. Si el contribuyente vive en un pueblo que está en alguna de estas listas, el skill le informará de las deducciones adicionales a las que tiene derecho.

---

## Fuentes oficiales

Toda la información fiscal de este skill procede exclusivamente de fuentes oficiales. Para el régimen común, la fuente principal es el Manual Práctico de Renta 2025 de la AEAT (1.903 páginas). Para los territorios forales, se han utilizado los manuales oficiales publicados por cada hacienda foral (1.311 páginas adicionales).

### Fuente principal: Manual Práctico de Renta 2025 (AEAT)

- [Manual Práctico de Renta 2025 - Parte 1: Normativa general (PDF, 1.270 páginas)](https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025/ManualRenta2025Parte1_es_es.pdf)
- [Manual Práctico de Renta 2025 - Parte 2: Deducciones autonómicas (PDF, 633 páginas)](https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025-Deducciones-autonomicas/ManualRenta2025Parte2_eu_es.pdf)
- [Manual Práctico de Renta 2025 - Índice general (web)](https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html)
- [Manual Práctico de Renta 2025 - Índice Deducciones autonómicas (web)](https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100/deducciones-autonomicas.html)

### Agencia Estatal de Administración Tributaria (AEAT) - Otras fuentes

- [Guía de Deducciones Autonómicas del IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html)
- [Deducciones generales y autonómicas aplicables en 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/introduccion/deducciones-generales-autonomicas-aplicables.html)
- [Gravamen estatal IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-general/gravamen-estatal.html)
- [Gravamen ahorro estatal IRPF 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-ahorro/gravamen-estatal.html)
- [Mínimo personal y familiar 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c14-adecuacion-impuesto-circunstancias-personales/cuadro-resumen-minimo-personal-familiar.html)
- [Régimen especial impatriados (Ley Beckham)](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/manual-tributacion-no-residentes/regimenes-opcionales/regimen-especial-impatriados.html)
- [Monedas virtuales - Tributación IRPF](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2024/c11-ganancias-perdidas-patrimoniales/monedas-virtuales/compra-venta-monedas-virtuales-tributacion-inversor.html)
- [Campaña de Renta 2025](https://sede.agenciatributaria.gob.es/Sede/Renta.html)
- [Servicios de ayuda Campaña Renta 2025](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c01-campana-declaracion-renta/servicios-ayuda-campana-renta.html)
- [Residencia habitual en territorio español](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c02-irpf-cuestiones-generales/sujecion-irpf-aspectos-personales/residencia-habitual-territorio-espanol.html)
- [Tributacion individual y opcion por tributacion conjunta](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c02-irpf-cuestiones-generales/sujecion-irpf-aspectos-personales/tributacion-individual-opcion-tributacion-conjunta.html)
- [Reduccion por tributacion conjunta](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c13-determinacion-renta-contribuyente-sujeta-gravamen/reducciones-base-imponible-general/reduccion-tributacion-conjunta.html)
- [Pago en dos plazos: Fraccionamiento especial 60/40](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c01-campana-declaracion-renta/pago-deuda-tributaria-irpf/opciones-pago/pago-dos-plazos.html)
- [Autoliquidacion rectificativa - Modificar declaracion presentada](https://sede.agenciatributaria.gob.es/Sede/irpf/campana-renta/modificacion-declaracion-renta-2025-presentada/resultado-autoliquidacion-rectificativa-ingresar-menor-importe.html)
- [Entidades en regimen de atribucion de rentas](https://sede.agenciatributaria.gob.es/Sede/irpf/empresarios-individuales-profesionales/entidades-regimen-atribucion-renta.html)
- [Modelo 184 - Declaracion informativa atribucion de rentas](https://sede.agenciatributaria.gob.es/Sede/procedimientoini/GI04.shtml)
- [Deduccion rentas Ceuta/Melilla](https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/deduccion-rentas-obtenidas-ceuta-melilla.html)
- [Pagina general de manuales practicos](https://sede.agenciatributaria.gob.es/Sede/manuales-practicos.html)

### Haciendas Forales

- [Hacienda Foral de Navarra - Manual Práctico IRPF 2025](https://hacienda.navarra.es)
- [Diputación Foral de Álava - Manual Práctico IRPF 2025](https://web.araba.eus/es/hacienda)
- [Diputación Foral de Bizkaia - Manual Práctico IRPF 2024](https://www.bizkaia.eus/es/hacienda-y-finanzas)
- [Diputación Foral de Gipuzkoa - Manual Práctico IRPF 2025](https://www.gipuzkoa.eus/es/hacienda-y-finanzas)

### Boletín Oficial del Estado (BOE)

- [Orden HAC/277/2026 - Modelos declaración Renta 2025](https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041)
- [Ley 28/2022 - Ley de Startups (nómadas digitales)](https://www.boe.es/buscar/act.php?id=BOE-A-2022-21739)
- [Orden HAC/242/2025 - Modelos declaracion Renta 2024 y autoliquidacion rectificativa](https://www.boe.es/buscar/act.php?id=BOE-A-2025-5049)
- [Ley 35/2006 del IRPF (texto consolidado)](https://www.boe.es/buscar/doc.php?id=BOE-A-2006-20764)
- [Ley 6/2017 - Reformas Urgentes del Trabajo Autonomo](https://www.boe.es/buscar/doc.php?id=BOE-A-2017-12207)

---

## Cifras del skill

- 1.903 páginas del Manual Práctico de la AEAT condensadas y estructuradas
- 1.311 páginas adicionales de los 4 manuales forales (Navarra 308p, Álava 243p, Gipuzkoa 214p, Bizkaia 546p)
- 15 comunidades autónomas de régimen común cubiertas
- 4 territorios forales cubiertos (Navarra, Álava, Bizkaia, Gipuzkoa) con IRPF completo propio
- 2 ciudades autónomas (Ceuta y Melilla) con régimen especial
- Mas de 383 deducciones autonomicas documentadas con porcentajes exactos, importes en euros, limites de renta individual/conjunta, formulas de reduccion, requisitos de edad/discapacidad/situacion personal, incompatibilidades y reglas de prorrateo (todos verificados contra las paginas AEAT)
- 11 categorias de deducciones estatales
- 8 regimenes y casos especiales (Beckham, cripto, no residentes, nomadas digitales, atribucion de rentas, etc.)
- Residencia fiscal completa (3 criterios del art. 9 LIRPF, paraisos fiscales, clausula anti-deslocalizacion)
- Individualizacion de rentas (art. 11 LIRPF, gananciales vs separacion de bienes)
- Tributacion conjunta vs individual con estrategia de decision detallada
- 8 modelos de declaracion documentados (100, 102, 714, 720, 721, 149, 151, 184)
- 24 categorías de gastos deducibles para autónomos con criterios y límites
- 3 regímenes de actividades económicas documentados (EDS, EDN, Módulos)
- 3 ejemplos numéricos completos de liquidación (asalariado, autónomo, arrendador)
- 98 preguntas de descubrimiento organizadas en 9 categorias (incluyendo fuentes de datos, autonomos y perfiles especificos)
- 6 tramos de la escala general estatal + 5 tramos de la escala del ahorro
- 4 escalas forales completas (Navarra 11 tramos, Álava 7, Bizkaia 8, Gipuzkoa 8)
- Mínimos personales y familiares por edad, parentesco y discapacidad (estatales y forales)
- 3.214 páginas de documentación oficial procesadas en total

---

## Limitaciones conocidas

- **Bizkaia usa datos de 2024.** El manual 2025 de Bizkaia no estaba publicado al cierre de este skill. Las cuantías pueden variar ligeramente.
- **En modo preparación, los cálculos son orientativos.** El skill puede calcular la declaración desde datos en bruto, pero el resultado debe verificarse siempre contra los datos fiscales de la AEAT y/o con un asesor profesional antes de presentar.
- **No accede a los sistemas de la AEAT.** No puede consultar datos fiscales reales del contribuyente; trabaja con la información que el usuario le facilita.
- **No cumplimenta Renta WEB.** El skill calcula importes y presenta las casillas principales, pero el contribuyente o su asesor debe introducir los datos manualmente en la plataforma de la AEAT.
- **Ejercicio 2025 únicamente.** La normativa de ejercicios anteriores puede diferir.
- **Canarias requiere revisión manual.** Muchas deducciones canarias no aparecen automáticamente en el borrador de la AEAT.
- **Cuantías aproximadas en algunos casos.** Aunque la fuente principal es el PDF oficial de 1.903 páginas de la AEAT, algunas deducciones autonómicas tienen fórmulas y condiciones muy complejas. Cuando no ha sido posible condensar todos los matices, se indica que se consulte la fuente oficial.
- **Deducciones restringidas.** Muchas deducciones autonómicas (especialmente las de alquiler de vivienda) existen en la normativa pero solo son aplicables a perfiles concretos (jóvenes, desempleados, discapacitados, familias numerosas, etc.). Los requisitos de acceso están documentados en cada archivo regional, pero el skill advierte siempre de que la existencia de una deducción no implica que sea aplicable a todos los contribuyentes.

---

## Contribuir

Las contribuciones son bienvenidas, especialmente:

- Correcciones de datos fiscales con referencia a la fuente oficial (página del PDF o URL de la AEAT)
- Actualizaciones cuando cambie la normativa
- Ampliación de cuantías en deducciones autonómicas que falten detalle
- Actualización del manual de Bizkaia cuando se publique el ejercicio 2025
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
