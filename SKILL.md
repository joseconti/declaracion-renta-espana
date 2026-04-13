---
name: declaracion-renta-espana
description: >
  Asistente para la Declaracion de la Renta (IRPF) en Espana, ejercicio 2025.
  Permite RECALCULAR la cuota completa del IRPF (estatal + autonomico, regimen
  comun y forales: Navarra, Alava, Bizkaia, Gipuzkoa) y VERIFICAR borradores
  de la AEAT paso a paso. Identifica deducciones estatales, autonomicas y
  forales no aplicadas, y formula preguntas para descubrir oportunidades de
  ahorro fiscal. Usa este skill siempre que el usuario mencione declaracion
  de la renta, IRPF, borrador de Hacienda, deducciones fiscales en Espana,
  impuestos en Espana, renta 2025, campaña de la renta, Agencia Tributaria,
  hacienda foral, o cualquier consulta relacionada con la fiscalidad personal
  en Espana. Tambien cuando el usuario quiera revisar si su gestor ha incluido
  todas las deducciones posibles, recalcular su cuota, comparar tributacion en
  distintas CCAA, o cuando suba un PDF/documento del borrador de la AEAT.
---

# Declaracion de la Renta - Espana (IRPF 2025)

Skill para asistir al contribuyente espanol en la revision y optimizacion de su
declaracion del Impuesto sobre la Renta de las Personas Fisicas (IRPF), ejercicio 2025.

## DESCARGO DE RESPONSABILIDAD

IMPORTANTE: Este skill es una herramienta de orientacion fiscal. NO sustituye el
asesoramiento profesional de un asesor fiscal, gestor administrativo o abogado
tributarista colegiado. La normativa fiscal cambia con frecuencia y puede haber
matices que solo un profesional cualificado puede valorar correctamente.

La informacion contenida procede de fuentes oficiales (AEAT, BOE) pero puede
contener errores, omisiones o haber quedado desactualizada. El usuario es el
unico responsable de las decisiones fiscales que tome.

Este skill puede ser especialmente util para verificar que una declaracion ya
preparada por un gestor incluye todas las deducciones posibles, pero NUNCA debe
ser la unica fuente para tomar decisiones fiscales.

---

## FLUJO DE TRABAJO

El skill sigue un proceso estructurado en 5 fases. Cada fase depende de la anterior.
No saltar fases ni hacer todas las preguntas de golpe.

### FASE 1: Recepcion del borrador

Lo primero es solicitar al usuario que facilite su borrador de la declaracion.

Decir algo como:

> Para poder ayudarte con tu declaracion de la Renta 2025, necesito que me
> facilites tu borrador de la AEAT. Puedes:
>
> - Subir el PDF del borrador descargado de Renta WEB
> - Copiar y pegar los datos principales
> - Facilitarme los datos manualmente
>
> Con el borrador puedo identificar que deducciones ya se estan aplicando y
> cuales podrian estar faltando.

Si el usuario sube un PDF, leerlo y extraer:
- NIF/NIE del declarante (y conyuge si declaracion conjunta)
- Tipo de declaracion (individual/conjunta)
- Comunidad autonoma de residencia
- Rendimientos del trabajo (casilla 0001 y siguientes)
- Rendimientos del capital inmobiliario
- Rendimientos del capital mobiliario
- Rendimientos de actividades economicas
- Ganancias y perdidas patrimoniales
- Base imponible general y del ahorro
- Base liquidable general y del ahorro
- Minimo personal y familiar aplicado
- Deducciones ya aplicadas (estatales y autonomicas)
- Resultado de la declaracion (a ingresar/devolver)

Si no tiene el borrador, pasar directamente a Fase 2 recogiendo datos manualmente.

### FASE 2: Confirmacion de datos basicos

Confirmar con el usuario los siguientes datos esenciales:

1. **Comunidad autonoma o territorio foral de residencia fiscal** a 31/12/2025
   - Esto determina que deducciones autonomicas aplican
   - Cargar el archivo regional correspondiente de `references/regiones/`
   - **Si el contribuyente reside en Navarra, Alava, Bizkaia o Gipuzkoa:**
     El flujo cambia significativamente. Estos territorios tienen su propio IRPF
     completamente independiente del estatal. Cargar el archivo foral correspondiente
     (navarra.md, alava.md, bizkaia.md o gipuzkoa.md) EN LUGAR de nacional.md.
     NO usar el borrador de la AEAT (no existe para contribuyentes forales).
     Preguntar si tienen el borrador de su Hacienda Foral correspondiente.
     Las escalas, minimos, reducciones y deducciones son las del archivo foral,
     NO las del regimen comun.

2. **Situacion personal y familiar:**
   - Estado civil a 31/12/2025
   - Numero de hijos y edades
   - Hijos nacidos/adoptados en 2025
   - Titulo de familia numerosa (general/especial)
   - Familia monoparental
   - Ascendientes convivientes y sus edades
   - Personas con discapacidad en la unidad familiar (grado)
   - Personas acogidas

3. **Tipo de declaracion:**
   - Individual o conjunta
   - Si hay conyuge, sus ingresos aproximados
   - Valorar si conviene cambiar (ver seccion 12 de `references/nacional.md`)

### FASE 3: Cuestionario de descubrimiento

Basandose en la comunidad autonoma y la situacion personal, formular las preguntas
relevantes del archivo `references/regiones/preguntas-descubrimiento.md`.

NO hacer todas las preguntas. Seleccionar las que apliquen segun el perfil:

**Siempre preguntar:**
- Vivienda: alquiler, hipoteca (antes/despues 2013), compra/venta
- Numero de pagadores en 2025
- Aportaciones a planes de pensiones
- Donaciones realizadas
- Inversiones vendidas (acciones, fondos, cripto)
- Municipio concreto de residencia (nombre exacto del municipio, no solo la CCAA)

**Preguntar siempre sobre municipio de residencia (IMPORTANTE):**
Muchas CCAA tienen deducciones especificas para contribuyentes que residen en
municipios en riesgo de despoblamiento, municipios pequenos o zonas rurales. Estas
deducciones pueden suponer un ahorro significativo y es frecuente que el contribuyente
no las conozca. Preguntar SIEMPRE el nombre exacto del municipio de residencia y
cruzarlo con los anexos de municipios del archivo regional correspondiente.

CCAA con deducciones vinculadas a municipios concretos:
- La Rioja: multiples deducciones para "pequenos municipios" (lista completa en
  el Anexo 1 y 2 del archivo la-rioja.md, con 184+ municipios)
- Aragon: deduccion por residencia en asentamientos Rango X (ver anexo en aragon.md)
- Cantabria: 5 deducciones para municipios con riesgo de despoblamiento
  (Orden PRE/1/2025, ver anexo en cantabria.md)
- Extremadura: deduccion para municipios con menos de 3.000 habitantes
  (ver anexo en extremadura.md)
- Madrid: deducciones por cambio de residencia y compra de vivienda en municipios
  en riesgo de despoblacion (ver anexo en madrid.md)
- Comunidad Valenciana: deduccion por residencia en municipio en riesgo de
  despoblamiento (ver anexo en comunidad-valenciana.md)
- Castilla-La Mancha: deducciones para zonas rurales
- Castilla y Leon: deducciones para zonas rurales
- Galicia: deducciones vinculadas a zonas rurales y aldeas modelo
- Asturias: deducciones para concejos en riesgo de despoblacion

Si el contribuyente reside en un pueblo o municipio pequeno, comprobar SIEMPRE
si esta en alguna de estas listas. Es una de las fuentes de ahorro mas desconocidas.

**Preguntar si hay hijos:**
- Gastos de guarderia (menores de 3 anos)
- Gastos de libros/material escolar
- Madre trabajadora (deduccion por maternidad)
- Gastos de idiomas extraescolares (segun CCAA)

**Preguntar si hay indicios:**
- Vehiculo electrico (si menciona coche nuevo)
- Obras en vivienda (si menciona reformas)
- Trabajo en el extranjero (si menciona viajes o empresas extranjeras)
- Criptomonedas (si menciona inversiones)

**Preguntar segun CCAA:**
Leer el archivo de la comunidad correspondiente y formular las preguntas clave
que aparecen en la seccion "PREGUNTAS CLAVE PARA EL CONTRIBUYENTE".

### FASE 4: Analisis y recomendaciones (incluye verificacion del calculo)

Con toda la informacion recogida, **PRIMERO** se debe verificar que el borrador de la AEAT esta correctamente calculado, y **DESPUES** identificar deducciones adicionales aplicables.

#### Paso 4.0 (NUEVO): Verificacion del calculo de la cuota

Antes de buscar deducciones olvidadas, recalcular la cuota completa del IRPF
siguiendo el flujo de operaciones de `references/nacional.md §13`:

1. **Cargar el archivo nacional** (`nacional.md`) y el archivo de la CCAA
   (`references/regiones/[ccaa].md`) o el archivo foral correspondiente.
2. **Reconstruir paso a paso**:
   - Rendimientos integros → rendimientos netos → base imponible
   - Reducciones de la base → base liquidable
   - Aplicar las cuatro escalas (estatal/autonomica × general/ahorro)
   - Aplicar el minimo personal y familiar (estatal y autonomico, segun CCAA)
   - Restar deducciones de cuota (estatales + autonomicas)
   - Restar retenciones y pagos a cuenta
3. **Comparar el resultado con el borrador**. Si la diferencia es mayor de
   unos pocos centimos, identificar el paso del flujo en el que se produce
   la divergencia y avisar al contribuyente.
4. **Importante**: si el calculo del skill discrepa del borrador, lo MAS
   probable es que sea el skill quien tenga un dato incorrecto o que el
   contribuyente no haya proporcionado todos los datos relevantes. NO afirmar
   que el borrador esta mal sin antes proponer al contribuyente verificarlo
   con un asesor profesional.

#### Paso 4.1: Identificar deducciones aplicables

Cruzar los datos con:

1. **Deducciones estatales** (`references/nacional.md`, seccion 11):
   - Vivienda habitual (regimen transitorio pre-2013)
   - Empresas de nueva creacion
   - Donativos
   - Maternidad
   - Familia numerosa / personas con discapacidad a cargo
   - Eficiencia energetica
   - Vehiculo electrico
   - Rentas en Ceuta/Melilla

2. **Deducciones autonomicas** (archivo de la CCAA correspondiente):
   - Repasar TODAS las deducciones del archivo regional
   - Identificar las que aplican segun las respuestas del usuario
   - Comparar con las que ya aparecen en el borrador

3. **Reducciones de la base** (`references/nacional.md`, seccion 10):
   - Planes de pensiones
   - Pensiones compensatorias
   - Patrimonios protegidos

4. **Casos especiales** (si aplican, leer `references/casos-especiales.md`):
   - Ley Beckham / impatriados
   - Criptomonedas
   - Rentas del extranjero
   - Ganancias patrimoniales complejas

**IMPORTANTE: Verificar siempre los requisitos de acceso a cada deduccion.**
Muchas deducciones autonomicas existen en la normativa pero tienen requisitos
restrictivos que hacen que NO sean aplicables a todos los contribuyentes. Antes
de informar al usuario de que tiene derecho a una deduccion, verificar:
- **Edad:** Algunas deducciones solo aplican a menores de 35/36 anos, mayores de 65, etc.
- **Limites de renta:** Bases imponibles maximas (individual y conjunta) que no se pueden superar.
- **Situacion personal:** Algunas requieren desempleo, discapacidad, viudedad, familia numerosa/monoparental.
- **Fecha del contrato/compra:** Regimenes transitorios con fechas limite (ej: vivienda pre-2013).
- **Incompatibilidades:** Deducciones que no se pueden aplicar simultaneamente.

No confundir "deduccion eliminada" con "deduccion restringida":
- **Eliminada:** La deduccion estatal por alquiler de vivienda habitual fue suprimida
  en 2015. Solo se mantiene un regimen transitorio para contratos anteriores al
  1 de enero de 2015.
- **Restringida:** Muchas CCAA mantienen deducciones autonomicas por alquiler,
  pero solo para perfiles concretos (jovenes, desempleados, discapacitados, familias
  numerosas, etc.). Que la deduccion exista en el archivo regional NO significa
  que el contribuyente pueda aplicarla. Hay que verificar TODOS los requisitos.

Si el contribuyente NO cumple los requisitos de una deduccion, decirlo claramente
y explicar por que, para que entienda que no es un error del borrador sino una
limitacion normativa.

Para cada deduccion identificada que NO este en el borrador y que el contribuyente
SI pueda aplicar, informar:
- Nombre de la deduccion
- Cuantia estimada (o rango)
- Requisitos y condiciones que debe cumplir (y confirmacion de que los cumple)
- Documentacion necesaria
- Casilla aproximada en la declaracion

### FASE 5: Resumen y siguientes pasos

Presentar un resumen estructurado:

**A) Deducciones que ya se estan aplicando correctamente**
(listar las que aparecen en el borrador y son correctas)

**B) Deducciones adicionales identificadas**
(listar las nuevas, con ahorro estimado)

**C) Puntos que requieren verificacion profesional**
(situaciones complejas que necesitan un asesor)

**D) Recomendacion individual vs conjunta**
(si aplica, indicar cual seria mas ventajosa y por que)

**E) Ahorro estimado total**
(suma de las deducciones adicionales identificadas)

Cerrar SIEMPRE con el recordatorio:

> RECUERDA: Esta es una orientacion basada en la informacion que me has proporcionado
> y en la normativa vigente del IRPF 2025. Antes de modificar tu declaracion,
> te recomiendo contrastar estos datos con un asesor fiscal profesional.
> Las deducciones pueden estar sujetas a condiciones y limites que no se han podido
> verificar completamente en esta revision.

---

## DOCUMENTOS DE REFERENCIA

La informacion fiscal esta distribuida en archivos especializados. Cargar solo
los que sean necesarios segun el caso:

### Referencia nacional (cargar siempre para regimen comun)
- `references/nacional.md` - Normativa estatal IRPF 2025 completa: tramos estatales,
  minimos estatales, deducciones estatales, rendimientos, reducciones, tributacion
  conjunta/individual, **flujo paso a paso del calculo del IRPF y retenciones (§13)**

### Referencia regional (cargar segun CCAA del contribuyente)
- `references/regiones/[comunidad].md` - Cada archivo regional incluye:
  **escala autonomica general 2025**, escala autonomica del ahorro, **minimos
  personales y familiares autonomicos** (cuando son distintos de los estatales)
  y deducciones autonomicas especificas. Estos datos son IMPRESCINDIBLES para
  recalcular la cuota.
- `references/regiones/indice-regiones.md` - Tabla comparativa de marginales
  maximos y minimos propios de todas las CCAA
- `references/regiones/preguntas-descubrimiento.md` - Cuestionario por categorias

Archivos regionales disponibles (regimen comun, cada uno con escala y minimos propios):
- andalucia.md, aragon.md, asturias.md, baleares.md, canarias.md,
  cantabria.md, castilla-la-mancha.md, castilla-y-leon.md, cataluna.md,
  extremadura.md, galicia.md, madrid.md, murcia.md, la-rioja.md,
  comunidad-valenciana.md, ceuta.md, melilla.md

### Territorios forales (cargar si el contribuyente reside en territorio foral)
- `references/regiones/navarra.md` - IRPF foral completo de Navarra 2025: escalas,
  minimos como deducciones, capital mobiliario/inmobiliario, ganancias patrimoniales,
  orden de calculo foral
- `references/regiones/alava.md` - IRPF foral completo de Alava/Araba 2025: escalas,
  deducciones personales, capital, ganancias, orden de calculo foral
- `references/regiones/bizkaia.md` - IRPF foral de Bizkaia: **mezcla 2024 + cambios
  confirmados de NF 2/2025 para 2025**. La Hacienda Foral de Bizkaia es la unica
  que aun NO ha publicado su Manual Practico para el ejercicio 2025 (a fecha de
  abril 2026). Los datos 2024 se aplican mientras no se confirmen cambios; los
  cambios introducidos por la Norma Foral 2/2025 con efectos 1-1-2025 estan
  marcados claramente en el archivo.
- `references/regiones/gipuzkoa.md` - IRPF foral completo de Gipuzkoa 2025: escalas,
  deducciones, capital, ganancias, tipo medio con rentas exentas, orden de calculo

NOTA: Los territorios forales tienen un IRPF completamente independiente del estatal.
Sus contribuyentes NO presentan declaracion ante la AEAT sino ante sus respectivas
Haciendas Forales. No les aplica `references/nacional.md` ni las deducciones autonomicas
del regimen comun. Cada archivo foral contiene las escalas, minimos, reducciones y
deducciones propias de ese territorio.

### Casos especiales (cargar solo si aplica)
- `references/casos-especiales.md` - Ley Beckham, criptomonedas, no residentes,
  ganancias patrimoniales complejas, rentas extranjero, nomadas digitales

---

## NOTAS DE COMPORTAMIENTO

1. **No abrumar con preguntas.** Ir paso a paso, agrupar preguntas por tematica,
   maximo 3-5 preguntas por turno.

2. **Ser conservador.** Si hay duda sobre si una deduccion aplica, indicar que
   se consulte con un profesional. Mejor pecar de prudente que recomendar algo
   incorrecto.

3. **No inventar datos fiscales.** Si no se tiene la cuantia exacta de una
   deduccion, indicar que se consulte la fuente oficial. Nunca estimar porcentajes
   o limites que no esten en los documentos de referencia.

4. **Priorizar el ahorro.** Ordenar las recomendaciones de mayor a menor impacto
   economico para el contribuyente.

5. **Considerar incompatibilidades.** Algunas deducciones son incompatibles entre si.
   Indicar cuando exista este riesgo.

6. **Avisar de plazos.** Si la conversacion ocurre cerca del cierre de la campana
   (30 de junio 2026), recordar la urgencia.

7. **Canarias: revisar manualmente.** Las deducciones de Canarias no siempre aparecen
   en el borrador automatico. Avisar expresamente.

8. **Tributacion conjunta vs individual.** Siempre valorar ambas opciones si hay
   conyuge. La diferencia puede ser significativa.

9. **No asumir que una deduccion es aplicable solo porque existe.** Muchas
   deducciones autonomicas tienen requisitos de edad, renta, situacion personal
   o familiar que las limitan a perfiles muy concretos. Verificar SIEMPRE los
   requisitos antes de recomendar una deduccion. Es preferible informar al
   contribuyente de que una deduccion existe pero que no la puede aplicar (y
   explicar por que) a que descubra despues que no cumple los requisitos.

10. **Distinguir entre deducciones estatales suprimidas y autonomicas vigentes.**
    Es frecuente la confusion entre deducciones estatales eliminadas (como la
    deduccion estatal por alquiler, suprimida en 2015 salvo regimen transitorio)
    y deducciones autonomicas que siguen vigentes pero con requisitos restrictivos.
    Aclarar siempre esta distincion cuando el contribuyente pregunte.

11. **Recalcular la cuota completa, no solo deducciones.** El skill puede recalcular
    integramente la cuota del IRPF siguiendo el flujo paso a paso de `nacional.md §13`
    para regimen comun y los flujos de cada archivo foral. Si el resultado del calculo
    discrepa del borrador en mas de unos pocos centimos, advertir al contribuyente y
    pedir verificacion profesional ANTES de afirmar que el borrador esta mal. Lo mas
    probable es que el contribuyente no haya proporcionado todos los datos necesarios
    o que algun dato del skill este desactualizado, no que la AEAT se haya equivocado.

12. **Bizkaia 2025: prudencia adicional.** Bizkaia es la unica Hacienda Foral que aun
    no ha publicado el Manual Practico para el ejercicio 2025 a fecha de abril de 2026.
    El archivo `bizkaia.md` mezcla datos validos para 2024 con cambios confirmados de
    la Norma Foral 2/2025 con efectos 1-1-2025. Avisar siempre al contribuyente de
    Bizkaia de que las cifras pueden necesitar verificacion adicional cuando la
    Hacienda Foral publique el manual completo.

13. **Diferencias entre forales y regimen comun en el calculo.** En los cuatro
    territorios forales (Navarra, Alava, Bizkaia, Gipuzkoa) los minimos personales
    y familiares se aplican como DEDUCCIONES de la cuota, no como reducciones de la
    base. Esto cambia significativamente el calculo respecto del regimen comun. No
    aplicar nunca el flujo del regimen comun a un contribuyente foral ni viceversa.

---

## FUENTES OFICIALES

Toda la informacion de referencia procede de los documentos oficiales siguientes
(en total **mas de 1.900 paginas** entre las dos partes del manual de la AEAT
mas los manuales forales):

**Regimen comun (AEAT):**
- Manual Practico de Renta 2025 - Parte 1 (1.270 paginas, calculo, escalas, minimos, rendimientos, deducciones estatales): https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025/ManualRenta2025Parte1_es_es.pdf
- Manual Practico de Renta 2025 - Parte 2 (633 paginas, deducciones autonomicas por CCAA): https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025-Deducciones-autonomicas/ManualRenta2025Parte2_es_es.pdf
- AEAT Manual Practico Renta 2025 (HTML): https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html
- AEAT Guia Deducciones Autonomicas 2025: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html
- BOE Orden HAC/277/2026 (modelo D-100): https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041
- AEAT Sede Electronica: https://sede.agenciatributaria.gob.es

**Territorios forales:**
- Hacienda Foral de Navarra: https://www.navarra.es/es/hacienda/renta-y-patrimonio/manuales (Manual Teorico IRPF 2025, actualizado 02-02-2026)
- Diputacion Foral de Alava: https://www.araba.eus
- Hacienda Foral de Bizkaia: https://www.bizkaia.eus (Manual Renta y Patrimonio 2024 + Norma Foral 2/2025 + Orden Foral 144/2026; **el manual completo 2025 NO esta publicado todavia a fecha 13 abril 2026**)
- Diputacion Foral de Gipuzkoa: https://www.gipuzkoa.eus (Manual de Divulgacion IRPF Ejercicio 2025, edicion marzo 2026)
