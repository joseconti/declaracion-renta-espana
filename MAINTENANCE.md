# MAINTENANCE.md — Checklist de actualización anual del skill

Este documento enumera todos los archivos y valores que deben revisarse cuando el ejercicio fiscal cambia (es decir, al arrancar la campaña del ejercicio N+1). Seguir este proceso en orden reduce el riesgo de publicar datos obsoletos o contradictorios.

---

## 0. Antes de empezar: obtener las fuentes del nuevo ejercicio

| Fuente | URL / localización |
|---|---|
| Manual Práctico IRPF (nuevo año) — Parte 1 | `https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-{AÑO}/ManualRenta{AÑO}Parte1_es_es.pdf` |
| Manual Práctico IRPF — Parte 2 (deducciones autonómicas) | `https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-{AÑO}-Deducciones-autonomicas/ManualRenta{AÑO}Parte2_eu_es.pdf` |
| Índice web del manual (capítulos individuales) | `https://sede.agenciatributaria.gob.es/Sede/Ayuda/{2dígitosdAÑO}Manual/100.html` |
| BOE — Orden de modelos de declaración (Orden HAC) | Buscar en `https://www.boe.es` con texto "modelos declaracion Renta {AÑO}" |
| Ley de Presupuestos Generales / Ley de medidas fiscales | BOE, enero del año de la campaña |
| Manuales forales (Navarra, Álava, Gipuzkoa, Bizkaia) | Webs de cada Hacienda Foral (ver §9) |

Descargar los PDF y tenerlos a mano antes de editar ningún archivo.

---

## 1. SKILL.md — valores año-dependientes

| Campo | Ubicación | Qué actualizar |
|---|---|---|
| Frontmatter `description` | Líneas 1-5 | "renta 2025", "ejercicio 2025" → nuevo año |
| Frontmatter `trigger` | Mismas líneas | Keywords "renta 2025", "IRPF 2025" → nuevo año |
| Referencia al año en notas de comportamiento | Cuerpo de SKILL.md | Buscar "2025" con grep; actualizar año de ejercicio en cada mención |
| Hardcoded "2026" (año de campaña) | Cuerpo de SKILL.md | Plazos de presentación, fechas de domiciliación |
| Nota de comportamiento #12 (gastos difícil justificación) | Cuerpo de SKILL.md | Verificar si el porcentaje (actualmente 5%) ha cambiado para el nuevo ejercicio |
| Nota de comportamiento #15 (perfiles especiales) | Cuerpo de SKILL.md | Verificar si cambian las referencias a nacional-detalle.md |
| Advertencia inline de Bizkaia | Rama foral Fase 2 | Actualizar si bizkaia.md ya cubre el nuevo ejercicio |

Comando de auditoría rápida:
```bash
grep -n "2025\|2026" SKILL.md | grep -v "^#"
```

---

## 2. references/nacional.md (núcleo) — valores año-dependientes

| Clase de valor | Sección | Qué verificar |
|---|---|---|
| Escala general estatal | §2 | 6 tramos: tipos y umbrales (fuente: c15 del manual AEAT) |
| Escala del ahorro estatal | §3 | 5 tramos: tipos y umbrales (fuente: c15 del manual AEAT) — el tramo >300.000€ subió al 15%/30% combinado en 2025; verificar si hay nuevos cambios |
| Mínimo del contribuyente | §4.1 | 5.550 EUR — verificar si la LGP lo modifica |
| Mínimos por descendientes | §4.2 | 2.400/2.700/4.000/4.500 EUR — verificar LGP |
| Mínimos por ascendientes | §4.3 | 1.150/2.550 EUR — verificar LGP |
| Mínimo por discapacidad | §4.4 | 3.000/9.000/3.000/12.000 EUR — verificar LGP |
| Reducción por rendimientos del trabajo | §5.1–5.4 | Umbrales y fórmulas (7.302 EUR, tramos 14.852/17.673/19.747) — cambiaron en 2025; verificar LGP siguiente |
| Reducción por tributación conjunta | §12 | 3.400/2.150 EUR — verificar LGP |
| Obligación de declarar — umbrales | §1 | 22.000/15.876 EUR y otros umbrales — verificar Orden HAC del nuevo año |
| Fechas de campaña | §1 o cabecera | Inicio campaña, fin campaña, domiciliación, segundo plazo |
| Planes de pensiones — límites | §10 | 1.500/8.500/10.000 EUR — verificar LGP; son especialmente volátiles |
| Fecha de caducidad deducciones energéticas | §11 (índice) / nacional-detalle.md §11 | Las deducciones de eficiencia energética (rehabilitación, ventanas, HVAC) tienen fecha de expiración — comprobar si siguen vigentes o han sido prorrogadas/suprimidas |
| Deducción vehículo eléctrico — vigencia | §11 (índice) | Comprobar si la deducción del 15% (base máx 20.000€ = 3.000€) y recarga (15%, base 4.000€ = 600€) siguen vigentes o tienen nueva fecha límite |
| URL base del manual AEAT | Todas las citas inline | Patrón `irpf-2025` → `irpf-{AÑO}` en todas las URLs de fuente |

---

## 3. references/nacional-detalle.md — valores año-dependientes

| Clase de valor | Sección | Qué verificar |
|---|---|---|
| Detalle de deducciones estatales (11.1–11.10) | §11 completa | Porcentajes, bases máximas, topes, condiciones y vigencias de cada deducción estatal; especialmente: eficiencia energética (fecha de caducidad), vehículo eléctrico (fecha de caducidad), maternidad (1.200 EUR + 1.000 EUR custodia), familia numerosa/discapacidad (8 tipos) |
| Perfiles especiales de contribuyente | §5.6–5.12, §8.4, §9.6 | Mutualistas (DT 2ª LIRPF), pensionistas, trabajador del hogar — verificar si hay cambios normativos |
| Flujo de cuota diferencial y ejemplos numéricos | §13.1–13.4 | Verificar que los tipos y cálculos de los ejemplos siguen siendo correctos con el nuevo ejercicio; actualizar años en los ejemplos |
| Obligaciones formales — plazos | §13 | Fechas de la campaña, fraccionamiento 60/40, modelos |

---

## 4. references/autonomos.md — valores año-dependientes

| Clase de valor | Sección | Qué verificar |
|---|---|---|
| Gastos de difícil justificación | §20 | Porcentaje (5% para 2025) y tope (2.000 EUR, art. 30 RIRPF) — verificar si hay nuevas medidas temporales |
| Límite EDS (estimación directa simplificada) | §2 | 600.000 EUR — verificar si se modifica |
| Límite módulos | §3 | 250.000 EUR — verificar si se modifica |
| Tabla de amortización simplificada EDS | §2.4 | La tabla de 10 grupos es la Orden de 27 de marzo de 1998; estable, pero verificar si ha habido nueva orden |
| Retenciones por tipo de actividad | §4 o equivalente | Tipos de retención (7%/15%/19%/2%, etc.) — verificar si hay cambios en el RIRPF |
| Límites planes de pensiones | §10 | Los mismos que en nacional.md — sincronizar |
| Modelo 130 — criterio de exoneración | §5.1 | Art. 109 RIRPF: 70% de ingresos con retención — verificar si cambia el umbral legal |
| Bienes de inversión IVA | §6.2 | Umbral 3.005,06 EUR (art. 108 LIVA) — estable pero verificar |
| Año del ejercicio en encabezados | Todo el archivo | Buscar "2025" con grep |

---

## 5. references/casos-especiales.md — valores año-dependientes

| Clase de valor | Sección | Qué verificar |
|---|---|---|
| Escala Ley Beckham — trabajo | §1 | 24%/47% — verificar si hay cambios en art. 93 LIRPF |
| Escala Ley Beckham — ahorro | §1 | 19%→30% en 6 tramos — verificar |
| Tipo máximo IRNR | §1 | Verificar |
| Exención art. 7.p | §5 | 60.100 EUR — verificar si se actualiza |
| Coeficientes de abatimiento — cómputo | §9.6 | 11,11%, límite 400.000 EUR acumulado (DT 9ª LIRPF) — estable normalmente |
| Modelo 720/721 — umbrales | §5.3 | 50.000 EUR — verificar |
| URLs de cita | Secciones con fuente | Actualizar `irpf-2024`/`irpf-2025` → nuevo año |

---

## 6. references/regiones/ — archivos autonómicos (régimen común)

Para cada uno de los 15 archivos de CCAA + Ceuta y Melilla:

| Tarea | Detalle |
|---|---|
| Verificar novedades autonómicas | Buscar en el BOE y en los boletines autonómicos (BOJA, DOGC, etc.) si la CA ha aprobado nuevas deducciones o ha modificado importes, límites de renta o requisitos |
| Marcar "Novedad {AÑO}" | Añadir la etiqueta en las deducciones modificadas, siguiendo el estilo existente |
| Actualizar leyes base | Si la CA ha aprobado una ley de acompañamiento presupuestario, actualizar la referencia normativa del encabezado |
| Archivos prioritarios a revisar | cataluna.md (Decreto Ley 5/2025 en vigor para 2025; verificar si hay nueva norma para 2026), comunidad-valenciana.md (DANA, Ley 5/2025), murcia.md, la-rioja.md |
| Recuento de deducciones | Tras cualquier adición o eliminación, actualizar el número en `indice-regiones.md` (fuente de verdad) y en el árbol de `README.md` |

Ley y decreto ley a vigilar anualmente:

- **Cataluña:** Decreto Ley 5/2025 (en vigor 2025). Vigilar si se aprueba nueva norma para el ejercicio siguiente. Posible deducción por rehabilitación rural (Ley 8/2025, 15%, base 6.000€) — ausente en 2025, señalada para 2026.
- **Comunitat Valenciana:** Ley 5/2025 — verificar si hay continuidad o cambios en las deducciones DANA.
- **Bizkaia:** ver §9 abajo.

---

## 7. references/regiones/indice-regiones.md — fuente de verdad de recuentos

Este archivo es la **única fuente de verdad** para el número de deducciones por CCAA. Mantenerlo sincronizado con los archivos regionales reales.

Proceso de verificación:
```bash
# comprobar número real de deducciones en cada archivo
for f in andalucia aragon asturias baleares canarias cantabria \
          castilla-la-mancha castilla-y-leon cataluna extremadura \
          galicia madrid murcia la-rioja comunidad-valenciana; do
  count=$(grep -c "^### " references/regiones/${f}.md 2>/dev/null)
  echo "$f: $count"
done
```

Revisar si algún `###` es en realidad una "NOTA" o "Orden de aplicación" (no una deducción) y ajustar el recuento a mano. Después de verificar, actualizar también el árbol de `README.md` para que coincida.

---

## 8. references/regiones/ — territorios forales

| Archivo | Estado actual | Acción anual |
|---|---|---|
| navarra.md | IRPF foral 2025 completo | Verificar publicación del Manual Práctico de Hacienda Foral de Navarra del nuevo ejercicio; actualizar escala (13%–52%), mínimos, umbrales de obligación de declarar y plazos |
| alava.md | IRPF foral 2025 completo | Verificar Norma Foral y Manual de la Diputación Foral de Álava; actualizar SMI si cambia |
| gipuzkoa.md | IRPF foral 2025 completo | Verificar Manual de la Diputación Foral de Gipuzkoa; actualizar plazos |
| bizkaia.md | **PENDIENTE: ejercicio 2025 documentado (NF 2/2025), pero escala del ahorro de 9 tramos entra en vigor el 01/01/2026** | Para la campaña 2026 (ejercicio 2025): aplicar escala ahorro de 5 tramos (vigente 2025). Para la campaña 2027 (ejercicio 2026): aplicar la nueva escala del ahorro de 9 tramos (hasta 28%) aprobada en NF 2/2025 con efectos 2026. Verificar publicación del manual oficial de Bizkaia 2025 si aún no se ha publicado. |

Para los cuatro territorios forales, las URLs de los manuales son:
- Navarra: `https://hacienda.navarra.es`
- Álava: `https://web.araba.eus/es/hacienda`
- Bizkaia: `https://www.bizkaia.eus/es/hacienda-y-finanzas`
- Gipuzkoa: `https://www.gipuzkoa.eus/es/hacienda-y-finanzas`

---

## 9. README.md y documentación

| Campo | Qué actualizar |
|---|---|
| Encabezado: ejercicio fiscal, fechas de campaña | "Ejercicio fiscal: 2025", "Campaña de presentación: del 8 de abril al 30 de junio de 2026", domiciliación y segundo plazo |
| Sección "Novedades del ejercicio" | Añadir o revisar los cambios del nuevo ejercicio; eliminar los del anterior si ya no son novedad |
| Árbol de ficheros | Verificar que refleja todos los archivos existentes; no listar archivos que no existan |
| Recuento de deducciones ("más de 383") | Recalcular sumando el output del script del §7 |
| URLs de fuentes | Verificar que las URLs del Manual AEAT apuntan al nuevo año; actualizar patrón `IRPF-2025` → `IRPF-{AÑO}` |
| Limitaciones conocidas | Actualizar o eliminar la limitación de Bizkaia si ya está resuelta |

---

## 10. CHANGELOG.md — proceso de publicación de versión

Al completar la actualización anual, añadir una entrada al inicio del CHANGELOG con el siguiente formato:

```
## v{AÑO}-X.Y — [Título descriptivo]

**Fecha:** DD de mes de AAAA

### Resumen
[1-2 párrafos]

### Correcciones fiscales
- `archivo` -- descripción del cambio con fuente oficial

### Actualizaciones de normativa
- `archivo` -- descripción

### Documentación
- `archivo` -- descripción

### Fuentes
- [fuentes utilizadas]
```

Reglas del CHANGELOG:
- Una entrada por versión; no editar entradas ya publicadas
- Toda corrección fiscal debe citar la fuente oficial (artículo de ley, URL del manual AEAT, BOE)
- Los recuentos de deducciones en el CHANGELOG son informativos; la fuente de verdad es siempre `indice-regiones.md`

---

## 11. Búsquedas de auditoría rápida (ejecutar antes de publicar)

```bash
# hardcoded del año anterior en todos los archivos del skill
grep -rn "2025" SKILL.md references/ README.md | grep -v "^Binary"

# URLs que apuntan al manual del año anterior
grep -rn "irpf-2025\|IRPF-2025\|irpf-2024\|IRPF-2024" references/ SKILL.md

# verificar recuento de deducciones por CCAA (ver §7)
for f in andalucia aragon asturias baleares canarias cantabria \
          castilla-la-mancha castilla-y-leon cataluna extremadura \
          galicia madrid murcia la-rioja comunidad-valenciana; do
  count=$(grep -c "^### " references/regiones/${f}.md 2>/dev/null)
  echo "$f: $count"
done

# comprobar que no existan archivos listados en README que no estén en disco
ls references/regiones/

# comprobar que SKILL.md no supera el límite de frontmatter (~1024 chars)
head -20 SKILL.md | wc -c
```

---

## 12. Orden recomendado de actualización

1. Obtener manuales AEAT y forales del nuevo ejercicio (§0)
2. Actualizar `references/nacional.md` — escalas, mínimos, reducción por trabajo (§2)
3. Actualizar `references/nacional-detalle.md` — deducciones estatales, vigencias, ejemplos (§3)
4. Actualizar `references/autonomos.md` — gastos difícil justificación, límites (§4)
5. Actualizar `references/casos-especiales.md` — Beckham, cripto (§5)
6. Revisar archivos autonómicos de régimen común (§6) — priorizar Cataluña y C. Valenciana
7. Actualizar territorios forales (§8) — prestar especial atención a Bizkaia
8. Actualizar `indice-regiones.md` con recuentos verificados (§7)
9. Actualizar `SKILL.md` — año, fechas, notas de comportamiento (§1)
10. Actualizar `README.md` — fechas, árbol, recuentos, fuentes (§9)
11. Ejecutar auditorías de búsqueda (§11)
12. Publicar entrada en `CHANGELOG.md` (§10)
