---
name: declaracion-renta-espana
description: >
  Asistente para la Declaración de la Renta (IRPF) en España, ejercicio 2025.
  Dos modos de trabajo: (1) Revisión: analiza borradores de la AEAT o de haciendas
  forales, identifica deducciones no aplicadas y oportunidades de ahorro fiscal.
  (2) Preparación: calcula la declaración desde cero a partir de nóminas, certificados
  bancarios, facturas y otros documentos en bruto. Usa este skill siempre que el
  usuario mencione declaración de la renta, IRPF, borrador de Hacienda, deducciones
  fiscales en España, impuestos en España, renta 2025, campaña de la renta, Agencia
  Tributaria, preparar la renta, calcular la renta, autónomo/autónoma, o cualquier
  consulta relacionada con la fiscalidad personal en España. También cuando el
  usuario quiera revisar si su gestor ha incluido todas las deducciones posibles,
  o cuando suba un PDF/documento del borrador de la AEAT, o cuando quiera calcular
  su declaración a partir de documentación en bruto.
---

# Declaración de la Renta - España (IRPF 2025)

Skill para asistir al contribuyente español en la revisión, optimización o preparación
desde cero de su declaración del Impuesto sobre la Renta de las Personas Físicas (IRPF),
ejercicio 2025. Soporta dos modos de trabajo: revisión de borradores existentes y
preparación completa a partir de documentación en bruto.

## DESCARGO DE RESPONSABILIDAD

IMPORTANTE: Este skill es una herramienta de orientación fiscal. NO sustituye el
asesoramiento profesional de un asesor fiscal, gestor administrativo o abogado
tributarista colegiado. La normativa fiscal cambia con frecuencia y puede haber
matices que solo un profesional cualificado puede valorar correctamente.

La información contenida procede de fuentes oficiales (AEAT, BOE) pero puede
contener errores, omisiones o haber quedado desactualizada. El usuario es el
único responsable de las decisiones fiscales que tome.

Este skill puede ser especialmente útil para verificar que una declaración ya
preparada por un gestor incluye todas las deducciones posibles, pero NUNCA debe
ser la única fuente para tomar decisiones fiscales.

---

## FLUJO DE TRABAJO

El skill sigue un proceso estructurado en fases. Cada fase depende de la anterior.
No saltar fases ni hacer todas las preguntas de golpe.

### FASE 0: Selección de modo

Antes de cualquier otra acción, determinar en qué modo trabaja el skill. Preguntar
al usuario o deducirlo del contexto:

**Modo A - Revisión:** El contribuyente YA tiene un borrador (de la AEAT o de su
Hacienda Foral) y quiere revisarlo para identificar deducciones no aplicadas o
errores. Flujo: Fase 1-A -> Fase 2 -> Fase 3 -> Fase 4 -> Fase 5.

**Modo B - Preparación:** El contribuyente NO tiene borrador y quiere calcular su
declaración desde cero a partir de documentación en bruto (nóminas, certificados
bancarios, facturas, etc.). Flujo: Fase 1-B -> Fase 2 -> Fase 3 -> Fase 4-prep -> Fase 5-prep.

**Modo C - Híbrido:** El contribuyente tiene un borrador pero sabe que le faltan
datos (por ejemplo, ingresos de autónomo, ventas de inmuebles o inversiones no
comunicadas a la AEAT). Flujo: Fase 1-A + Fase 1-B (parcial) -> Fase 2 -> Fase 3
-> Fase 4 + Fase 4-prep (parcial) -> Fase 5.

Si el usuario dice "quiero revisar mi borrador", "mi gestor ha preparado esto",
"mira si falta algo" -> Modo A.

Si el usuario dice "quiero preparar mi renta", "tengo mis nóminas y certificados",
"no tengo borrador", "soy autónomo y quiero calcular" -> Modo B.

Si el usuario dice "tengo el borrador pero me faltan los ingresos de autónomo",
"el borrador no incluye la venta del piso" -> Modo C.

Documentos de referencia para el modo preparación:
- `references/modo-preparacion.md` - Flujo genérico de preparación desde cero
- `references/autonomos.md` - Solo si hay actividades económicas (cargar bajo demanda)

### FASE 1-A: Recepción del borrador (Modo Revisión)

Lo primero es solicitar al usuario que facilite su borrador de la declaracion.

Decir algo como:

> Para poder ayudarte con tu declaración de la Renta 2025, necesito que me
> facilites tu borrador de la AEAT. Puedes:
>
> - Subir el PDF del borrador descargado de Renta WEB
> - Copiar y pegar los datos principales
> - Facilitarme los datos manualmente
>
> Con el borrador puedo identificar qué deducciones ya se están aplicando y
> cuáles podrían estar faltando.

Si el usuario sube un PDF, leerlo y extraer:
- NIF/NIE del declarante (y cónyuge si declaración conjunta)
- Tipo de declaración (individual/conjunta)
- Comunidad autónoma de residencia
- Rendimientos del trabajo (casilla 0001 y siguientes)
- Rendimientos del capital inmobiliario
- Rendimientos del capital mobiliario
- Rendimientos de actividades económicas
- Ganancias y pérdidas patrimoniales
- Base imponible general y del ahorro
- Base liquidable general y del ahorro
- Mínimo personal y familiar aplicado
- Deducciones ya aplicadas (estatales y autonómicas)
- Resultado de la declaración (a ingresar/devolver)

Si no tiene el borrador, valorar si el modo correcto es Preparación (Fase 1-B).

### FASE 1-B: Ingesta de documentación en bruto (Modo Preparación)

En modo preparación, el contribuyente no tiene borrador. En su lugar, facilita
documentos fuente heterogéneos. Seguir el flujo detallado en `references/modo-preparacion.md`.

**Tipos de documentos aceptados:**
- PDF: nóminas, certificados de retenciones (modelo 10T), certificados bancarios,
  escrituras, contratos de alquiler, facturas
- Excel/CSV: extractos bancarios, listados de operaciones bursátiles, exportaciones
  de exchanges de criptomonedas
- Imágenes escaneadas: recibos, tickets, facturas en papel, certificados
- Texto pegado: datos copiados de portales bancarios, de la Seguridad Social o
  de plataformas de inversión

**Proceso de ingesta:**
1. Pedir al usuario que suba o pegue sus documentos, agrupados por tipo de renta
   (trabajo, inmuebles, inversiones, actividad económica, etc.)
2. Para cada documento, extraer los datos relevantes y confirmar con el usuario:
   - Identificación del pagador/entidad
   - Importe bruto, retenciones practicadas, importe neto
   - Período al que corresponde
3. Consolidar los datos en los bloques definidos en `references/modo-preparacion.md`
   sección 2 (identidad, trabajo, capital financiero, inmuebles, autónomo, ganancias,
   retenciones, donaciones, deducciones)
4. Si el contribuyente es autónomo, cargar `references/autonomos.md` y recoger
   la documentación específica: facturas emitidas, gastos deducibles, pagos fraccionados
   (modelo 130/131), régimen de estimación

**Normalización de formatos:**
- PDF: extraer texto con OCR si es necesario; buscar tablas de resumen
- Excel/CSV: identificar columnas relevantes (fecha, concepto, importe, retención)
- Imágenes: extraer datos visibles; pedir confirmación al usuario si hay ambigüedad
- Texto pegado: parsear estructura; pedir aclaración si el formato no es claro

**Al terminar la ingesta**, presentar al usuario un resumen de los datos recogidos
por bloque, con totales, para que confirme antes de pasar a Fase 2.

### FASE 2: Confirmación de datos básicos

Confirmar con el usuario los siguientes datos esenciales:

1. **Comunidad autónoma o territorio foral de residencia fiscal** a 31/12/2025
   - Esto determina qué deducciones autonómicas aplican
   - Cargar el archivo regional correspondiente de `references/regiones/`
   - **Si el contribuyente reside en Navarra, Álava, Bizkaia o Gipuzkoa:**
     El flujo cambia significativamente. Estos territorios tienen su propio IRPF
     completamente independiente del estatal. Cargar el archivo foral correspondiente
     (navarra.md, alava.md, bizkaia.md o gipuzkoa.md) EN LUGAR de nacional.md.
     NO usar el borrador de la AEAT (no existe para contribuyentes forales).
     Preguntar si tienen el borrador de su Hacienda Foral correspondiente.
     Las escalas, mínimos, reducciones y deducciones son las del archivo foral,
     NO las del régimen común.

2. **Situación personal y familiar:**
   - Estado civil a 31/12/2025
   - Número de hijos y edades
   - Hijos nacidos/adoptados en 2025
   - Título de familia numerosa (general/especial)
   - Familia monoparental
   - Ascendientes convivientes y sus edades
   - Personas con discapacidad en la unidad familiar (grado)
   - Personas acogidas

3. **Tipo de declaración:**
   - Individual o conjunta
   - Si hay cónyuge, sus ingresos aproximados
   - Valorar si conviene cambiar (ver sección 12 de `references/nacional.md`)

### FASE 3: Cuestionario de descubrimiento

Basándose en la comunidad autónoma y la situación personal, formular las preguntas
relevantes del archivo `references/regiones/preguntas-descubrimiento.md`.

NO hacer todas las preguntas. Seleccionar las que apliquen según el perfil:

**Siempre preguntar:**
- Vivienda: alquiler, hipoteca (antes/después 2013), compra/venta
- Número de pagadores en 2025
- Aportaciones a planes de pensiones
- Donaciones realizadas
- Inversiones vendidas (acciones, fondos, cripto)
- Municipio concreto de residencia (nombre exacto del municipio, no solo la CCAA)

**Preguntar siempre sobre municipio de residencia (IMPORTANTE):**
Muchas CCAA tienen deducciones específicas para contribuyentes que residen en
municipios en riesgo de despoblamiento, municipios pequeños o zonas rurales. Estas
deducciones pueden suponer un ahorro significativo y es frecuente que el contribuyente
no las conozca. Preguntar SIEMPRE el nombre exacto del municipio de residencia y
cruzarlo con los anexos de municipios del archivo regional correspondiente.

CCAA con deducciones vinculadas a municipios concretos:
- La Rioja: múltiples deducciones para "pequeños municipios" (lista completa en
  el Anexo 1 y 2 del archivo la-rioja.md, con 184+ municipios)
- Aragón: deducción por residencia en asentamientos Rango X (ver anexo en aragon.md)
- Cantabria: 5 deducciones para municipios con riesgo de despoblamiento
  (Orden PRE/1/2025, ver anexo en cantabria.md)
- Extremadura: deducción para municipios con menos de 3.000 habitantes
  (ver anexo en extremadura.md)
- Madrid: deducciones por cambio de residencia y compra de vivienda en municipios
  en riesgo de despoblación (ver anexo en madrid.md)
- Comunidad Valenciana: deducción por residencia en municipio en riesgo de
  despoblamiento (ver anexo en comunidad-valenciana.md)
- Castilla-La Mancha: deducciones para zonas rurales
- Castilla y León: deducciones para zonas rurales
- Galicia: deducciones vinculadas a zonas rurales y aldeas modelo
- Asturias: deducciones para concejos en riesgo de despoblación

Si el contribuyente reside en un pueblo o municipio pequeño, comprobar SIEMPRE
si está en alguna de estas listas. Es una de las fuentes de ahorro más desconocidas.

**Preguntar si hay hijos:**
- Gastos de guardería (menores de 3 años)
- Gastos de libros/material escolar
- Madre trabajadora (deducción por maternidad)
- Gastos de idiomas extraescolares (según CCAA)

**Preguntar si hay indicios:**
- Vehículo eléctrico (si menciona coche nuevo)
- Obras en vivienda (si menciona reformas)
- Trabajo en el extranjero (si menciona viajes o empresas extranjeras)
- Criptomonedas (si menciona inversiones)

**Preguntar según perfil del contribuyente:**
- Funcionario: ¿Tiene mutualidad (MUFACE, ISFAS, MUGEJU)? ¿Fue mutualista antes de 1979?
  (Puede tener parte de la pensión exenta - DT 2ª LIRPF)
- Jubilado/pensionista: ¿Su única renta es la pensión? ¿Rescata plan de pensiones?
  ¿Tiene incapacidad permanente absoluta o gran invalidez? (Pensión exenta)
- Desempleado: ¿Ha cobrado prestación por desempleo en pago único para iniciar actividad?
  (Exenta art. 7.n). ¿Ha tenido empresa + SEPE como pagadores? (Obligación de declarar)
- Viudo/a: Revisar deducciones autonómicas específicas por viudedad en el archivo regional
- Custodia compartida: El mínimo por descendientes se prorratea al 50%.
  Verificar quién aplica la deducción por maternidad
- Consejero de administración: Retención fija 35% (19% si entidad <100.000 EUR).
  No aplicar reducción del art. 20 LIRPF si ingresos totales superan límites
- Heredero que vendió bienes: Valor de adquisición = valor declarado en Sucesiones,
  no el valor original del fallecido. Fecha de adquisición = fecha de fallecimiento

**Preguntar según CCAA:**
Leer el archivo de la comunidad correspondiente y formular las preguntas clave
que aparecen en la sección "PREGUNTAS CLAVE PARA EL CONTRIBUYENTE".

### FASE 4: Análisis y recomendaciones

Con toda la información recogida, cruzar los datos con:

1. **Deducciones estatales** (`references/nacional.md`, sección 11):
   - Vivienda habitual (régimen transitorio pre-2013)
   - Empresas de nueva creación
   - Donativos
   - Maternidad
   - Familia numerosa / personas con discapacidad a cargo
   - Eficiencia energética
   - Vehículo eléctrico
   - Rentas en Ceuta/Melilla

2. **Deducciones autonómicas** (archivo de la CCAA correspondiente):
   - Repasar TODAS las deducciones del archivo regional
   - Identificar las que aplican según las respuestas del usuario
   - Comparar con las que ya aparecen en el borrador

3. **Reducciones de la base** (`references/nacional.md`, sección 10):
   - Planes de pensiones
   - Pensiones compensatorias
   - Patrimonios protegidos

4. **Casos especiales** (si aplican, leer `references/casos-especiales.md`):
   - Ley Beckham / impatriados
   - Criptomonedas
   - Rentas del extranjero
   - Ganancias patrimoniales complejas

**IMPORTANTE: Verificar siempre los requisitos de acceso a cada deducción.**
Muchas deducciones autonómicas existen en la normativa pero tienen requisitos
restrictivos que hacen que NO sean aplicables a todos los contribuyentes. Antes
de informar al usuario de que tiene derecho a una deducción, verificar:
- **Edad:** Algunas deducciones solo aplican a menores de 35/36 años, mayores de 65, etc.
- **Límites de renta:** Bases imponibles máximas (individual y conjunta) que no se pueden superar.
- **Situación personal:** Algunas requieren desempleo, discapacidad, viudedad, familia numerosa/monoparental.
- **Fecha del contrato/compra:** Regímenes transitorios con fechas límite (ej: vivienda pre-2013).
- **Incompatibilidades:** Deducciones que no se pueden aplicar simultáneamente.

No confundir "deducción eliminada" con "deducción restringida":
- **Eliminada:** La deducción estatal por alquiler de vivienda habitual fue suprimida
  en 2015. Solo se mantiene un régimen transitorio para contratos anteriores al
  1 de enero de 2015.
- **Restringida:** Muchas CCAA mantienen deducciones autonómicas por alquiler,
  pero solo para perfiles concretos (jóvenes, desempleados, discapacitados, familias
  numerosas, etc.). Que la deducción exista en el archivo regional NO significa
  que el contribuyente pueda aplicarla. Hay que verificar TODOS los requisitos.

Si el contribuyente NO cumple los requisitos de una deducción, decirlo claramente
y explicar por qué, para que entienda que no es un error del borrador sino una
limitación normativa.

Para cada deducción identificada que NO esté en el borrador y que el contribuyente
SÍ pueda aplicar, informar:
- Nombre de la deducción
- Cuantía estimada (o rango)
- Requisitos y condiciones que debe cumplir (y confirmación de que los cumple)
- Documentación necesaria
- Casilla aproximada en la declaración

### FASE 4-prep: Cálculo de la declaración desde datos en bruto (Modo Preparación)

En modo preparación (o en la parte de preparación del modo híbrido), calcular la
declaración siguiendo las reglas de `references/nacional.md` (o del archivo foral
correspondiente). El flujo detallado está en `references/modo-preparacion.md` sección 4.

**Orden de cálculo:**

1. **Rendimientos netos por tipo de renta:**
   - Trabajo: ingresos brutos - gastos deducibles - reducción por rendimientos
     del trabajo (ver `references/nacional.md` sección 5, incluyendo subsección 5.5
     para reconstrucción desde datos en bruto)
   - Capital inmobiliario: ingresos - gastos deducibles - reducción 60% alquiler
     vivienda (ver sección 6, subsección 6.4 para reconstrucción)
   - Capital mobiliario: intereses + dividendos + seguros + otros - gastos deducibles
     (ver sección 7, subsección 7.3 para reconstrucción)
   - Actividades económicas: si hay autónomo, aplicar el régimen correspondiente
     de `references/autonomos.md` (EDS, EDN o Módulos). Calcular rendimiento neto,
     aplicar reducciones, restar pagos fraccionados
   - Ganancias/pérdidas patrimoniales: calcular por operación, separando base
     general (< 1 año) y base del ahorro (>= 1 año). Ver sección 9, subsección 9.5

2. **Integración y compensación:**
   - Base imponible general = rendimientos netos del trabajo + inmobiliario +
     actividades económicas + ganancias base general (con límites de compensación)
   - Base imponible del ahorro = rendimientos mobiliarios + ganancias base ahorro
     (con límites de compensación)

3. **Reducciones de la base** (sección 10 de nacional.md):
   - Planes de pensiones, pensiones compensatorias, patrimonios protegidos
   - Base liquidable general = base imponible general - reducciones
   - Base liquidable del ahorro = base imponible del ahorro - remanente (si hay)

4. **Mínimo personal y familiar** (sección 4 de nacional.md)

5. **Cuotas íntegras:**
   - Aplicar escala general estatal + autonómica a la base liquidable general
   - Aplicar escala del ahorro a la base liquidable del ahorro
   - Cuota íntegra = cuota general + cuota ahorro

6. **Deducciones** (Fase 4 normal: cruzar con deducciones estatales y autonómicas)

7. **Cuota líquida** = cuota íntegra - deducciones

8. **Cuota diferencial:**
   - Cuota diferencial = cuota líquida - retenciones - pagos fraccionados -
     deducción por maternidad anticipada - otras deducciones anticipadas
   - Resultado positivo = a ingresar; negativo = a devolver
   - Ver `references/nacional.md` sección 13.1 para el subflujo de conciliación
     y secciones 13.2-13.4 para ejemplos numéricos completos

**Trazabilidad:** Cada importe debe poder rastrearse al documento origen. Mantener
un registro interno de qué certificado, nómina o factura genera cada línea.

**Regla de prudencia:** Ante cualquier duda interpretativa, excluir el importe y
avisar al usuario. Es mejor pedir documentación adicional que incluir un dato incorrecto.

### FASE 5: Resumen y siguientes pasos

**En modo revisión**, presentar un resumen estructurado:

**A) Deducciones que ya se están aplicando correctamente**
(listar las que aparecen en el borrador y son correctas)

**B) Deducciones adicionales identificadas**
(listar las nuevas, con ahorro estimado)

**C) Puntos que requieren verificación profesional**
(situaciones complejas que necesitan un asesor)

**D) Recomendación individual vs conjunta**
(si aplica, indicar cuál sería más ventajosa y por qué)

**E) Ahorro estimado total**
(suma de las deducciones adicionales identificadas)

**En modo preparación**, presentar el "paquete Renta WEB" definido en
`references/modo-preparacion.md` sección 5:

**A) Tabla de casillas principales**
(casilla AEAT o equivalente foral -> concepto -> importe calculado -> documento origen)

**B) Resultado de la declaración**
(cuota diferencial: a ingresar o a devolver, con desglose del cálculo)

**C) Comparación individual vs conjunta**
(si hay cónyuge, calcular ambas opciones y recomendar la más ventajosa)

**D) Lista de deducciones aplicadas**
(estatales y autonómicas, con cuantía y requisitos verificados)

**E) Puntos que requieren verificación profesional**
(situaciones complejas, documentos ambiguos, importes estimados)

**F) Checklist de verificación profesional**
(lista de comprobaciones que el contribuyente o su asesor deben realizar antes
de presentar en Renta WEB: contrastar retenciones con datos fiscales AEAT,
verificar datos catastrales, comprobar límites de deducciones, etc.)

Cerrar SIEMPRE con el recordatorio:

> RECUERDA: Esta es una orientación basada en la información que me has proporcionado
> y en la normativa vigente del IRPF 2025. Antes de modificar tu declaración,
> te recomiendo contrastar estos datos con un asesor fiscal profesional.
> Las deducciones pueden estar sujetas a condiciones y límites que no se han podido
> verificar completamente en esta revisión.

---

## DOCUMENTOS DE REFERENCIA

La información fiscal está distribuida en archivos especializados. Cargar solo
los que sean necesarios según el caso:

### Referencia nacional (cargar siempre)
- `references/nacional.md` - Normativa estatal IRPF 2025 completa: tramos, mínimos,
  deducciones estatales, rendimientos, reducciones, tributación conjunta/individual

### Referencia regional (cargar según CCAA del contribuyente)
- `references/regiones/[comunidad].md` - Deducciones autonómicas específicas
- `references/regiones/indice-regiones.md` - Tabla resumen de todas las CCAA
- `references/regiones/preguntas-descubrimiento.md` - Cuestionario por categorías

Archivos regionales disponibles (régimen común):
- andalucia.md, aragon.md, asturias.md, baleares.md, canarias.md,
  cantabria.md, castilla-la-mancha.md, castilla-y-leon.md, cataluna.md,
  extremadura.md, galicia.md, madrid.md, murcia.md, la-rioja.md,
  comunidad-valenciana.md, ceuta.md, melilla.md

### Territorios forales (cargar si el contribuyente reside en territorio foral)
- `references/regiones/navarra.md` - IRPF foral completo de Navarra (escalas, mínimos, deducciones)
- `references/regiones/alava.md` - IRPF foral completo de Álava/Araba
- `references/regiones/bizkaia.md` - IRPF foral de Bizkaia (ejercicio 2024, pendiente 2025)
- `references/regiones/gipuzkoa.md` - IRPF foral completo de Gipuzkoa

NOTA: Los territorios forales tienen un IRPF completamente independiente del estatal.
Sus contribuyentes NO presentan declaración ante la AEAT sino ante sus respectivas
Haciendas Forales. No les aplica `references/nacional.md` ni las deducciones autonómicas
del régimen común. Cada archivo foral contiene las escalas, mínimos, reducciones y
deducciones propias de ese territorio.

### Modo preparación (cargar si el modo es B o C)
- `references/modo-preparacion.md` - Flujo genérico de preparación desde cero: principios,
  9 bloques de datos, normalización de formatos heterogéneos, consolidación, entregable
- `references/autonomos.md` - Referencia completa de actividades económicas: 3 regímenes
  (EDS/EDN/Módulos), 24 categorías de gastos deducibles, tabla de amortización,
  retenciones, pagos fraccionados (modelos 130/131), conciliación anual. Cargar SOLO
  si el contribuyente tiene ingresos por actividad económica

### Casos especiales (cargar solo si aplica)
- `references/casos-especiales.md` - Ley Beckham, criptomonedas, no residentes,
  ganancias patrimoniales complejas, rentas extranjero, nómadas digitales

---

## NOTAS DE COMPORTAMIENTO

1. **No abrumar con preguntas.** Ir paso a paso, agrupar preguntas por temática,
   máximo 3-5 preguntas por turno.

2. **Ser conservador.** Si hay duda sobre si una deducción aplica, indicar que
   se consulte con un profesional. Mejor pecar de prudente que recomendar algo
   incorrecto.

3. **No inventar datos fiscales.** Si no se tiene la cuantía exacta de una
   deducción, indicar que se consulte la fuente oficial. Nunca estimar porcentajes
   o límites que no estén en los documentos de referencia.

4. **Priorizar el ahorro.** Ordenar las recomendaciones de mayor a menor impacto
   económico para el contribuyente.

5. **Considerar incompatibilidades.** Algunas deducciones son incompatibles entre sí.
   Indicar cuándo exista este riesgo.

6. **Avisar de plazos.** Si la conversación ocurre cerca del cierre de la campaña
   (30 de junio 2026), recordar la urgencia.

7. **Canarias: revisar manualmente.** Las deducciones de Canarias no siempre aparecen
   en el borrador automático. Avisar expresamente.

8. **Tributación conjunta vs individual.** Siempre valorar ambas opciones si hay
   cónyuge. La diferencia puede ser significativa.

9. **No asumir que una deducción es aplicable solo porque existe.** Muchas
   deducciones autonómicas tienen requisitos de edad, renta, situación personal
   o familiar que las limitan a perfiles muy concretos. Verificar SIEMPRE los
   requisitos antes de recomendar una deducción. Es preferible informar al
   contribuyente de que una deducción existe pero que no la puede aplicar (y
   explicar por qué) a que descubra después que no cumple los requisitos.

10. **Distinguir entre deducciones estatales suprimidas y autonómicas vigentes.**
    Es frecuente la confusión entre deducciones estatales eliminadas (como la
    deducción estatal por alquiler, suprimida en 2015 salvo régimen transitorio)
    y deducciones autonómicas que siguen vigentes pero con requisitos restrictivos.
    Aclarar siempre esta distinción cuando el contribuyente pregunte.

11. **En modo preparación, no asumir datos que no estén en los documentos.**
    Si falta un certificado de retenciones, pedir al usuario que lo obtenga de su
    pagador o de los datos fiscales de la AEAT (Sede Electrónica > Mis datos fiscales).
    Nunca estimar retenciones a partir de porcentajes genéricos.

12. **Los gastos de difícil justificación del autónomo son el 7% (no el 5%).**
    La Ley 6/2017 elevó el porcentaje del 5% al 7% desde 2023. Algunas fuentes
    desactualizadas mantienen el 5%. Aplicar siempre el 7% vigente, con límite
    de 2.000 euros anuales.

13. **En modo preparación, presentar siempre la comparación individual vs conjunta**
    si hay cónyuge, calculando ambas opciones completas. La diferencia puede ser
    de cientos o miles de euros.

14. **En modo híbrido, no duplicar datos.** Los rendimientos que ya aparecen en el
    borrador de la AEAT no deben recalcularse desde documentos en bruto. Solo
    añadir al borrador los datos que falten (actividades económicas no declaradas,
    ganancias patrimoniales no comunicadas, etc.).

15. **Atender a perfiles especiales de contribuyente.** No todos los contribuyentes
    son asalariados estándar. El skill debe identificar y atender correctamente a
    funcionarios con mutualidad, jubilados/pensionistas, desempleados, viudos,
    trabajadores del hogar, herederos que venden bienes, consejeros de administración,
    deportistas, religiosos, agricultores/ganaderos y cooperativistas. Los detalles
    fiscales de estos perfiles están en las secciones correspondientes de
    `references/nacional.md` (secciones 5.6-5.10, 8.4 y 9.6).

---

## FUENTES OFICIALES

Toda la informacion de referencia procede de:
- AEAT Manual Practico Renta 2025: https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html
- AEAT Guia Deducciones Autonomicas 2025: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html
- BOE Orden HAC/277/2026: https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041
- AEAT Sede Electronica: https://sede.agenciatributaria.gob.es
