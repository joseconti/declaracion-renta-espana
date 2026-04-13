# Changelog

Todas las versiones notables de este skill se documentan en este archivo.

---

## v2025-4 -- Modo preparación, autónomos y ejemplos numéricos

**Fecha:** 13 de abril de 2026

### Modo preparación: nuevo flujo de trabajo

El skill ahora soporta tres modos de trabajo:

- **Modo A - Revisión:** El contribuyente tiene borrador y quiere revisarlo (flujo original).
- **Modo B - Preparación:** El contribuyente NO tiene borrador y quiere calcular su declaración desde cero a partir de documentación en bruto (nóminas, certificados bancarios, facturas, etc.).
- **Modo C - Híbrido:** El contribuyente tiene borrador pero le faltan datos (ingresos de autónomo, ventas no comunicadas, etc.).

### Nuevos archivos

- `references/autonomos.md` (556 líneas) -- Referencia completa de actividades económicas para autónomos y profesionales. 3 regímenes (EDS hasta 600.000 EUR, EDN, Módulos hasta 250.000 EUR), catálogo de 24 categorías de gastos deducibles con criterios y límites, tabla simplificada de amortización (12 grupos), gastos de difícil justificación (7%, hasta 2.000 EUR), retenciones por tipo de actividad (10 tipos, del 1% al 19%), pagos fraccionados trimestrales (modelos 130 y 131), conciliación anual con cuota diferencial, 18 preguntas clave para el contribuyente autónomo.

- `references/modo-preparacion.md` (309 líneas) -- Flujo genérico de preparación desde cero para cualquier tipo de contribuyente. Principios (trazabilidad, prudencia, responsabilidad), 9 bloques de datos a recoger (identidad, trabajo, capital financiero, inmuebles, autónomo, ganancias, retenciones, donaciones, deducciones), normalización de documentos heterogéneos (PDF, Excel, CSV, imágenes, texto pegado), consolidación, entregable final ("paquete Renta WEB") con tabla de casillas principales y checklist de verificación profesional.

### Expansión de archivos existentes

- `references/nacional.md` -- Expandido de 632 a 909 líneas (+277 líneas, +44%). Nuevas subsecciones de reconstrucción de datos en bruto: sección 5.5 (rendimientos del trabajo desde nóminas), sección 6.4 (rendimientos inmobiliarios desde escrituras y contratos), sección 7.3 (rendimientos financieros desde certificados bancarios), sección 9.5 (ganancias patrimoniales desde documentos de compraventa). Sección 8 reducida a resumen con puntero a autonomos.md. Nueva sección 13.1 (subflujo de conciliación retenciones + pagos fraccionados). 3 ejemplos numéricos completos de liquidación: sección 13.2 (asalariado con 35.000 EUR -> devolución 2.343,54 EUR), sección 13.3 (autónomo profesional con 40.000 EUR facturados -> devolución 4.217,24 EUR), sección 13.4 (arrendador con salario 28.000 EUR + alquiler 12.000 EUR -> devolución 1.977,28 EUR).

- `SKILL.md` -- Nuevas fases: Fase 0 (selección de modo: Revisión/Preparación/Híbrido), Fase 1-B (ingesta de documentación heterogénea), Fase 4-prep (cálculo de la declaración desde datos en bruto con 8 pasos), Fase 5 ampliada con entregable de modo preparación ("paquete Renta WEB"). Nuevos documentos de referencia (autonomos.md, modo-preparacion.md). 4 nuevas notas de comportamiento (11-14): no asumir datos ausentes, gastos difícil justificación 7% no 5%, comparación individual/conjunta obligatoria en preparación, no duplicar datos en modo híbrido.

- `references/regiones/preguntas-descubrimiento.md` -- 2 nuevos bloques de preguntas: "Fuentes de datos en bruto" (13 preguntas, para modo preparación) y "Actividades económicas / Autónomos" (16 preguntas). Total: de 56 a 85 preguntas en 8 categorías. Instrucciones de uso actualizadas para ambos modos.

- `README.md` -- Descripción actualizada con los 3 modos de trabajo (revisión, preparación, híbrido). Sección "Qué es este skill" reescrita con los 3 flujos. Árbol de archivos ampliado con autonomos.md y modo-preparacion.md. Nuevos ejemplos de uso para modo preparación. "Qué contiene" ampliado con párrafos de autónomos y modo preparación. Cifras actualizadas (85 preguntas, 24 categorías gastos, 3 ejemplos numéricos). Limitaciones revisadas: eliminada "no calcula el impuesto", añadidas notas sobre cálculos orientativos y Renta WEB.

### Corrección ortográfica global

Revisión completa de ortografía en todos los archivos del skill: tildes, eñes, signos de interrogación y exclamación de apertura. Los archivos de referencia (autonomos.md, modo-preparacion.md, nacional.md expandido) se han creado ya con ortografía correcta. Los archivos preexistentes (SKILL.md, README.md, CHANGELOG.md, preguntas-descubrimiento.md, indice-regiones.md, 15 archivos CCAA + 2 ciudades autónomas + 4 forales) se han revisado sistemáticamente.

### Cifras de esta versión

- 2 archivos nuevos (autonomos.md 556 líneas, modo-preparacion.md 309 líneas)
- nacional.md expandido un 44% (de 632 a 909 líneas)
- SKILL.md expandido con 4 fases nuevas y 4 notas de comportamiento
- preguntas-descubrimiento.md ampliado de 56 a 85 preguntas (+29)
- 3 ejemplos numéricos completos de liquidación
- 24 categorías de gastos deducibles para autónomos documentadas
- Total acumulado: 3.214+ páginas de documentación oficial, 25 archivos de referencia, cobertura del 100% del territorio español, 2 modos de trabajo completos

---

## v2025-3 -- Territorios forales y auditoría completa de requisitos

**Fecha:** 12 de abril de 2026

### Territorios forales: nuevos archivos

- `references/regiones/navarra.md` -- IRPF foral 2025 completo de la Comunidad Foral de Navarra. Escala general de 11 tramos (13%-52%), escala del ahorro de 6 tramos (20%-28%), mínimos personales y familiares, deducciones de cuota (alquiler 15%, donaciones 25-75%, energías renovables 15%, vehículos eléctricos), obligación de declarar, plazos. Fuente: Manual Práctico IRPF 2025 de Hacienda Foral de Navarra (308 páginas).

- `references/regiones/alava.md` -- IRPF foral 2025 completo de Álava/Araba. Escala general de 7 tramos (23%-49%), escala del ahorro de 5 tramos (20%-25%), deducciones por descendientes (668-2.151 EUR), ascendientes (385 EUR), discapacidad (932-1.992 EUR), vivienda (alquiler 20%/35%, compra 23%/25%), EPSV, actividad económica, bonificación del 15% en municipios pequeños. Fuente: Manual Práctico IRPF 2025 de la Diputación Foral de Álava (243 páginas).

- `references/regiones/gipuzkoa.md` -- IRPF foral 2025 completo de Gipuzkoa. Escala general de 8 tramos (23%-49%), reducción por rendimientos del trabajo de 8.000 EUR, deducción por actividades económicas del 23%, vivienda (alquiler hasta 1.955 EUR), donaciones, plazos (7 abril - 2 julio 2026). Fuente: Manual Práctico IRPF 2025 de la Diputación Foral de Gipuzkoa (214 páginas).

- `references/regiones/bizkaia.md` -- IRPF foral de Bizkaia. Escala general de 8 tramos (23%-49%), bonificaciones por rendimientos del trabajo, descendientes 668-2.151 EUR, alquiler 20-30%. Basado en el manual del ejercicio 2024 (546 páginas) porque el manual 2025 no estaba publicado al cierre de esta versión.

### Auditoría completa de requisitos

Se ha detectado que muchas deducciones autonómicas tenían requisitos incompletos (faltaban límites de renta, condiciones de edad, requisitos de situación personal, porcentajes o cuantías sin especificar). Se ha realizado una auditoría sistemática de TODOS los archivos del skill, verificando cada deducción contra las fuentes oficiales (Manual AEAT de 1.903 páginas y webs de haciendas forales/autonómicas).

**Corrección crítica:** La deducción por alquiler de vivienda habitual en Cataluña (deducción 3 de cataluna.md) estaba documentada sin los requisitos restrictivos de acceso. Solo pueden aplicarla contribuyentes menores de 35 años, desempleados 183+ días, con discapacidad >= 65%, viudos >= 65 años, o familias numerosas/monoparentales, y con base imponible inferior a 30.000 EUR (individual) o 45.000 EUR (conjunta). Este mismo patrón de requisitos incompletos se encontró en otras CCAA.

**Archivos del régimen común corregidos (15 CCAA):**

- `cataluna.md` -- Deducción 3 (alquiler): añadidos requisitos de edad, desempleo, discapacidad, viudedad, familia numerosa y límites de renta. Deducciones 6, 7, 8 (donaciones): añadidos porcentajes (15%). Deducción 9 (ángel inversor): añadidos requisitos de empresa (1M facturación, 1 trabajador, mantenimiento 3 años).
- `asturias.md` -- 8 deducciones nuevas de 2025 completadas con cuantías y requisitos (autónomos despoblamiento 1.000 EUR, formación trabajos cualificados 2.000 EUR, traslado domicilio fiscal 15%, emancipación jóvenes, gastos vitales jóvenes < 35, gastos arrendamiento vivienda 500 EUR, ELA).
- `canarias.md` -- Deducción 19 (alquiler): corregido porcentaje de 15-20% a 24%, límite de 740/760 EUR según edad.
- `extremadura.md` -- Deducción 8 (arrendamiento vivienda): añadidos requisitos restrictivos (edad, familia numerosa, discapacidad 65%), límites de renta (28.000/45.000 EUR), requisitos patrimoniales.
- `castilla-la-mancha.md` -- Deducciones 17, 18, 19 (donaciones): añadido porcentaje (15%). Deducción 6 (discapacidad): añadido límite base imponible. Deducción 12 (alquiler jóvenes): añadidos límites de renta.
- `castilla-y-leon.md` -- Deducción 4 (adopción): añadidas cuantías (784 EUR nacional, 3.625 EUR internacional). Deducción 17 (vivienda nueva construcción): añadido porcentaje (7,5%), base máxima (9.040 EUR).
- `cantabria.md` -- 3 deducciones completadas (traslado estudios 200 EUR, gastos educación, ayuda doméstica 20%/300 EUR).
- `murcia.md` -- 10 deducciones completadas con cuantías (material escolar 120 EUR, mujeres trabajadoras 300-400 EUR, idiomas 15%/300 EUR, Internet 30%/300 EUR, cristales 30%/150 EUR, deporte 30%/100 EUR, enfermedades raras 100%).
- `madrid.md` -- 5 deducciones completadas (inversión nueva creación 40-50%/9.279-12.372 EUR, arrendamiento viviendas vacías 1.000 EUR, cambio residencia despoblación 1.000 EUR, otras verificadas como estatales no autonómicas).
- `galicia.md` -- 3 deducciones completadas (nuevas tecnologías hogares 30%/100 EUR, inversión acciones MAB 15%/4.000 EUR, empresas en crecimiento 15-45%/4.000-35.000 EUR). Deducción aldeas modelo (15%). Arrendamiento viviendas vacías (500 EUR/inmueble).
- `comunidad-valenciana.md` -- Deducción donaciones ecológicas actualizada (20% primeros 250 EUR, 25% resto).
- `andalucia.md`, `aragon.md`, `baleares.md`, `la-rioja.md` -- Verificadas correctas; correcciones menores en cuantías de vehículos eléctricos (La Rioja: 15%/3.000 EUR).

**Archivo estatal corregido:**

- `references/nacional.md` -- Expandido de 486 a 632 lineas (+30%). 11 secciones completadas: formulas de reduccion por trabajo con ejemplo de calculo, rentas exentas ampliadas a 12 tipos, gastos deducibles inmobiliarios (10 tipos), modulos con limites, deducciones estatales (vivienda transitoria 15%/9.040 EUR/1.356 EUR, donativos con 4 tipos de entidades, maternidad 1.200 EUR + 1.000 EUR custodia, familia numerosa/discapacidad con 8 tipos, eficiencia energetica con 5 tipos de mejora, vehiculos electricos con 4 tipos).

**Archivo de casos especiales corregido:**

- `references/casos-especiales.md` -- Escala del ahorro de la Ley Beckham corregida: tipo maximo actualizado de 28% a 30% (novedad 2025).

**Archivos forales auditados y completados:**

- `navarra.md` -- Formula de reduccion por rendimientos del trabajo (1.400 EUR, con formula progresiva), umbrales de obligacion de declarar (14.500 EUR sube a 17.000 EUR en 2026), plazos concretos (9 abril - 25 junio 2026), umbral de patrimonio (1.000.000 EUR).
- `alava.md` -- SMI actualizado de 2024 a 2025 (16.576 EUR) en todas las secciones, vivienda completada (alquiler 20%/35%, limites 1.600/2.800 EUR, base <= 68.000 EUR; compra 23-25%, limites 1.955/2.346 EUR), 9 secciones de deducciones economicas (I+D 35%/20%, energias renovables 15%/3.000 EUR, cultura, edicion libros), plazos (7 abril - 25 junio 2026). Anadida Norma Foral 3/2025.
- `bizkaia.md` -- 45+ datos completados: discapacidad con importes por grado, vivienda (intereses hipotecarios 15%/1.200 EUR, gastos notariales 1.500 EUR), planes de pensiones (5.000-6.000 EUR), donativos (20%/1.000 EUR), mecenazgo (25%/1.200 EUR), PYMES (20%/600-12.000 EUR), nueva seccion de plazos (01/04 - 02/07/2025, fraccionamiento 60/40).
- `gipuzkoa.md` -- 65+ datos completados: ascendientes (321 EUR), discapacidad por grado (1.350/2.700 EUR), viudedad (2.150 EUR), edad (385/700 EUR con formula progresiva), cuidado menores/dependientes (600-1.200 EUR), vivienda (alquiler 20-30%/1.530-1.955 EUR, compra 23%), inversiones (PYMES 23%, prioritarias 30%, ecologica 18%), donativos (23%/1.955 EUR, investigacion 25%/2.500 EUR), prevision social (autonomos 2.400 EUR), eficiencia energetica (23-40%/1.530-1.955 EUR), vehiculos (30% electricos, 25% hibridos/1.000 EUR).

### Mejoras en SKILL.md

- Nuevas instrucciones en Fase 4: verificar SIEMPRE los requisitos de acceso a cada deduccion antes de recomendarla (edad, renta, situacion personal, fecha de contrato, incompatibilidades).
- Nueva seccion sobre distinguir "deduccion eliminada" (estatal alquiler suprimida 2015, salvo regimen transitorio pre-2015) vs "deduccion restringida" (autonomicas vigentes pero limitadas a perfiles concretos).
- Nuevas notas de comportamiento 9 y 10: no asumir que una deduccion es aplicable solo porque existe; distinguir entre deducciones estatales suprimidas y autonomicas vigentes.
- Seccion de documentos de referencia forales con instrucciones de flujo alternativo.
- Fase 2 actualizada para detectar contribuyentes forales.

### Otros archivos modificados

- `references/regiones/indice-regiones.md` -- Tabla de territorios forales con escalas y aspectos destacados.
- `README.md` -- Reescritura completa: territorios forales como cubiertos, flujo foral, ejemplos de uso forales, arbol ampliado, cifras a 3.214 paginas, fuentes forales.
- `CHANGELOG.md` -- Creado con historial de versiones.

### Cifras de esta version

- 1.311 paginas de manuales forales procesadas (Navarra 308 + Alava 243 + Gipuzkoa 214 + Bizkaia 546)
- 4 archivos forales nuevos con IRPF completo
- ~70 deducciones corregidas o completadas en archivos existentes
- nacional.md expandido un 30% (de 486 a 632 lineas)
- 0 datos pendientes, vagos o sin cuantificar en todo el skill
- Total acumulado: 3.214 paginas de documentacion oficial, 23 archivos regionales, cobertura del 100% del territorio espanol

### Nota sobre Bizkaia

El archivo de Bizkaia usa datos del ejercicio 2024 porque la Diputacion Foral no habia publicado el manual 2025 en el momento de esta release. Hay una tarea programada que comprueba diariamente la publicacion del manual 2025. Cuando se publique, se actualizara bizkaia.md y se liberara la **v2025-4**.

---

## v2025-2 -- Correccion de datos y anexos de municipios

**Fecha:** 11 de abril de 2026

### Correcciones criticas

- `references/nacional.md` -- Reduccion por rendimientos del trabajo corregida: de 6.498 EUR / 2 tramos (dato de 2024) a 7.302 EUR / 3 tramos (dato correcto 2025). Nueva seccion 5.3 con la reduccion por rendimientos del trabajo artistico (novedad 2025, 30%, limite 150.000 EUR).

- `references/casos-especiales.md` -- Tributacion del ahorro en Ley Beckham corregida: de tipo fijo del 19% a escala progresiva IRNR (19%-28% en 5 tramos).

### Reescritura completa de deducciones autonomicas

Los 15 archivos regionales de CCAA de regimen comun han sido reescritos integramente a partir del Manual Practico de Renta 2025 - Parte 2 (PDF oficial de la AEAT, 633 paginas). Se ha pasado de una cobertura parcial (~25%) a la cobertura completa: 355 de 355 deducciones documentadas segun el indice oficial del PDF.

### Anexos de municipios

Incorporacion de listas de municipios con derecho a deducciones por despoblamiento en 6 archivos regionales: la-rioja.md (184 + 193 municipios completos), aragon.md, cantabria.md, extremadura.md, madrid.md, comunidad-valenciana.md (con referencias a normativa oficial).

### Otros cambios

- `SKILL.md` -- Nueva seccion en Fase 3 para preguntar siempre por el municipio exacto de residencia y cruzarlo con los anexos de despoblamiento.
- `README.md` -- Reescritura completa con nuevas secciones: "Que contiene este skill", "Anexos de municipios", "Novedades del ejercicio 2025", "Cifras del skill", fuentes con enlaces directos a los PDF.

---

## v2025-1 -- Version inicial

**Fecha:** 10 de abril de 2026

Primera version del skill con cobertura completa del IRPF 2025 para regimen comun.

### Contenido

- `SKILL.md` -- Flujo de trabajo en 5 fases (recibir borrador, confirmar datos, cuestionario de descubrimiento, analisis, informe)
- `references/nacional.md` -- Normativa IRPF estatal 2025 (escalas, minimos, reducciones, deducciones estatales)
- `references/casos-especiales.md` -- Ley Beckham, criptomonedas, exit tax, art. 7.p, nomadas digitales
- `references/regiones/` -- 15 archivos de CCAA + Ceuta y Melilla + indice + cuestionario de descubrimiento
- `README.md`, `LICENSE` (GPLv3), `.gitignore`
