# Changelog

Todas las versiones notables de este skill se documentan en este archivo.

---

## v2025-3 -- Territorios forales y auditoria completa de requisitos

**Fecha:** 12 de abril de 2026

### Territorios forales: nuevos archivos

- `references/regiones/navarra.md` -- IRPF foral 2025 completo de la Comunidad Foral de Navarra. Escala general de 11 tramos (13%-52%), escala del ahorro de 6 tramos (20%-28%), minimos personales y familiares, deducciones de cuota (alquiler 15%, donaciones 25-75%, energias renovables 15%, vehiculos electricos), obligacion de declarar, plazos. Fuente: Manual Practico IRPF 2025 de Hacienda Foral de Navarra (308 paginas).

- `references/regiones/alava.md` -- IRPF foral 2025 completo de Alava/Araba. Escala general de 7 tramos (23%-49%), escala del ahorro de 5 tramos (20%-25%), deducciones por descendientes (668-2.151 EUR), ascendientes (385 EUR), discapacidad (932-1.992 EUR), vivienda (alquiler 20%/35%, compra 23%/25%), EPSV, actividad economica, bonificacion del 15% en municipios pequenos. Fuente: Manual Practico IRPF 2025 de la Diputacion Foral de Alava (243 paginas).

- `references/regiones/gipuzkoa.md` -- IRPF foral 2025 completo de Gipuzkoa. Escala general de 8 tramos (23%-49%), reduccion por rendimientos del trabajo de 8.000 EUR, deduccion por actividades economicas del 23%, vivienda (alquiler hasta 1.955 EUR), donaciones, plazos (7 abril - 2 julio 2026). Fuente: Manual Practico IRPF 2025 de la Diputacion Foral de Gipuzkoa (214 paginas).

- `references/regiones/bizkaia.md` -- IRPF foral de Bizkaia. Escala general de 8 tramos (23%-49%), bonificaciones por rendimientos del trabajo, descendientes 668-2.151 EUR, alquiler 20-30%. Basado en el manual del ejercicio 2024 (546 paginas) porque el manual 2025 no estaba publicado al cierre de esta version.

### Auditoria completa de requisitos

Se ha detectado que muchas deducciones autonomicas tenian requisitos incompletos (faltaban limites de renta, condiciones de edad, requisitos de situacion personal, porcentajes o cuantias sin especificar). Se ha realizado una auditoria sistematica de TODOS los archivos del skill, verificando cada deduccion contra las fuentes oficiales (Manual AEAT de 1.903 paginas y webs de haciendas forales/autonomicas).

**Correccion critica:** La deduccion por alquiler de vivienda habitual en Cataluna (deduccion 3 de cataluna.md) estaba documentada sin los requisitos restrictivos de acceso. Solo pueden aplicarla contribuyentes menores de 35 anos, desempleados 183+ dias, con discapacidad >= 65%, viudos >= 65 anos, o familias numerosas/monoparentales, y con base imponible inferior a 30.000 EUR (individual) o 45.000 EUR (conjunta). Este mismo patron de requisitos incompletos se encontro en otras CCAA.

**Archivos del regimen comun corregidos (15 CCAA):**

- `cataluna.md` -- Deduccion 3 (alquiler): anadidos requisitos de edad, desempleo, discapacidad, viudedad, familia numerosa y limites de renta. Deducciones 6, 7, 8 (donaciones): anadidos porcentajes (15%). Deduccion 9 (angel inversor): anadidos requisitos de empresa (1M facturacion, 1 trabajador, mantenimiento 3 anos).
- `asturias.md` -- 8 deducciones nuevas de 2025 completadas con cuantias y requisitos (autonomos despoblamiento 1.000 EUR, formacion trabajos cualificados 2.000 EUR, traslado domicilio fiscal 15%, emancipacion jovenes, gastos vitales jovenes < 35, gastos arrendamiento vivienda 500 EUR, ELA).
- `canarias.md` -- Deduccion 19 (alquiler): corregido porcentaje de 15-20% a 24%, limite de 740/760 EUR segun edad.
- `extremadura.md` -- Deduccion 8 (arrendamiento vivienda): anadidos requisitos restrictivos (edad, familia numerosa, discapacidad 65%), limites de renta (28.000/45.000 EUR), requisitos patrimoniales.
- `castilla-la-mancha.md` -- Deducciones 17, 18, 19 (donaciones): anadido porcentaje (15%). Deduccion 6 (discapacidad): anadido limite base imponible. Deduccion 12 (alquiler jovenes): anadidos limites de renta.
- `castilla-y-leon.md` -- Deduccion 4 (adopcion): anadidas cuantias (784 EUR nacional, 3.625 EUR internacional). Deduccion 17 (vivienda nueva construccion): anadido porcentaje (7,5%), base maxima (9.040 EUR).
- `cantabria.md` -- 3 deducciones completadas (traslado estudios 200 EUR, gastos educacion, ayuda domestica 20%/300 EUR).
- `murcia.md` -- 10 deducciones completadas con cuantias (material escolar 120 EUR, mujeres trabajadoras 300-400 EUR, idiomas 15%/300 EUR, Internet 30%/300 EUR, cristales 30%/150 EUR, deporte 30%/100 EUR, enfermedades raras 100%).
- `madrid.md` -- 5 deducciones completadas (inversion nueva creacion 40-50%/9.279-12.372 EUR, arrendamiento viviendas vacias 1.000 EUR, cambio residencia despoblacion 1.000 EUR, otras verificadas como estatales no autonomicas).
- `galicia.md` -- 3 deducciones completadas (nuevas tecnologias hogares 30%/100 EUR, inversion acciones MAB 15%/4.000 EUR, empresas en crecimiento 15-45%/4.000-35.000 EUR). Deduccion aldeas modelo (15%). Arrendamiento viviendas vacias (500 EUR/inmueble).
- `comunidad-valenciana.md` -- Deduccion donaciones ecologicas actualizada (20% primeros 250 EUR, 25% resto).
- `andalucia.md`, `aragon.md`, `baleares.md`, `la-rioja.md` -- Verificadas correctas; correcciones menores en cuantias de vehiculos electricos (La Rioja: 15%/3.000 EUR).

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
