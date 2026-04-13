# Modo Preparación - Declaración IRPF 2025 desde cero

Flujo de trabajo para calcular la declaración del IRPF cuando el contribuyente no tiene borrador previo o quiere reconstruir su declaración a partir de documentación en bruto.

---

## 1. Principios del modo preparación

- **Cuándo usar este modo vs. modo revisión**: El modo preparación se utiliza cuando partimos de cero: documentos fiscales sin procesar (nóminas, certificados bancarios, facturas de autónomo, etc.). El modo revisión analiza un borrador AEAT preexistente.

- **Distinción crítica**: El skill CALCULA importes a partir de documentos y reglas IRPF. NO cumplimenta ni presenta la declaración en Renta WEB. El contribuyente o su asesor es responsable de introducir los datos en la plataforma de la AEAT.

- **Regla de prudencia**: Ante cualquier duda interpretativa, excluir el importe y avisar. Es mejor pedir documentación adicional que incluir un importe incorrecto.

- **Trazabilidad**: Cada importe calculado debe poder rastrearse a un documento origen específico. Se mantiene un registro de qué certificado, nómina o factura genera cada línea de cálculo.

- **Información incompleta**: Cuando falta documentación, el skill la pide explícitamente. Nunca asume valores (salarios medios, tasas de rendimiento, etc.).

- **Responsabilidad final**: El contribuyente o su asesor deben revisar todos los importes calculados y verificarlos contra sus datos fiscales en la AEAT antes de presentar.

---

## 2. Bloques de datos a recoger

El modo preparación estructura la recogida de información en bloques temáticos. Se procesan en orden. No todos los contribuyentes tienen todos los bloques: se pregunta primero cuáles aplican.

### 2.1 Identidad y unidad familiar

- NIF/NIE del contribuyente
- Estado civil a 31 de diciembre de 2025 (soltero, casado, separado, divorciado, viudo)
- Régimen matrimonial (si aplica): sociedad de gananciales, separación de bienes
- Hijos: número total, fechas de nacimiento exactas, custodia (compartida o exclusiva), si son mayores de edad
- Ascendientes convivientes: edad, si tienen rentas, grado de discapacidad
- Discapacidades en la unidad familiar: grado de minusvalía de cada miembro
- Comunidad autónoma de residencia a 31/12/2025 (importante para deducciones)
- Municipio exacto de residencia (algunos municipios tienen deducciones por despoblamiento)
- Familia numerosa: categoría general (3+ hijos) o especial (4+ hijos). Certificado vigente.
- Familia monoparental: si aplica (custodia exclusiva o pensión compensatoria)
- Tributación individual vs. conjunta: si hay cónyuge, valorar ambas opciones

**Documentos**: DNI/NIF, libro de familia, certificado de minusvalía, resolución judicial de separación/divorcio, certificado de familia numerosa

---

### 2.2 Rendimientos del trabajo

**Documentos típicos**: nóminas mensuales, certificado de retenciones (modelo 10T del pagador), certificado de pensiones del INSS, prestaciones SEPE, certificados de servicios

**Datos a extraer**:

- Retribuciones íntegras: salario base, pagas extras, bonus, gratificaciones, dietas (indicar cuáles son exentas), complementos, prestaciones
- Contribuciones a Seguridad Social a cargo del trabajador (descontadas de nómina)
- Retenciones de IRPF practicadas por cada pagador (línea "retención" o "IRPF retenido")
- Número de pagadores distintos durante 2025
- Rendimientos en especie: valoración de comedor de empresa, seguros de salud, vehículos de empresa (usar valor catastral si aplica)
- Indemnizaciones por despido: importe total, parte exenta (hasta 180 000 EUR con límites adicionales) vs. parte no exenta
- Atrasos de ejercicios anteriores (rendimientos irregulares calificados como tales)
- Rentas potencialmente exentas: art. 7.p (trabajos extranjero) u otras causas

**Cálculo**:

1. Ingresos íntegros = suma de todas las retribuciones brutas de todos los pagadores + rendimientos en especie
2. Gastos deducibles art. 19 LIRPF: cuotas a SS, colegios profesionales, sindicatos, gastos de defensa jurídica
3. Rendimiento neto previo = ingresos íntegros - gastos deducibles
4. Reducción por rendimientos del trabajo (sistemas de tramos y fórmulas según el importe neto previo)
5. Rendimiento neto reducido del trabajo

Ver referencias completas en `nacional.md` sección 5.

---

### 2.3 Rendimientos del capital mobiliario

**Documentos**: certificados bancarios de intereses, certificados de dividendos, liquidaciones de fondos de inversión, extractos de brokers, certificados de seguros de ahorro, letras del Tesoro

**Datos a extraer**:

- Intereses de cuentas corrientes y depósitos a plazo
- Dividendos de acciones de sociedades anónimas
- Rendimientos de letras del Tesoro, bonos del Estado, obligaciones
- Rendimientos de fondos de inversión: diferencia entre valor de reembolso final y valor de suscripción inicial
- Rendimientos de pólizas de seguros de vida/ahorro
- Retenciones practicadas (normalmente 19% sobre rendimientos)
- Fecha de adquisición (relevante para cálculo de ganancias/pérdidas si se liquida)

**Clasificación**:

- Rendimientos a integrar en base del ahorro: la mayoría (intereses, dividendos de no relacionadas, fondos, etc.)
- Rendimientos a integrar en base general: propiedad intelectual del propio autor, rentas de activos cesan o transmiten

Ver referencias en `nacional.md` sección 7.

---

### 2.4 Rendimientos del capital inmobiliario

**Documentos**: contratos de arrendamiento, recibos de alquileres cobrados, recibos de IBI, pólizas de seguro, extractos de hipoteca (intereses), recibos de comunidad, facturas de reparaciones, certificado catastral

**Para cada inmueble arrendado**:

- Ingresos íntegros: rentas mensuales cobradas + importes pendientes de cobro (deudores)
- Gastos deducibles:
  * Intereses de préstamo hipotecario o línea de crédito para adquisición o mejora
  * Tributos: IBI, tasas municipales (basura, etc.)
  * Cuota de comunidad de propietarios
  * Prima de seguro de hogar
  * Gastos de conservación y reparación (NO mejora capital)
  * Servicios personales: portería, vigilancia, jardinería
  * Amortización: 3% anual sobre el mayor de (coste adquisición menos valor suelo) o (valor catastral construcción)
  * Suministros a cargo del propietario: agua, luz, gas, internet
  * Saldos de dudoso cobro: alquileres no pagados con antigüedad suficiente
  
- Reducción por arrendamiento de vivienda: 50% en viviendas arrendadas bajo contrato nuevo (desde 26/05/2023) con requisitos Ley de Vivienda; 60% o 90% en zonas tensionadas según condiciones

- Rendimiento neto reducido = (ingresos - gastos - reducción %)

**Inmuebles NO arrendados** (segundas viviendas, locales vacíos): imputación de renta inmobiliaria = 1,1% o 2% del valor catastral según revisión catastral reciente

Ver referencias en `nacional.md` sección 6.

---

### 2.5 Actividades económicas (autónomos)

Si el contribuyente declara actividad económica, cargar `references/autonomos.md` para el flujo completo.

**Datos mínimos para decidir régimen**:

- Empresario o profesional: epígrafe(s) IAE principal(es)
- Fecha de alta en el censo de actividades económicas
- Cifra de negocios (facturación) del ejercicio 2025
- Régimen elegido: Estimación Directa (Simplificada o Normal) o Estimación Objetiva (Módulos)
- Categoría principal de actividad (comercio, servicios, profesión, etc.)
- Número de empleados
- Bienes de inversión adquiridos durante 2025 (valor, depreciación)
- Pagos fraccionados realizados (modelos 130/131, importes de cada trimestre)
- Pluriactividad: si compagina trabajo por cuenta ajena con autónomo

**Documentación fiscal**: modelo 10T de pagadores, modelos 130/131 de trimestres anteriores, balances, cuentas de resultados, libro registro de facturas

Todo el detalle en `references/autonomos.md`.

---

### 2.6 Ganancias y pérdidas patrimoniales

**Documentos**: escrituras de compraventa de inmuebles, liquidaciones de broker (acciones vendidas), extractos de exchanges de criptomonedas, certificados de premios, documentación de transmisiones por herencia

**Categorías**:

a) **Transmisiones onerosas**: venta de bienes (inmuebles, acciones, fondos, criptomonedas)
   - Valor de adquisición: precio de compra + gastos notariales + mejoras - amortizaciones anteriores
   - Valor de transmisión: precio de venta - gastos de enajenación
   - Método FIFO para acciones e instrumentos cripto
   - Coeficientes de abatimiento: bienes adquiridos antes de 31/12/1994, límite 400 000 EUR acumulado

b) **Ganancias no derivadas de transmisión**: premios, subvenciones, indemnizaciones (si aplicables)

c) **Pérdidas**: compensables con ganancias del mismo tipo en 2025 y 4 años posteriores

Ver referencias en `nacional.md` sección 9 y `referencias/casos-especiales.md` para criptomonedas y exit tax.

---

### 2.7 Retenciones y pagos a cuenta (consolidación)

Agregar TODAS las retenciones de todos los bloques anteriores:

- Retenciones en nóminas (certificado modelo 10T)
- Retenciones en capital mobiliario (certificados bancarios, dividendos)
- Retenciones en capital inmobiliario (si hay)
- Retenciones en actividades económicas (si cliente tiene actividad)
- Pagos fraccionados (modelos 130/131 trimestres 1-4)
- Retenciones sobre ganancias patrimoniales
- Ingresos a cuenta por rendimientos en especie

**Total consolidado** = suma de todas las retenciones y pagos. Se resta de la cuota líquida total para obtener la cuota diferencial (a ingresar o a devolver).

---

### 2.8 Aportaciones y donativos deducibles

- **Planes de pensiones**: límite 1 500 EUR anual (o 4 250 EUR si autónomo con reducción especial, o 8 500 EUR si hay aportación complementaria empresarial)
- **Pensiones compensatorias**: al ex-cónyuge por resolución judicial
- **Donativos**: a entidades acogidas a Ley de Mecenazgo: 80% primeros 250 EUR, 40% resto (45% si recurrente)
- **Cuotas sindicales**: deducibles como gasto de trabajo (ya incluidas en 2.2) o como deducción de base
- **Cuotas a partidos políticos**: 20% de la cuota, máximo 600 EUR de base imponible

---

### 2.9 Deducciones estatales y autonómicas

Preguntar específicamente sobre:

- **Vivienda habitual**: hipoteca formalizada antes de 01/01/2013 (deducción 15% hasta 9 040 EUR anuales si cumple requisitos)
- **Eficiencia energética**: obras con certificado energético previo y posterior
- **Vehículo eléctrico**: adquisición de vehículos con etiqueta CERO o ECO (hasta 2 500 EUR en circunstancias)
- **Inversión en EECC**: aportación a sociedades de nueva creación
- **Maternidad**: madre trabajadora con hijos menores de 3 años (hasta 1 200 EUR si tienen menos de 1 año)
- **Familia numerosa o personas con discapacidad a cargo**
- **Deducciones autonómicas**: varían por comunidad. Cargar archivo regional y seguir preguntas clave

---

## 3. Normalización de entradas heterogéneas

### 3.1 Formatos aceptados

El skill acepta cualquier formato de documento origen:

- PDF escaneado (nómina, certificado bancario, contrato)
- Imagen fotográfica o captura de pantalla (extracto de broker, recibo)
- Archivo Excel o CSV (listado de ingresos, gastos)
- Texto plano pegado (descripción verbal de datos)
- Documento Word o similar

No importa el formato: se normaliza a datos estructurados.

### 3.2 Procedimiento de normalización

1. Identificar tipo de documento: nómina, certificado de retenciones, contrato de alquiler, extracto bancario, modelo 130, factura, etc.
2. Extraer campos relevantes según bloque temático (sección 2 anterior)
3. Mostrar al usuario tabla resumen con importes interpretados
4. Solicitar confirmación explícita antes de usar los importes
5. Si valor es ilegible o ambiguo: pedir transcripción manual al usuario

### 3.3 Reglas de seguridad

- **NUNCA adivinar un importe** ilegible o dudoso
- Marcar con `[ESTIMADO]` cualquier valor no verificable con certeza
- Si documento parece incompleto (nómina de 11 meses en lugar de 12): avisar y preguntar si hay más páginas
- Distinguir siempre entre importes brutos y netos: trabajar con bruto + retención separada
- Detectar inconsistencias: si certificado bancario muestra retención del 25% pero norma dice 19%, marcar discrepancia

---

## 4. Consolidación y cálculo

Una vez completos todos los bloques relevantes, el cálculo IRPF sigue el flujo de `nacional.md` sección 13:

1. **Base imponible general** = rendimientos trabajo + capital inmobiliario + actividades económicas + ganancias no derivadas de transmisión + imputaciones renta
2. **Base imponible ahorro** = capital mobiliario (ahorro) + ganancias derivadas de transmisión
3. Aplicar reducciones de base (planes de pensiones, pensiones compensatorias, etc.)
4. **Base liquidable general y ahorro**
5. Aplicar escalas: estatal + autonómica (o foral si aplica)
6. **Cuota íntegra**
7. Restar deducciones: estatales + autonómicas
8. **Cuota líquida total**
9. Restar retenciones + pagos a cuenta + pagos fraccionados
10. **Cuota diferencial** (positiva = ingresar, negativa = devolver)

Este flujo está completo en `nacional.md`. No se duplica aquí.

---

## 5. Entregable final: paquete Renta WEB

### 5.1 Tabla de casillas principales

Presentar tabla con casillas IRPF más relevantes:

| Casilla | Concepto | Importe calculado | Documento justificativo |
|---------|----------|-------------------|-----------------------|
| 0001 | Rendimientos íntegros trabajo | XXX EUR | Certificado pagador, nóminas |
| 0012 | Retenciones trabajo | XXX EUR | Modelo 10T |
| 0100 | Rendimientos netos capital mobiliario | XXX EUR | Certificados bancarios, broker |
| 0200 | Rendimientos netos capital inmobiliario | XXX EUR | Recibos alquiler, IBI |
| 0500 | Rendimientos netos actividades económicas | XXX EUR | Modelo 130/131, balance |
| 0700 | Ganancia/pérdida patrimonial | XXX EUR | Liquidaciones broker, escrituras |
| 1000 | Base imponible general | XXX EUR | Consolidación 4.1 a 4.3 |
| 1100 | Base imponible ahorro | XXX EUR | Consolidación 4.2 |
| 2000 | Cuota íntegra | XXX EUR | Aplicar escala fiscal |
| 3000 | Cuota líquida | XXX EUR | Restar deducciones |
| 3200 | Retenciones y pagos a cuenta | XXX EUR | Consolidación 2.7 |
| 3300 | Cuota diferencial | XXX EUR | (2000 o 3000) - 3200 |

### 5.2 Comparación con datos fiscales AEAT

Si el contribuyente tiene acceso a "Mis datos" en Renta WEB o porta fiscal, comparar:

- Ingresos declarados vs. ingresos que constan en Hacienda (cruce de datos de pagadores)
- Retenciones calculadas vs. certificados de retenciones en poder de AEAT
- Discrepancias: avisar y solicitar aclaración al contribuyente

---

### 5.3 Checklist de verificación profesional

Antes de trasladar importes a Renta WEB, revisar:

- [ ] Todos los ingresos declarados coinciden con certificados oficiales (10T, 10A, certificados bancarios)
- [ ] Las retenciones cuadran exactamente con certificados de pagadores
- [ ] Gastos deducibles de actividades económicas están correctamente clasificados (gasto corriente vs. inversión)
- [ ] Deducciones autonómicas cumplen TODOS los requisitos de acceso (documentación, límites, períodos)
- [ ] Opción tributación individual vs. conjunta es la más favorable (si aplica)
- [ ] Pagos fraccionados (130/131) están correctamente conciliados
- [ ] No hay ingresos omitidos que Hacienda pueda detectar por cruce de datos de terceros
- [ ] Imputación de renta inmobiliaria (viviendas vacías) correctamente calculada
- [ ] Ganancias patrimoniales: método de cálculo de valor de adquisición verificado con documentos
- [ ] Período de tenencia (bienes pre-1995 con abatimiento) acreditado con documentación

---

## FUENTES OFICIALES

- Manual Práctico de Renta 2025 (AEAT): https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html
- Programa Renta WEB: https://sede.agenciatributaria.gob.es/Sede/Renta.html
- Ley del Impuesto sobre la Renta de las Personas Físicas (LIRPF): https://www.boe.es/
- Real Decreto 439/1997 (Reglamento IRPF): https://www.boe.es/
