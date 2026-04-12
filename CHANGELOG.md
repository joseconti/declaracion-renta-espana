# Changelog

Todas las versiones notables de este skill se documentan en este archivo.

---

## v2025-3 -- Territorios forales

**Fecha:** 12 de abril de 2026

### Nuevos archivos

- `references/regiones/navarra.md` -- IRPF foral 2025 completo de la Comunidad Foral de Navarra. Escala general de 11 tramos (13%-52%), escala del ahorro de 6 tramos (20%-28%), minimos personales y familiares, deducciones de cuota (alquiler 15%, donaciones 25-75%, energias renovables 15%, vehiculos electricos), obligacion de declarar, plazos. Fuente: Manual Practico IRPF 2025 de Hacienda Foral de Navarra (308 paginas).

- `references/regiones/alava.md` -- IRPF foral 2025 completo de Alava/Araba. Escala general de 7 tramos (23%-49%), escala del ahorro de 5 tramos (20%-25%), deducciones por descendientes (668-2.151 EUR), ascendientes (385 EUR), discapacidad (932-1.992 EUR), vivienda, EPSV, actividad economica, bonificacion del 15% en municipios pequenos. Fuente: Manual Practico IRPF 2025 de la Diputacion Foral de Alava (243 paginas).

- `references/regiones/gipuzkoa.md` -- IRPF foral 2025 completo de Gipuzkoa. Escala general de 8 tramos (23%-49%), reduccion por rendimientos del trabajo de 8.000 EUR, deduccion por actividades economicas del 23%, vivienda (alquiler hasta 1.955 EUR), donaciones, plazos (7 abril - 2 julio 2026). Fuente: Manual Practico IRPF 2025 de la Diputacion Foral de Gipuzkoa (214 paginas).

- `references/regiones/bizkaia.md` -- IRPF foral de Bizkaia. Escala general de 8 tramos (23%-49%), bonificaciones por rendimientos del trabajo, descendientes 668-2.151 EUR, alquiler 20-30%. Basado en el manual del ejercicio 2024 (546 paginas) porque el manual 2025 no estaba publicado al cierre de esta version.

### Archivos modificados

- `SKILL.md` -- Nueva seccion de documentos de referencia forales. Fase 2 actualizada: deteccion automatica de contribuyente foral, instrucciones para cargar el archivo foral correspondiente en lugar de nacional.md, nota sobre que los contribuyentes forales no tienen borrador de la AEAT.

- `references/regiones/indice-regiones.md` -- Antigua seccion "Nota sobre regimen foral" sustituida por tabla completa de los 4 territorios forales con escalas, numero de tramos y aspectos destacados. Nuevas fuentes de haciendas forales.

- `README.md` -- Reescritura significativa: nueva seccion "Territorios forales" en "Que contiene este skill", flujo de trabajo actualizado para incluir regimen foral, ejemplos de uso forales, arbol de estructura con separacion visual entre regimen comun y foral, cifras actualizadas a 3.214 paginas procesadas, eliminada la limitacion "No cubre regimen foral", nueva limitacion sobre Bizkaia 2024, fuentes de haciendas forales.

### Cifras de esta version

- 1.311 paginas de manuales forales procesadas (Navarra 308 + Alava 243 + Gipuzkoa 214 + Bizkaia 546)
- 4 archivos nuevos con IRPF foral completo (escalas, minimos, reducciones, deducciones)
- Total acumulado del skill: 3.214 paginas de documentacion oficial, 23 archivos regionales, cobertura del 100% del territorio espanol

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
