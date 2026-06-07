# IRPF 2025 - Normativa Nacional (DETALLE)

Documento de detalle de la normativa estatal del IRPF para el ejercicio 2025. Complementa al núcleo `references/nacional.md`: contiene el material que NO se carga siempre, sino bajo demanda (al llegar a Fase 4 / Fase 4-prep o cuando se necesite el detalle de una deducción estatal, una reconstrucción desde datos en bruto, un perfil especial de contribuyente, un ejemplo numérico completo o las obligaciones formales).

Toda la información procede de fuentes oficiales: AEAT (Agencia Estatal de Administración Tributaria) y BOE.

Fuente principal: Manual Práctico de Renta 2025 de la AEAT
https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html

---

## MAPA DE SECCIONES (núcleo vs. detalle)

Las secciones conservan su numeración original para que las referencias externas sigan funcionando. Reparto entre los dos archivos:

**En el núcleo `references/nacional.md`** (cargar para régimen común):
- 1 Obligación de declarar; 1B Residencia fiscal; 1C Individualización de rentas
- 2 Escala general estatal; 3 Escala del ahorro estatal; 4 Mínimo personal y familiar
- 5.1-5.4.bis Rendimientos del trabajo (gastos, reducción por trabajo, reducción artística, rentas exentas, retribuciones en especie exentas)
- 6.1-6.3 Rendimientos del capital inmobiliario (alquiler, reducciones, imputación)
- 7.1-7.2 Rendimientos del capital mobiliario (base del ahorro, gastos)
- 8.1-8.3 y 8.5 Actividades económicas (regímenes, resumen; cooperativista)
- 9.1-9.4, 9.7, 9.8 Ganancias y pérdidas patrimoniales (cálculo, integración, compensación, exenciones, recompra art. 33.5, guía Renta Web acciones)
- 10 Reducciones de la base imponible
- 11 (solo ÍNDICE) Deducciones estatales de la cuota
- 12 Tributación conjunta vs individual

**En este archivo `references/nacional-detalle.md`** (cargar bajo demanda):
- 5.5 Reconstrucción del rendimiento del trabajo desde datos crudos
- 5.6-5.12 Perfiles especiales del trabajo (mutualista, pensionista, desempleado, trabajador del hogar, consejero, deportista, sacerdote)
- 6.4 Reconstrucción del rendimiento inmobiliario desde datos crudos
- 7.3 Reconstrucción del rendimiento del capital mobiliario desde datos crudos
- 8.4 Perfil especial: agricultor y ganadero
- 9.5 Reconstrucción de ganancias y pérdidas patrimoniales desde datos crudos
- 9.6 Perfil especial: heredero que vende bienes heredados
- 11.1-11.10 Deducciones estatales de la cuota (detalle completo)
- 13 Obligaciones formales, plazos, flujo de cuota diferencial y ejemplos numéricos completos (13.1-13.4)

Las secciones 5, 8 y 9 están repartidas entre ambos archivos: la parte conceptual y de cuantías está en el núcleo; la reconstrucción desde datos crudos y los perfiles especiales están aquí.

---

## 5.5. Cómo reconstruir el rendimiento del trabajo desde datos crudos

**Documentos necesarios:**
- Certificado de retenciones del pagador (modelo 10T o certificado de empresa)
- Nóminas mensuales (si no se tiene el certificado anual)
- Certificado del INSS (para pensionistas)
- Certificado del SEPE (para prestaciones de desempleo)

**Procedimiento:**
1. Sumar las retribuciones íntegras de todos los pagadores
2. Identificar rendimientos en especie y su valoración
3. Sumar cotizaciones a SS del trabajador (de las nóminas o del certificado)
4. Sumar retenciones de IRPF practicadas
5. Calcular gastos deducibles del art. 19 (SS + colegios + sindicatos + defensa jurídica, máx. 300 EUR)
6. Obtener rendimiento neto = ingresos íntegros - gastos deducibles
7. Aplicar reducción por rendimientos del trabajo (§5.2, en `nacional.md`)
8. Resultado = rendimiento neto reducido del trabajo

**Dato clave:** Si hay más de un pagador y el segundo y sucesivos suman > 1.500 EUR, el límite de no obligación baja de 22.000 a 15.876 EUR.

## 5.6. Funcionario con mutualidad (MUFACE, ISFAS, MUGEJU)

Las cuotas a mutualidades de funcionarios (MUFACE para funcionarios civiles, ISFAS para fuerzas y cuerpos de seguridad, MUGEJU para judicatura) son gastos deducibles de los rendimientos del trabajo, con límite del art. 19.2.a LIRPF (sin superar los límites generales de gastos deducibles).

**Régimen especial para jubilados funcionarios mutualistas:**
- Si el funcionario fue mutualista antes del 1/1/1979, una parte de la pensión de jubilación puede estar EXENTA del IRPF conforme a la Disposición Transitoria 2ª LIRPF
- Este caso es muy relevante para jubilados que fueron funcionarios
- La exención depende del régimen de cotización en vigor en el momento de la jubilación

**Tributación de prestaciones:**
- Las prestaciones de estas mutualidades se consideran rendimientos del trabajo (pensiones, asignaciones de jubilación)
- Están sujetas a retención (como el resto de rendimientos del trabajo)

## 5.7. Pensionista y jubilado

**Pensiones públicas de la Seguridad Social:**
- Son rendimientos del trabajo
- Están sujetas a retención

**Pensiones derivadas de planes de pensiones:**
- El 100% del importe del rescate tributa como rendimiento del trabajo
- EXCEPTO: rescate en forma de capital con aportaciones realizadas antes de 2007, que tiene reducción del 40% (aplicable solo a esa parte)
- No se aplica la reducción general por rendimientos del trabajo si los ingresos totales superan ciertos límites

**Pensiones por incapacidad permanente absoluta o gran invalidez:**
- SON EXENTAS 100% (art. 7.f LIRPF)
- No tributan en el IRPF

**Pensiones de viudedad y orfandad:**
- Son rendimientos del trabajo
- NO están exentas

**Mínimos personales incrementados para pensionistas:**
- Contribuyente mayor de 65 años: incremento adicional de +1.150 euros al mínimo personal
- Contribuyente mayor de 75 años: incremento adicional de +1.400 euros (adicionales al anterior)

**Anualidades por alimentos recibidas del ex-cónyuge:**
- Se consideran rendimientos del trabajo
- Están sujetas a retención (normalmente a cargo de quien las paga)

## 5.8. Desempleado

**Prestación por desempleo (SEPE):**
- Es rendimiento del trabajo sujeto a retención
- El SEPE actúa como pagador

**Prestación por desempleo en pago único para iniciar actividad económica:**
- EXENTA íntegramente del IRPF (art. 7.n LIRPF)
- Requisito: acreditar que se destina a iniciar una actividad económica por cuenta propia

**Subsidio por desempleo:**
- Es rendimiento del trabajo
- Está sujeto a retención

**Renta Activa de Inserción (RAI):**
- Es rendimiento del trabajo
- Está sujeta a retención

**Obligación de declarar en caso de múltiples pagadores:**
- Si el desempleado recibe prestaciones de desempleo y además tiene otro pagador (empresa, enseñanza, etc.) y el segundo pagador supera 1.500 EUR, está obligado a declarar aunque la suma sea inferior a 15.876 EUR

## 5.9. Trabajador del hogar

Los ingresos derivados del trabajo en el hogar se consideran **rendimientos del trabajo**.

**Características especiales:**
- Su empleador (el hogar/persona física) NO tiene obligación de retener IRPF
- Por tanto, el trabajador del hogar suele estar obligado a presentar declaración de la Renta
- Está incluido en el sistema especial de la Seguridad Social (no RETA), lo que implica aportaciones y cotizaciones diferentes al autónomo

**Gastos deducibles:**
- Cotizaciones a la Seguridad Social (cuota de trabajador)
- Pueden aplicarse otros gastos conforme al art. 19 LIRPF

## 5.10. Consejero de administración

**Retribución de consejeros y administradores:**
- Se considera rendimiento del trabajo (art. 17.2.e LIRPF)
- Está sujeta a retención en la fuente

**Retención practicada:**
- 35% sobre las retribuciones (o 19% si la entidad tiene cifra de negocios inferior a 100.000 EUR)
- La entidad debe practicar retención y declarar en modelo 190

**Limitaciones a reducciones:**
- Si los ingresos totales como consejero superan ciertos umbrales, NO se aplica la reducción general por rendimientos del trabajo (art. 20 LIRPF)
- Deben reconstruirse todos los rendimientos del trabajo para comprobar si se cumplen los requisitos de la reducción

## 5.11. Deportista de élite

**Rendimientos generales:**
- Los pagos por actuaciones, competiciones y entrenamientos son rendimientos del trabajo

**Reducción por rendimientos irregulares:**
- Si el deportista cobra premios o pagos plurianuales de forma irregular, puede aplicar la reducción por rendimientos irregulares del art. 18.2 LIRPF
- Requiere que los rendimientos de 2+ ejercicios anteriores sean inferiores al 75% del rendimiento del año actual

**Exención de premios (caso especial):**
- Los premios de la Administración por competiciones deportivas internacionales pueden estar parcialmente exentos conforme a art. 7.m LIRPF (exención limitada)
- No es una exención ilimitada

## 5.12. Sacerdote y religioso

**Ingresos como rendimiento del trabajo:**
- La asignación recibida del obispado/diócesis o del instituto religioso se considera rendimiento del trabajo
- Está incluida en los rendimientos del trabajo sujetos a impuesto

**Inclusión en Seguridad Social:**
- Están afiliados al Régimen General de la Seguridad Social (a través de la diócesis u organización religiosa)
- Las cotizaciones a la SS son deducibles como gastos del rendimiento

---

## 6.4. Cómo reconstruir el rendimiento inmobiliario desde datos crudos

**Documentos necesarios:**
- Contrato de arrendamiento
- Recibos de alquiler cobrado (o transferencias bancarias)
- Recibo del IBI (valor catastral y año de revisión)
- Extracto de hipoteca (desglose de intereses)
- Recibos de comunidad, seguro, reparaciones
- Referencia catastral del inmueble

**Procedimiento por cada inmueble arrendado:**
1. Ingresos íntegros = rentas anuales cobradas + repercutibles al inquilino
2. Gastos deducibles: intereses hipotecarios + IBI + comunidad + seguro + conservación + amortización (3% del mayor entre coste adquisición-suelo o valor catastral construcción) + saldos dudoso cobro
3. Rendimiento neto = ingresos - gastos (mínimo 0 para amortización)
4. Reducción 50% si es vivienda habitual del inquilino (60% o 90% en zonas tensionadas según requisitos)
5. Rendimiento neto reducido

**Inmuebles no arrendados:** imputación = 1,1% × valor catastral (si revisado después de 1994) o 2% × valor catastral (si no revisado)

---

## 7.3. Cómo reconstruir el rendimiento del capital mobiliario desde datos crudos

**Documentos necesarios:**
- Certificados bancarios de intereses e ingresos
- Liquidaciones de operaciones (compraventa de valores, fondos de inversión)
- Extractos de brokers/plataformas de inversión
- Confirmaciones de dividendos y participaciones
- Recibos de comisiones y gastos

**Procedimiento:**
1. Identificar todos los activos y operaciones (depósitos, bonos, acciones, fondos, seguros, criptomonedas)
2. Calcular intereses y dividendos brutos devengados/cobrados en el año
3. Sumar ganancias por venta de activos = precio venta - precio compra - comisiones
4. Sumar pérdidas por venta de activos (cifra negativa)
5. Sumar rendimientos de seguros de vida/rentas vitalicias
6. Gastos deducibles: comisiones custodia, corretaje, transferencias, cambio divisas
7. Base del ahorro = intereses + dividendos + ganancias netas - gastos
8. Separar ganancias patrimoniales (transmisión) de rendimientos (intereses/dividendos)
9. Rendimiento móvil = rendimiento neto para integrar en base ahorro

**Dato clave:** Las pérdidas patrimoniales de la base del ahorro solo compensan ganancias de la misma base, hasta 25% de rendimientos móviles. Arrastre a 4 años.

---

## 8.4. Agricultor y ganadero

**Régimen de tributación frecuente:**
Muchos agricultores y ganaderos tributan en **estimación objetiva (módulos)** con índices específicos agrícolas establecidos por la administración tributaria.

**Para los que tributan en estimación directa:**
- Las subvenciones agrícolas de la PAC (Política Agrícola Común) son ingresos computables y tributan como ingresos de la actividad
- Se incluyen en el cálculo del rendimiento neto

**Gastos deducibles específicos (aplicables en estimación directa):**
- Semillas, plantas de vivero y otros materiales de reproducción
- Fertilizantes, abonos, enmiendas del suelo
- Piensos para el ganado (alimentos concentrados, forrajes comprados)
- Combustible y energía (gasóleo agrícola, electricidad para explotación)
- Seguros agrarios (contra granizo, sequía, plagas, etc.)
- Tratamientos fitosanitarios y desinfectantes
- Herramientas y aperos menores
- Mantenimiento de máquinas agrícolas
- Riego y sistemas de riego
- Mano de obra estacional

**Retención sobre pagos a agricultores:**
- 2% para ganaderos y agricultores que tributan en módulos
- 1% para actividades agrícolas en estimación directa
- Aplicable cuando facturan a empresas de ciertos sectores

---

## 9.5. Cómo reconstruir ganancias y pérdidas patrimoniales desde datos crudos

**Documentos necesarios:**
- Contratos de compra y venta (inmuebles, acciones, fondos)
- Recibos y comprobantes de pago (con gastos de transacción)
- Liquidaciones de operaciones (broker, banco)
- Confirmaciones de transmisión (certificados de compra/venta)
- Documentación de mejoras y ampliaciones capitalizadas
- Certificados de retención (si fue practicada)

**Procedimiento por cada transmisión o ganancia:**
1. Valor de adquisición = precio compra + gastos transacción (notaría, registro, comisiones) + mejoras capitalizadas - amortizaciones aplicadas
2. Valor de transmisión = precio venta - gastos transmisión (comisiones, impuestos inherentes)
3. Ganancia/pérdida = valor transmisión - valor adquisición
4. Clasificar: ganancias/pérdidas patrimoniales (venta elementos) vs. ingresos (premios, compensaciones)
5. Si es elemento de la base ahorro: integrar en base del ahorro. Si es base general: integrar en base general.
6. Aplicar compensaciones (pérdidas con ganancias, con 25% rendimientos móviles)
7. Aplicar arrastre de pérdidas previas (máx. 4 años)
8. Aplicar exenciones (vivienda habitual, business angels, reinversión)
9. Resultado = ganancia/pérdida neta integrable

**Dato clave:** Las ganancias por transmisión de vivienda habitual tributada después de 2015 están completamente exentas para mayores de 65 años. Reinversión en nueva vivienda exenta sin límite dentro de 2 años.

## 9.6. Heredero que vende bienes heredados

**Valor de adquisición:**
- El valor de adquisición del bien heredado es el valor declarado en el Impuesto sobre Sucesiones (no el valor original del bien a fecha del fallecimiento del causante)
- Excepto: en ciertos casos, se usa el valor de la tributación del Impuesto de Sucesiones al momento de la herencia

**Fecha de adquisición:**
- La fecha de adquisición del bien heredado es la **fecha del fallecimiento del causante** (no la fecha de liquidación del Impuesto de Sucesiones, ni la fecha de la transmisión posterior)
- Esta fecha es determinante para calcular el período de tenencia del bien

**Exención por reinversión en vivienda habitual (NO aplicable):**
- Si el bien heredado era la vivienda habitual del fallecido y el heredero la vende dentro de los 2 años siguientes al fallecimiento, **NO hay exención por reinversión**
- Motivo: la vivienda habitual del causante NO es vivienda habitual del heredero; por tanto, no cumple los requisitos de exención
- Sí puede aplicarse exención de transmisión si el heredero es mayor de 65 años y cumple otros requisitos

**Coeficientes de abatimiento (DT 9ª LIRPF):**
- Se aplican SOLO si el bien fue **adquirido por el fallecido antes del 31/12/1994**
- Si el causante adquirió el bien después del 31/12/1994, NO se aplican coeficientes de abatimiento
- El porcentaje reductor es el 11,11% por cada año de permanencia que exceda de 2, redondeado por exceso, computado desde la fecha de adquisición hasta el 31/12/1996 (no hasta la transmisión)
- Límite conjunto: 400.000 euros de valor de transmisión acumulado por contribuyente (todos los elementos acogidos al régimen transitorio)

---

## 11. DEDUCCIONES ESTATALES DE LA CUOTA

### 11.1. Deducción por inversión en vivienda habitual (regimen transitorio)

Solo aplicable a contribuyentes que cumplan TODAS estas condiciones:
- Compraron/empezaron a pagar la vivienda antes del 01/01/2013 y todavia tienen deuda pendiente
- Han venido deduciendo esta deduccion en ejercicios anteriores
- La vivienda sigue siendo su vivienda habitual (vivienda permanente del nucleo familiar)
- Mantienen la obligacion de pagar capital e intereses

Cuantias de la deduccion:
- Porcentaje: 15% (7,5% estatal + 7,5% autonomico) sobre los gastos deducibles (intereses de hipoteca, seguros, comisiones...)
- Base maxima de deduccion: 9.040 euros anuales
- Deduccion maxima anual: 1.356 euros (15% de 9.040)
- Sin efectos en el futuro para compras posteriores a 31/12/2012

### 11.2. Deducción por inversión en empresas de nueva o reciente creación

- Porcentaje: 50% de las cantidades invertidas
- Base maxima: 100.000 euros anuales
- Deduccion maxima: 50.000 euros
- Requisitos: entidad creada en los ultimos 5 años (7 para ciertos sectores), fondos propios no superiores a 400.000 euros, participacion no superior al 40%

### 11.3. Deducciones por donativos y donaciones

Requisito previo: Entidades deducibles deben estar inscritas en el registro de entidades de la AEAT.

| Tipo de donativo | Base hasta 250 euros | Resto | Limite anual |
|---|---|---|---|
| Entidades beneficiarias de la Ley 49/2002 (ONGs, etc.) | 80% | 40% | 10% de base liquidable |
| Si donacion recurrente (3+ años consecutivos a misma entidad) | 80% | 45% | 10% de base liquidable |
| Actividades prioritarias de mecenazgo (cultura, investigacion, etc.) | 80% | 45% (50% si recurrente) | 15% de base liquidable |
| Partidos politicos, sindicatos, fundaciones publicas | 80% | 40% | 10% de base liquidable |

Notas:
- La base de la deduccion se calcula sumando todos los donativos realizados en el ano
- El porcentaje se aplica sobre el total o sobre tramos (hasta 250 euros y resto)
- Si se supera el limite anual, el exceso puede arrastrase a ejercicios siguientes (máximo 5 años)
- Requiere documentacion de la entidad receptora

**Quien deduce un donativo: regla del donante nominal**

A diferencia de las deducciones por gastos (sanidad, educacion, alquiler, deporte, etc.), donde la regla general es "quien paga efectivamente deduce" y los pagos desde cuentas conjuntas se presumen al 50/50, los donativos siguen una regla distinta:

**El donante es la persona que figura nominalmente en el certificado emitido por la entidad receptora**, independientemente del origen de los fondos. La entidad receptora informa a la AEAT del donativo via Modelo 182 identificando al donante por NIF, y la AEAT cruza ese NIF con la declaracion del IRPF.

Consecuencias practicas:
- Si una persona realiza una donacion de 200 EUR a su nombre desde una cuenta conjunta con su pareja/conyuge, solo el donante nominal puede deducir el 80% (= 160 EUR) en su IRPF. La pareja no puede prorratear el 50% en su propia declaracion.
- Si una pareja quiere que ambos deduzcan, deben realizar DOS donaciones SEPARADAS (cada uno con su propio certificado a su nombre y NIF), no una unica donacion que luego se intenta repartir.
- Si una donacion conjunta de matrimonios en regimen de gananciales lleva ambos nombres en el certificado (formato menos comun), entonces si se puede prorratear 50/50 entre los dos conyuges.

Esta regla aplica igualmente a los donativos a entidades de la Ley 49/2002, partidos politicos, sindicatos, y mecenazgo. El criterio rector es siempre la identidad del donante segun el documento informativo.

Fuentes:
- Art. 24 Ley 49/2002 (justificacion documental de los donativos): https://www.boe.es/buscar/act.php?id=BOE-A-2002-25039&p=20250712&tn=1#a24
- Modelo 182 (declaracion informativa de donativos por las entidades): https://sede.agenciatributaria.gob.es/Sede/procedimientoini/G414.shtml
- DGT V0598-19 sobre donativos desde cuentas mancomunadas (criterio del donante nominal frente a origen de fondos)

### 11.4. Deducción por rentas obtenidas en Ceuta o Melilla

- 60% de la parte de la cuota integra correspondiente a rentas obtenidas en Ceuta o Melilla
- Residentes de 3+ años: extension a todas las rentas (con condiciones)

### 11.5. Deducción por maternidad (articulo 25 y ss. LIRPF)

**Base de deduccion:**
- 1.200 euros anuales por cada hijo menor de 3 años (a 31 de diciembre del ano de la deduccion)
- Se deducen de la cuota (no reduce la base imponible)

**Incremento por gastos de custodia:**
- Hasta 1.000 euros adicionales por gastos de custodia en guarderias, escuelas infantiles o centros autorizados
- Documentacion: recibos y certificado de centro autorizado
- No se puede duplicar si hay obligacion de alimentos/custodia compartida

**Requisitos para acceder:**
- Madre trabajadora (por cuenta ajena o propia)
- Debe estar dada de alta en la Seguridad Social
- Guarda y custodia del hijo (minimo de 3 meses durante el ano)
- No tener otras deducciones por el mismo hijo (excluidos incrementos custodia)
- Compatible con prestaciones de maternidad/paternidad

**Cobro anticipado:**
- Posibilidad de solicitar abono anticipado de 100 euros/mes (1.200 euros/ano base, hasta 1.000 adicionales)
- Solicitud en empleador o autonomo en declaracion
- No reduce el importe de la deduccion en la declaracion del IRPF

### 11.6. Deducciones por familia numerosa o personas con discapacidad a cargo

| Concepto | Cuantia anual | Requisitos adicionales |
|---|---|---|
| Familia numerosa categoria general (3+ hijos) | 1.200 euros | Hijos menores o incapacitados judicialmente; certificado familia numerosa |
| Familia numerosa categoria especial (5+ hijos) | 2.400 euros | Hijos menores o incapacitados judicialmente; certificado familia numerosa |
| Por cada hijo adicional sobre el minimo de la categoria | +600 euros | Por encima del 3 (general) o 5 (especial) |
| Descendiente con discapacidad a cargo (discapacidad >= 33%) | 1.200 euros | Convivencia y dependencia economica |
| Ascendiente con discapacidad a cargo (discapacidad >= 33%) | 1.200 euros | Convivencia, mayores de 65 años o discapacidad >= 33%, dependencia economica |
| Familia monoparental con 2 hijos sin derecho a anualidades por alimentos | 1.200 euros | Custodia unilateral sin anualidades fijadas judicialmente |
| Conyuge no separado legalmente con discapacidad (discapacidad >= 33%) | 1.200 euros | Convivencia y dependencia economica |

- Compatibles entre si (se pueden aplicar varias simultaneamente)
- Cobro anticipado: 100 euros/mes por cada deduccion (solicitar a la empresa o para autonomos en la declaracion)

### 11.7. Deducciones por eficiencia energética (temporales hasta 31/12/2025)

**Deduccion sobre gastos realizados desde 01/01/2023 hasta 31/12/2025**

| Tipo de mejora energetica | Porcentaje | Base maxima anual | Requisitos |
|---|---|---|---|
| Reducción demanda calefaccion/refrigeracion (>= 7%) | 20% | 5.000 euros | Certificado energetico previo y posterior, mejoras aislamiento |
| Reducción consumo energia primaria no renovable (>= 30%) | 40% | 7.500 euros | Certificado energetico previo y posterior, cambio sistemas calefaccion/A.A. |
| Rehabilitación energética edificios residenciales completa (>= 30% consumo o letra A-B) | 60% | 15.000 euros (limite acumulado 5 años) | Certificado energetico previo y posterior, mejoras multiples |
| Mejoras aislamiento térmico (ventanas, puertas, envolvente...) | 20%-40% segun mejora | Incluido en base maxima | Certificado energetico, especificacion tecnica |
| Cambio sistemas energías renovables (placas solares, bomba calor...) | 40%-60% segun sistema | Incluido en base maxima | Certificado tecnico del sistema |

**Requisitos generales:**
- Inmueble situado en España destinado a habitacion del contribuyente
- Gasto realizado desde 01/01/2023
- Certificado de eficiencia energetica antes y despues de obras (expedido por tecnico competente)
- Facturas desglosadas de obras y suministros
- Compatible con otras deducciones por vivienda

### 11.8. Deducciones por vehículos electricos y puntos de recarga (hasta 31/12/2025)

**Deduccion sobre gastos realizados desde 01/01/2023 hasta 31/12/2025**

| Concepto | Porcentaje deduccion | Base maxima anual | Requisitos |
|---|---|---|---|
| Adquisicion vehículo eléctrico enchufable (PHEV) | 15% | 20.000 euros (3.000 euros maximo) | Matriculado en España, potencia <= 300 kW |
| Adquisición vehículo de pila de combustible (hidrogeno) | 15% | 20.000 euros (3.000 euros maximo) | Matriculado en España |
| Instalacion punto de recarga en vivienda propiedad del contribuyente | 15% | 4.000 euros (600 euros maximo) | Punto conectado a red electrica, instalador certificado |
| Instalacion punto recarga en garaje comun de comunidad propietarios | 15% | 4.000 euros | Instalador certificado, acuerdo junta propietarios |

**Requisitos generales:**
- Gasto realizado desde 01/01/2023
- Vehiculo o punto de recarga situado en territorio español
- Factura desglosada del gasto
- Compatible con otras deducciones por vivienda
- No compatible con subvenciones publicas para la misma finalidad (se elige una u otra)

### 11.9. Deducción por residencia habitual en La Palma (2022-2025)

- 60% de la cuota integra que proporcionalmente corresponda a rentas obtenidas en La Palma

### 11.10. Deducción por doble imposición internacional

- Se deduce la menor de: impuesto pagado en el extranjero o cuota que corresponderia en Espana por esas rentas

---

## 13. OBLIGACIONES FORMALES Y PLAZOS

Fuente: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c01-campana-declaracion-renta/servicios-ayuda-campana-renta.html

### 13.0. Modelos de declaracion

**Modelo 100 - Declaracion del IRPF:** Declaracion anual del Impuesto sobre la Renta de las Personas Fisicas. Es el modelo principal para todos los contribuyentes del IRPF en regimen comun.

**Modelo 102 - Segundo plazo IRPF:** Documento para el ingreso del segundo plazo (40%) cuando se fracciona el pago. Solo es necesario si no se domicilia el segundo plazo.

**Modelo 714 - Impuesto sobre el Patrimonio:** Declaracion anual del Impuesto sobre el Patrimonio. Obligatoria si la cuota resulta a ingresar o si el valor de los bienes y derechos supera 2.000.000 euros. Presentacion: 8 de abril a 30 de junio de 2026, exclusivamente por medios electronicos.

**Modelo 720 - Bienes en el extranjero:** Declaracion informativa sobre cuentas, valores e inmuebles en el extranjero cuando superen 50.000 euros en alguna de las tres categorias. Plazo: 1 de enero a 31 de marzo.

**Modelo 721 - Criptomonedas en el extranjero:** Declaracion informativa sobre monedas virtuales situadas en el extranjero cuando el saldo a 31 de diciembre supere 50.000 euros. Plazo: 1 de enero a 31 de marzo.

**Modelo 149 - Regimen impatriados:** Comunicacion de opcion, renuncia o exclusion del regimen especial de trabajadores desplazados (Ley Beckham). Plazo: 6 meses desde alta en Seguridad Social.

**Modelo 151 - Declaracion impatriados:** Declaracion anual especifica para acogidos al regimen de impatriados. Sustituye al Modelo 100.

**Modelo 184 - Atribucion de rentas:** Declaracion informativa anual de entidades en regimen de atribucion de rentas (comunidades de bienes, herencias yacentes, sociedades civiles). Plazo: enero del año siguiente.

### Campaña Renta 2025

Fuente: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c01-campana-declaracion-renta.html

| Concepto | Fecha |
|---|---|
| Inicio de campaña (Renta WEB) | 8 de abril de 2026 |
| Fin plazo presentacion (general) | 30 de junio de 2026 |
| Fin plazo con domiciliacion bancaria | 25 de junio de 2026 |
| Servicio "Le Llamamos" - solicitud cita | Desde 29 de abril de 2026 |
| Servicio "Le Llamamos" - atencion efectiva | Desde 6 de mayo de 2026 |
| Atencion presencial - solicitud cita | Desde 29 de mayo de 2026 |
| Atencion presencial - inicio | Desde 1 de junio de 2026 |
| Ultima solicitud de cita (telefono/presencial) | 29 de junio de 2026 |
| Segundo plazo de pago (modelo 102) | Hasta 5 de noviembre de 2026 |
| Domiciliacion del segundo plazo | Hasta 30 de septiembre de 2026 |

### Formas de presentación

**1. Renta WEB (por Internet):**
Herramienta principal de la AEAT para confeccionar y presentar la declaracion. Permite obtener el borrador, modificarlo y presentarlo electronicamente. Accesible desde el 8 de abril en la Sede Electronica.

**2. Renta Directa (presentacion instantanea):**
Novedad 2025. Permite presentar la declaracion en un solo clic sin necesidad de revisar el borrador. Disponible para 9 millones de contribuyentes elegibles (duplicacion respecto a 2024). Incluye contribuyentes con hipotecas, nuevos declarantes y contribuyentes con deducciones autonomicas.

**3. APP movil AEAT:**
Aplicacion movil gratuita de la AEAT. Permite acceder a los servicios de Renta WEB desde dispositivos moviles. Al confirmar borrador por APP, el pago debe realizarse necesariamente mediante domiciliacion bancaria de ambos plazos.

**4. Telefonica - Plan "Le Llamamos":**
Confeccion y presentacion asistida por telefono. Citas disponibles desde 29 de abril, atencion desde 6 de mayo. Telefonos: 91 553 00 71 / 901 22 33 44 (personal, 9-19h), 91 535 73 26 / 901 12 12 24 (automatico, 24h).

**5. Presencial en oficinas:**
Con cita previa. Disponible desde 1 de junio en oficinas de la AEAT y de las comunidades autonomas. Citas desde 29 de mayo.

### Medios de identificacion electronica

**Certificado digital / DNI electronico:** Firma electronica instalada en el navegador o DNIe. Permite acceso completo a todos los servicios.

**Cl@ve Movil:** Sistema de identificacion mediante la APP Cl@ve (escaneo de codigo QR). No requiere instalar certificados.

**Numero de referencia (RENO):** Referencia unica de 6 caracteres. Se obtiene con NIF + dato del ejercicio anterior (casilla 505 de la declaracion 2024, o IBAN en caso de no declarantes). Valida para la campaña en curso.

**Telefono de informacion tributaria:** 91 554 87 70, lunes a viernes de 9 a 19 horas.

### Fraccionamiento del pago (60/40)

El contribuyente puede fraccionar el pago en dos plazos sin intereses ni recargo, siempre que:
- La declaracion se presente dentro del plazo reglamentario (hasta 30 de junio)
- No sea una autoliquidacion complementaria

**Primer plazo:** 60% del importe, al momento de presentar la declaracion.

**Segundo plazo:** 40% restante, hasta el 5 de noviembre de 2026. Se puede:
- Domiciliar (mismo banco que el primer plazo): hasta 30 de septiembre de 2026
- Pagar mediante modelo 102 en entidad colaboradora o electronicamente

**Incumplimiento:** La falta de pago del 60% inicial determina el inicio del periodo ejecutivo por la totalidad del importe de la deuda.

**Caso especial APP movil:** Cuando se confirma el borrador mediante la aplicacion movil, el pago debe realizarse necesariamente mediante domiciliacion bancaria de ambos plazos.

### Rectificacion de autoliquidaciones

Desde el ejercicio 2024, la autoliquidacion rectificativa es el sistema unico para corregir declaraciones del IRPF (Orden HAC/242/2025). Sustituye al antiguo sistema dual de complementarias (a ingresar mas) y solicitudes de rectificacion (a devolver mas).

Fuente: https://sede.agenciatributaria.gob.es/Sede/irpf/campana-renta/modificacion-declaracion-renta-2025-presentada/resultado-autoliquidacion-rectificativa-ingresar-menor-importe.html

**Procedimiento:** Se presenta una nueva declaracion marcando la casilla 103 (autoliquidacion rectificativa) en Renta WEB. La nueva declaracion sustituye a la anterior.

**Plazo:** Se puede presentar en cualquier momento antes de que prescriba el derecho de la Administracion a determinar la deuda tributaria (4 años desde el final del plazo de presentacion voluntaria). Si se presenta fuera del plazo voluntario, se considera extemporanea (con recargos).

**Resultado a ingresar mas:** Si la rectificacion resulta en mayor pago, el contribuyente debe ingresar la diferencia. Se aplican recargos por extemporaneidad si se presenta fuera de plazo.

**Resultado a devolver:** Si la rectificacion resulta en menor pago o mayor devolucion, la Administracion procedera a devolver la diferencia.

**Declaraciones complementarias:** Siguen existiendo para ejercicios anteriores a 2024. Se presentan cuando se detectan errores que resultan en un mayor pago al fisco.

### Obligaciones de conservacion documental

Los contribuyentes deben conservar los justificantes y documentos acreditativos de las operaciones, rentas, gastos, ingresos, reducciones y deducciones declaradas, durante el plazo de prescripcion:

- **Plazo fiscal general:** 4 años desde el final del plazo de presentacion
- **Plazo mercantil (autonomos y empresarios):** 6 años a partir del ultimo asiento contable
- **Ejercicios con perdidas pendientes de compensar:** La documentacion debe conservarse durante todo el periodo en que las perdidas puedan compensarse (hasta 4 años adicionales)
- **Recomendacion practica:** Conservar toda documentacion fiscal durante al menos 6 años

**Documentos a conservar:** Certificados de retenciones, nominas, contratos de alquiler, escrituras de compraventa, facturas de gastos deducibles, certificados bancarios, justificantes de donativos, extractos de operaciones de inversion, recibos de IBI, certificados de aportaciones a planes de pensiones, y cualquier otro justificante de las partidas declaradas.

### 13.1. Flujo de cálculo de la cuota diferencial: conciliación de retenciones y pagos a cuenta

La cuota diferencial a ingresar o devolver se obtiene restando de la cuota líquida total todas las retenciones practicadas y pagos a cuenta efectuados durante el año:

**Cuota diferencial = Cuota líquida total
  - Retenciones del trabajo (certificados modelo 10T)
  - Retenciones del capital mobiliario (en origen del banco/broker)
  - Retenciones del capital inmobiliario (si aplica, en origen)
  - Retenciones por actividades económicas (si aplica, sobre facturas emitidas)
  - Pagos fraccionados modelo 130 (trimestral o anual)
  - Pagos fraccionados modelo 131 (para ciertos profesionales)
  - Retenciones sobre ganancias patrimoniales (si fueron retenidas)
  - Ingresos a cuenta por rendimientos en especie
  - Deducción por maternidad anticipada (si se cobró mensualmente)
  - Deducciones por familia numerosa/discapacidad anticipadas (si se cobraron adelantadas)**

**Si el resultado es POSITIVO:** A ingresar por el contribuyente
**Si el resultado es NEGATIVO:** A devolver por la Hacienda Pública

### 13.2. Ejemplo 1: Asalariado con intereses bancarios

**Situacion personal:**
- Soltero, sin descendientes
- Edad: 42 años, residente en Madrid
- Año: 2025

**Rendimientos del trabajo:**
- Salario bruto anual: 35.000 EUR
- Retención IRPF practicada: 5.250 EUR (15%)
- Cotizaciones SS del trabajador: 2.240 EUR (6,4%)

**Rendimientos del capital mobiliario:**
- Intereses bancarios devengados: 500 EUR
- Retención IRPF: 95 EUR (19%)

**Calculo paso a paso:**

1. **Rendimiento neto del trabajo:**
   - Ingresos íntegros: 35.000 EUR
   - Gastos deducibles (SS): 2.240 EUR
   - Rendimiento neto: 35.000 - 2.240 = 32.760 EUR

2. **Reducción por rendimientos del trabajo (§5.2):**
   - RNT = 32.760 EUR (> 19.747,50 EUR)
   - Reducción aplicable: 0 EUR (sin derecho)
   - Rendimiento neto reducido: 32.760 EUR

3. **Base imponible general:**
   - Rendimiento neto reducido trabajo: 32.760 EUR
   - Mínimo personal (contribuyente): 5.550 EUR
   - Base liquidable general: 32.760 - 5.550 = 27.210 EUR

4. **Base imponible del ahorro:**
   - Intereses bancarios: 500 EUR
   - Gastos deducibles: 0 EUR
   - Base liquidable ahorro: 500 EUR

5. **Cuota íntegra estatal (50% aplicable):**
   - Escala general sobre 27.210 EUR (50%):
     * Hasta 12.450 EUR × 9,50% = 1.182,75 EUR
     * Siguiente 14.760 EUR × 12% = 1.771,20 EUR
     * Cuota integra general (50%): 2.953,95 EUR
     * Cuota estatal general (50% del 50%): 1.476,98 EUR
   
   - Escala ahorro sobre 500 EUR (50%):
     * 500 EUR × 9,50% = 47,50 EUR
     * Cuota integra ahorro (50%): 47,50 EUR
     * Cuota estatal ahorro (50% del 50%): 23,75 EUR

6. **Cuota íntegra autonómica (Madrid, 50% aplicable):**
   - General: 1.476,98 EUR
   - Ahorro: 23,75 EUR

7. **Cuota líquida total (antes de deducciones):**
   - 1.476,98 + 23,75 + 1.476,98 + 23,75 = 3.001,46 EUR

8. **Cuota diferencial (a ingresar/devolver):**
   - Cuota líquida: 3.001,46 EUR
   - Retención del trabajo: 5.250 EUR
   - Retención del ahorro: 95 EUR
   - Total retenciones: 5.345 EUR
   - Diferencial: 3.001,46 - 5.345 = -2.343,54 EUR
   
   **Resultado: A DEVOLVER 2.343,54 EUR**

### 13.3. Ejemplo 2: Autónomo profesional con estimación directa simplificada

**Situacion personal:**
- Profesional sanitario (médico): consultor independiente
- Casado, 0 descendientes
- Conyuge sin rentas
- Edad: 50 años, residente en Barcelona
- Año: 2025

**Actividad económica:**
- Facturación anual: 40.000 EUR
- Retención practicada por clientes (profesionales): 6.000 EUR (15%)
- RETA mensual: 300 EUR × 12 = 3.600 EUR (pagado)
- Gastos documentados: 8.000 EUR (alquiler despacho, suministros, seguros)
- Gasto difícil justificación: 5% × (40.000 - 8.000) = 1.600 EUR (el 7% fue medida temporal solo del ejercicio 2023; art. 30 RIRPF / AEAT Manual Práctico Renta 2025, c07)

**Calculo paso a paso:**

1. **Rendimiento neto de actividad económica:**
   - Facturación íntegra: 40.000 EUR
   - Gastos documentados: 8.000 EUR
   - Gastos difícil justificación (5%, no alcanza el máx. de 2.000): 1.600 EUR
   - Rendimiento neto: 40.000 - 8.000 - 1.600 = 30.400 EUR

2. **Reduccion por inicio actividad (Novedad 2025):**
   - ¿Es el primer año?: NO (asumimos año 5 de actividad)
   - Reducción aplicable: 0 EUR

3. **Rendimiento neto reducido: 30.400 EUR**

4. **Base liquidable general:**
   - Rendimiento actividad: 30.400 EUR
   - Cotizaciones SS (RETA): 3.600 EUR (deducible)
   - Mínimo personal cónyuge (biparental): 3.400 EUR
   - Mínimo del contribuyente: 5.550 EUR
   - Base liquidable: 30.400 - 3.600 - 3.400 - 5.550 = 17.850 EUR

5. **Cuota íntegra estatal (50%):**
   - Hasta 12.450 EUR × 9,50% = 1.182,75 EUR
   - Siguiente 5.400 EUR × 12% = 648 EUR
   - Cuota integra: 1.830,75 EUR
   - Cuota estatal (50%): 915,38 EUR

6. **Cuota íntegra autonómica (Catalunya, 50%):**
   - Mismos tramos: 915,38 EUR

7. **Cuota líquida total:**
   - 915,38 + 915,38 = 1.830,75 EUR

8. **Cuota diferencial:**
   - Cuota líquida: 1.830,75 EUR
   - Retenciones por facturas: 6.000 EUR
   - Pagos fraccionados 130 (asumiendo 0 en este año): 0 EUR
   - Total retenciones/pagos: 6.000 EUR
   - Diferencial: 1.830,75 - 6.000 = -4.169,25 EUR
   
   **Resultado: A DEVOLVER 4.169,25 EUR**

**Nota sobre pagos fraccionados:** Si hubiera realizado pagos fraccionados (modelo 130) por ejemplo 300 EUR/trimestre = 1.200 EUR/año, la cuota diferencial sería: 1.830,75 - 6.000 - 1.200 = -5.369,25 EUR (mayor devolución).

### 13.4. Ejemplo 3: Arrendador con nomina

**Situacion personal:**
- Casado, 1 hijo de 8 años
- Ambos cónyuges trabajan (pero solo uno declara inmobiliaria)
- Edad: 55 años, residente en Valencia
- Año: 2025

**Rendimientos del trabajo (cónyuge contribuyente):**
- Salario bruto: 28.000 EUR
- Retención IRPF: 3.920 EUR (14%)
- Cotizaciones SS: 1.792 EUR (6,4%)

**Rendimientos del capital inmobiliario:**
- Inmueble arrendado: piso 2 habitaciones
- Alquiler cobrado: 12.000 EUR/año (1.000 EUR/mes)
- IBI: 400 EUR
- Comunidad: 900 EUR/año
- Intereses hipoteca: 1.200 EUR/año (resto es amortización capital)
- Amortización 3%: 1.500 EUR (valor catastral construcción base)
- Seguros: 150 EUR
- Valor catastral: 50.000 EUR (revisado en 2015)

**Calculo paso a paso:**

1. **Rendimiento neto del trabajo:**
   - Ingresos íntegros: 28.000 EUR
   - Gastos deducibles SS: 1.792 EUR
   - Rendimiento neto: 28.000 - 1.792 = 26.208 EUR

2. **Reduccion trabajo:**
   - RNT = 26.208 EUR (> 19.747,50)
   - Reducción: 0 EUR

3. **Rendimiento neto reducido trabajo: 26.208 EUR**

4. **Rendimiento neto del capital inmobiliario:**
   - Ingresos: 12.000 EUR
   - IBI: 400 EUR
   - Comunidad: 900 EUR
   - Intereses hipoteca: 1.200 EUR
   - Amortización (3%): 1.500 EUR
   - Seguros: 150 EUR
   - Gastos totales: 400 + 900 + 1.200 + 1.500 + 150 = 4.150 EUR
   - Rendimiento neto: 12.000 - 4.150 = 7.850 EUR

5. **Reduccion arrendamiento vivienda (§6.2):**
   - Contrato posterior a 26/05/2023: SÍ
   - ¿Zona tensionada?: NO (Valencia no está declarada en 2025)
   - ¿Rehabilitada?: NO
   - Reducción aplicable: 50%
   - Rendimiento reducido: 7.850 × 50% = 3.925 EUR

6. **Base liquidable general:**
   - Rendimiento trabajo: 26.208 EUR
   - Rendimiento inmobiliario reducido: 3.925 EUR
   - Mínimo descendiente (1er hijo): 2.400 EUR
   - Mínimo personal: 5.550 EUR
   - Mínimo biparental: 3.400 EUR
   - Base liquidable: 26.208 + 3.925 - 2.400 - 5.550 - 3.400 = 18.783 EUR

7. **Cuota íntegra estatal (50%):**
   - Hasta 12.450 EUR × 9,50% = 1.182,75 EUR
   - Siguiente 6.333 EUR × 12% = 759,96 EUR
   - Cuota integra: 1.942,71 EUR
   - Cuota estatal (50%): 971,36 EUR

8. **Cuota íntegra autonómica (Comunitat Valenciana, 50%):**
   - Mismos tramos: 971,36 EUR

9. **Cuota líquida total:**
   - 971,36 + 971,36 = 1.942,72 EUR

10. **Cuota diferencial:**
    - Cuota líquida: 1.942,72 EUR
    - Retención del trabajo: 3.920 EUR
    - Retención del ahorro: 0 EUR
    - Total retenciones: 3.920 EUR
    - Diferencial: 1.942,72 - 3.920 = -1.977,28 EUR
    
    **Resultado: A DEVOLVER 1.977,28 EUR**

**Nota adicional:** Si hubiera descendientes con discapacidad >= 33% o si la vivienda arrendada fuera de protección oficial, la reducción sería mayor (60% o 90%) y la devolución aumentaría.

---

## FUENTES OFICIALES

- AEAT Manual Practico Renta 2025: https://sede.agenciatributaria.gob.es/Sede/Ayuda/25Manual/100.html
- AEAT Deducciones generales: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c16-deducciones-generales-cuota/introduccion/deducciones-generales-autonomicas-aplicables.html
- BOE Orden HAC/277/2026 (modelos declaracion Renta 2025): https://www.boe.es/buscar/act.php?id=BOE-A-2026-7041
- AEAT Gravamen estatal: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025/c15-calculo-impuesto-determinacion-cuotas-integras/gravamen-base-liquidable-general/gravamen-estatal.html
