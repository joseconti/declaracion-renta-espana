# Indice de IRPF Autonomico 2025

Tabla comparativa de las 17 CCAA de regimen comun + 2 ciudades autonomas + 4 territorios forales. Cada archivo regional incluye AHORA tambien la escala autonomica general, la escala del ahorro, los minimos personales autonomicos (cuando son distintos de los estatales) y las deducciones autonomicas.

## Comunidades Autonomas de Regimen Comun (escalas y minimos 2025)

Marginales totales = marginal autonomico + marginal estatal (24,50%). Aplicable a partir de 300.000 EUR de base liquidable general.

| Comunidad | Archivo | Tramos | Marginal autonomico maximo | Marginal total | Minimo personal y familiar AUTONOMICO propio? | Deducciones |
|---|---|---|---|---|---|---|
| Madrid | madrid.md | 5 | **20,50%** | 45,00% | Si (todos los conceptos) | 23 |
| Castilla y Leon | castilla-y-leon.md | 5 | **21,50%** | 46,00% | Regulado, importes = estatal | 18 |
| Andalucia | andalucia.md | 5 | **22,50%** | 47,00% | Si (todos los conceptos) | 17 |
| Castilla-La Mancha | castilla-la-mancha.md | 5 | **22,50%** | 47,00% | No (escala = estatal) | 27 |
| Galicia | galicia.md | 5 | **22,50%** | 47,00% | Si (todos los conceptos) | 25 |
| Murcia | murcia.md | 5 | **22,50%** | 47,00% | No | 28 |
| Cantabria | cantabria.md | 6 | **24,50%** | 49,00% | No | 21 |
| Illes Balears | baleares.md | 9 | **24,75%** | 49,25% | Si (parcial: 65+, 2-4 desc., ascend., discap.) | 24 |
| Extremadura | extremadura.md | 9 | **25,00%** | 49,50% | No | 19 |
| Cataluna | cataluna.md | 8 | **25,50%** | 50,00% | Regulado, importes = estatal | 13 |
| Aragon | aragon.md | 9 | **25,50%** | 50,00% | No | 19 |
| Canarias | canarias.md | 7 | **26,00%** | 50,50% | Si | 29 |
| Asturias | asturias.md | 8 | **26,00%** | 50,50% | Si | 27 |
| La Rioja | la-rioja.md | 8 | **27,00%** | 51,50% | Si (solo discap. desc.) | 25 |
| Comunitat Valenciana | comunidad-valenciana.md | 11 | **29,50%** | 54,00% | Si | 41 |

**Lectura rapida:**
- **CCAA mas favorables a rentas altas:** Madrid (45,00% marginal total), Castilla y Leon (46,00%), Andalucia/Galicia/Murcia/CLM (47,00%).
- **CCAA mas gravosas a rentas altas:** Comunitat Valenciana (54,00%), La Rioja (51,50%), Asturias y Canarias (50,50%).
- **Diferencia maxima entre CCAA:** 9 puntos porcentuales (entre Madrid y Comunitat Valenciana).

**CCAA con minimo personal y familiar autonomico propio (distinto del estatal):**
Andalucia, Asturias, Illes Balears (parcial), Canarias, Galicia, Madrid, La Rioja (solo discapacidad de descendientes), Comunitat Valenciana.

## Ciudades Autonomas

Ceuta y Melilla NO tienen escala autonomica propia. Aplican la escala unica del art. 65 LIRPF (idéntica a la estatal del art. 63.1) y luego se benefician de la **bonificacion del 60% del art. 68.4 LIRPF** sobre la cuota integra correspondiente a las rentas obtenidas en estas ciudades. Es uno de los regimenes mas favorables del IRPF espanol.

| Ciudad | Archivo | Regimen |
|---|---|---|
| Ceuta | ceuta.md | Escala unica art. 65 LIRPF + bonificacion 60% art. 68.4 |
| Melilla | melilla.md | Escala unica art. 65 LIRPF + bonificacion 60% art. 68.4 |

## Territorios Forales (IRPF propio, NO regimen comun)

Navarra y los tres territorios historicos del Pais Vasco (Alava, Bizkaia, Gipuzkoa) tienen haciendas forales propias con un IRPF completamente independiente del estatal. Sus contribuyentes NO presentan la declaracion ante la AEAT sino ante sus respectivas Haciendas Forales. Cada archivo foral incluye escalas, minimos (aplicados como deducciones de cuota, NO como reducciones de la base — diferencia clave con el regimen comun), reducciones y deducciones completas.

| Territorio | Archivo | Escala general | Escala ahorro | Aspectos destacados | Estado 2025 |
|---|---|---|---|---|---|
| Navarra | navarra.md | 13%-52% (11 tramos) | 20%-28% (6 tramos) | Manual Teorico Hacienda Foral 2025 (act. 02-02-2026). Alquiler 15%, energias renovables. | OK |
| Alava/Araba | alava.md | 23%-49% (8 tramos) | 20%-25% (5 tramos) | Descendientes 668-2.151 EUR, EPSV, municipios pequenos +15% | OK |
| Bizkaia | bizkaia.md | 23%-49% (8 tramos) | 20%-25% (5 tramos) | **Datos basados en Manual 2024 + cambios confirmados de Norma Foral 2/2025 para 2025**. Nueva bonificacion del trabajo (8.000 EUR), arrendamiento vivienda 30%/70%, etc. | **Manual oficial 2025 NO publicado todavia** |
| Gipuzkoa | gipuzkoa.md | 23%-49% (8 tramos) | 20%-25% (5 tramos) | Manual de Divulgacion 2025 (marzo 2026). Bonificacion trabajo 8.000 EUR, regla 3% para valores < 10.000 EUR. | OK |

## Como recalcular un IRPF (resumen del flujo)

1. **Identificar territorio** del contribuyente.
2. **Si es regimen comun:** cargar `nacional.md` + `regiones/[ccaa].md` y aplicar el flujo de `nacional.md §13.1`.
3. **Si es foral:** cargar SOLO el archivo foral correspondiente (navarra.md, alava.md, bizkaia.md o gipuzkoa.md) y aplicar el flujo del propio archivo. NO usar `nacional.md` ni los archivos de regimen comun.

## Fuentes oficiales

**Regimen comun:**
- AEAT Manual Practico Renta 2025 - Parte 1 (PDF, 1.270 paginas): https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025/ManualRenta2025Parte1_es_es.pdf
- AEAT Manual Practico Renta 2025 - Parte 2 (PDF, 633 paginas, deducciones autonomicas): https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025-Deducciones-autonomicas/ManualRenta2025Parte2_es_es.pdf
- AEAT Guia deducciones autonomicas 2025 (HTML): https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/guia-deducciones-autonomicas.html
- BOE Orden HAC/277/2026 (modelo D-100): https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041

**Forales:**
- Hacienda Foral de Navarra: https://www.navarra.es/es/hacienda/renta-y-patrimonio
- Diputacion Foral de Alava: https://www.araba.eus
- Hacienda Foral de Bizkaia: https://www.bizkaia.eus
- Diputacion Foral de Gipuzkoa: https://www.gipuzkoa.eus
