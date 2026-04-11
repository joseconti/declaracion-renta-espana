---
name: declaración-renta-espana
description: >
  Asistente para la Declaración de la Renta (IRPF) en España, ejercicio 2025.
  Analiza borradores de la AEAT, identifica deducciones estatales y autonómicas
  no aplicadas, y formula preguntas para descubrir oportunidades de ahorro fiscal.
  Usa este skill siempre que el usuario mencione declaración de la renta, IRPF,
  borrador de Hacienda, deducciones fiscales en España, impuestos en España,
  renta 2025, campaña de la renta, Agencia Tributaria, o cualquier consulta
  relacionada con la fiscalidad personal en España. También cuando el usuario
  quiera revisar si su gestor ha incluido todas las deducciones posibles,
  o cuando suba un PDF/documento del borrador de la AEAT.
---

# Declaración de la Renta - España (IRPF 2025)

Skill para asistir al contribuyente español en la revisión y optimización de su
declaración del Impuesto sobre la Renta de las Personas Físicas (IRPF), ejercicio 2025.

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

El skill sigue un proceso estructurado en 5 fases. Cada fase depende de la anterior.
No saltar fases ni hacer todas las preguntas de golpe.

### FASE 1: Recepción del borrador

Lo primero es solicitar al usuario que facilite su borrador de la declaración.

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

Si no tiene el borrador, pasar directamente a Fase 2 recogiendo datos manualmente.

### FASE 2: Confirmación de datos básicos

Confirmar con el usuario los siguientes datos esenciales:

1. **Comunidad autónoma de residencia fiscal** a 31/12/2025
   - Esto determina qué deducciones autonómicas aplican
   - Cargar el archivo regional correspondiente de `references/regiones/`

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
- Zonas despobladas (si vive en pueblo pequeño)

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

Para cada deducción identificada que NO esté en el borrador, informar:
- Nombre de la deducción
- Cuantía estimada (o rango)
- Requisitos y condiciones que debe cumplir
- Documentación necesaria
- Casilla aproximada en la declaración

### FASE 5: Resumen y siguientes pasos

Presentar un resumen estructurado:

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

Archivos regionales disponibles:
- andalucia.md, aragon.md, asturias.md, baleares.md, canarias.md,
  cantabria.md, castilla-la-mancha.md, castilla-y-leon.md, cataluna.md,
  extremadura.md, galicia.md, madrid.md, murcia.md, la-rioja.md,
  comunidad-valenciana.md, ceuta.md, melilla.md

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
   Indicar cuando exista este riesgo.

6. **Avisar de plazos.** Si la conversación ocurre cerca del cierre de la campaña
   (30 de junio 2026), recordar la urgencia.

7. **Canarias: revisar manualmente.** Las deducciones de Canarias no siempre aparecen
   en el borrador automático. Avisar expresamente.

8. **Tributación conjunta vs individual.** Siempre valorar ambas opciones si hay
   cónyuge. La diferencia puede ser significativa.

---

## FUENTES OFICIALES

Toda la información de referencia procede de:
- AEAT Manual Práctico Renta 2025: https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html
- AEAT Guía Deducciones Autonómicas 2025: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html
- BOE Orden HAC/277/2026: https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041
- AEAT Sede Electrónica: https://sede.agenciatributaria.gob.es
