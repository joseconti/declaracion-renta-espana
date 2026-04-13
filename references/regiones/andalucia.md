# IRPF 2025 - Comunidad Autonoma de Andalucia

Tramo autonomico del IRPF 2025 aplicable a los contribuyentes con residencia habitual en Andalucia a 31/12/2025. Incluye escala autonomica general, escala del ahorro, minimos autonomicos y deducciones autonomicas.

Fuentes oficiales:
- Manual Practico Renta 2025, Parte 1 (AEAT), capitulos 14 y 15: https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025/ManualRenta2025Parte1_es_es.pdf
- Manual Practico Renta 2025, Parte 2: https://sede.agenciatributaria.gob.es/static_files/Sede/Biblioteca/Manual/Practicos/IRPF/IRPF-2025-Deducciones-autonomicas/ManualRenta2025Parte2_es_es.pdf
- Ley 5/2021, de 20 de octubre, de Tributos Cedidos de la Comunidad Autonoma de Andalucia

---

## ESCALA AUTONOMICA GENERAL 2025

Normativa: art. 23 Ley 5/2021, de 20 de octubre, de Tributos Cedidos de la Comunidad Autonoma de Andalucia.

| Base liquidable hasta (euros) | Cuota integra (euros) | Resto base hasta (euros) | Tipo aplicable (%) |
|---|---|---|---|
| 0,00 | 0,00 | 13.000,00 | 9,50 |
| 13.000,00 | 1.235,00 | 8.100,00 | 12,00 |
| 21.100,00 | 2.207,00 | 14.100,00 | 15,00 |
| 35.200,00 | 4.322,00 | 24.800,00 | 18,50 |
| 60.000,00 | 8.910,00 | En adelante | 22,50 |

**Tipo marginal maximo autonomico: 22,50%**.

**Tipo marginal maximo total (estatal + autonomico):** 22,50% + 24,50% = **47,00%** para rentas superiores a 300.000 EUR.

Andalucia ha mantenido una escala deflactada respecto de la estatal (primer tramo hasta 13.000 EUR frente a 12.450 EUR estatal).

---

## ESCALA AUTONOMICA DEL AHORRO 2025

Identica a la estatal (art. 76 LIRPF). Ver `nacional.md §3`.

---

## MINIMO PERSONAL Y FAMILIAR AUTONOMICO 2025

Normativa: art. 23 bis Ley 5/2021.

Andalucia ha aprobado importes del minimo personal y familiar **distintos de los estatales**. Los contribuyentes residentes en Andalucia deben aplicar estos importes a efectos del gravamen autonomico (Cuota 4 del flujo de `nacional.md §13.1`); a efectos del gravamen estatal (Cuota 3) se aplican los estatales de `nacional.md §4`.

### Minimo del contribuyente

| Concepto | Cuantia anual (euros) |
|---|---|
| General | 5.790 |
| Incremento mayores de 65 anos | +1.200 |
| Incremento adicional mayores de 75 anos | +1.460 |

### Minimo por descendientes

| Concepto | Cuantia anual (euros) |
|---|---|
| Primer descendiente | 2.510 |
| Segundo descendiente | 2.820 |
| Tercer descendiente | 4.170 |
| Cuarto y siguientes | 4.700 |
| Incremento por descendiente menor de 3 anos | +2.920 |

### Minimo por ascendientes

| Concepto | Cuantia anual (euros) |
|---|---|
| Por ascendiente > 65 anos o con discapacidad | 1.200 |
| Incremento por ascendiente > 75 anos | +1.460 |

### Minimo por discapacidad

| Grado | Cuantia anual (euros) |
|---|---|
| 33% - 65% | 3.130 |
| >= 65% | 9.390 |
| Incremento por ayuda de terceros o movilidad reducida | +3.130 |

---

## DEDUCCIONES

### 1. Por inversion en vivienda habitual protegida y para personas jovenes

- **Porcentaje:** 6% de las cantidades satisfechas para adquisicion o rehabilitacion
- **Base maxima:** 9.040 euros
- **Requisitos:**
  - La vivienda debe tener calificacion de protegida segun normativa de Andalucia, O
  - El adquirente es menor de 35 anos (al menos uno de los cónyuges o padre/madre en familia monoparental), O
  - La suma de bases imponibles general y ahorro no supera 25.000 euros (individual) o 30.000 euros (conjunta)
  - Concepto de vivienda habitual segun artículos 54.1, 54.2 y 55.2.c del Reglamento IRPF vigente a 31-12-2012
- **Incompatibilidades:** Compatible con deduccion por alquiler en el mismo ejercicio
- **Novedad 2025:** Mantiene requisitos de edicion anterior

### 2. Por cantidades invertidas en alquiler de vivienda habitual

- **Porcentaje:** 15% de las cantidades pagadas por alquiler
- **Limite maximo:** 1.200 euros anuales (1.500 euros si tiene discapacidad reconocida)
- **Base imponible:** No supera 25.000 euros (individual) o 30.000 euros (conjunta)
- **Requisitos:**
  - Contribuyente menor de 35 anos, O
  - Mayor de 65 anos, O
  - Victima de violencia domestica, terrorismo o persona afectada
  - En tributacion conjunta, alguno de los requisitos debe cumplirlo al menos uno de los cónyuges o padre/madre
  - Debe identificar al arrendador con su NIF
  - Ser el titular del contrato de arrendamiento
- **Consideraciones:** En caso de matrimonio, solo el cónyuge firmante puede deducir. Con multiples contribuyentes con derecho, cada uno aplica sobre sus cantidades. En tributacion conjunta, limite maximo de 1.200 euros por declaracion (1.500 si alguno tiene discapacidad)
- **Incompatibilidades:** Ninguna con otras deducciones de vivienda si ambas cumplen requisitos

### 3. Por nacimiento, adopcion de hijos o acogimiento familiar de menores

- **Cuantia general:** 200 euros por cada hijo nacido, adoptado o menor en acogimiento
- **Cuantia aumentada:** 400 euros por hijo en municipios con problemas de despoblacion (menos de 3.000 habitantes)
- **Incremento por partos/adopciones multiples:** 200 euros adicionales por cada hijo extra
- **Requisitos:**
  - Aplicable al nacimiento/adopcion/acogimiento en el periodo impositivo
  - Para acogimiento: convivencia minima de 90 dias durante el periodo impositivo
  - Para acogimiento: no haber recibido ayudas de la Administracion de Andalucia vinculadas
  - Convivencia no es requisito obligatorio para nacimiento/adopcion (puede aplicarse aunque haya separacion/divorcio)
  - Fallecimiento posterior del hijo en el mismo periodo no impide la deduccion
- **Distribucion:** Si hay dos contribuyentes con derecho, se distribuye por partes iguales
- **Incompatibilidades:** Incompatible con deduccion por adopcion internacional (respecto de los mismos hijos) e incompatible con deduccion para familia numerosa

### 4. Por adopcion de hijos en ambito internacional

- **Cuantia:** 600 euros por cada hijo adoptado internacionalmente
- **Base imponible:** No supera 80.000 euros (individual) o 100.000 euros (conjunta)
- **Requisitos:**
  - Adopcion de caracter internacional conforme a normas y convenios aplicables
  - Periodo impositivo en el que se inscriba en Registro Civil
- **Distribucion:** Si hay dos adoptantes con derecho, se distribuye por partes iguales. Si uno supera bases imponibles, el otro puede aplicar importe total
- **Incompatibilidades:** Incompatible con deduccion por nacimiento/adopcion/acogimiento (respecto de los mismos hijos)

### 5. Para padre o madre de familia monoparental

- **Cuantia base:** 100 euros para contribuyentes con familia monoparental
- **Incremento adicional:** 100 euros por cada ascendiente que conviva, si generan derecho a minimo por ascendientes mayores de 75 anos
- **Base imponible:** No supera 80.000 euros (individual) o 100.000 euros (conjunta)
- **Definicion familia monoparental:** Padre o madre con hijos que convivan y cumplan:
  - Menores de edad (excepto que vivan independientes con consentimiento)
  - Mayores de edad incapacitados judicialmente o con patria potestad prorrogada/rehabilitada antes del 1-1-2022
  - Mayores de edad con discapacidad con curador por resolucion judicial
- **Incompatibilidades:** Ninguna especificada

### 6. Para familia numerosa

- **Cuantia categoria general:** 200 euros
- **Cuantia categoria especial:** 400 euros
- **Base imponible:** No supera 25.000 euros (individual) o 30.000 euros (conjunta)
- **Requisitos:**
  - Ser ascendiente y formar parte de familia numerosa, O
  - Ser hermano huérfano en casos de familias constituidas por:
    - Dos o mas hermanos huérfanos sometidos a tutela/acogimiento/guarda que convivan pero no esten a sus expensas
    - Tres o mas hermanos huérfanos mayores de 18 anos (o dos si uno tiene discapacidad) que convivan y tengan dependencia economica
  - Ostentar titulo de familia numerosa en fecha de devengo
- **Distribucion:** Si multiples contribuyentes, se distribuye por partes iguales. Si uno supera base imponible, el otro puede deducir integramente
- **Incompatibilidades:** Incompatible con deduccion por nacimiento/adopcion/acogimiento

### 7. Por gastos educativos

- **Porcentaje:** 15% de cantidades satisfechas por gastos de enseñanza escolar o extraescolar de idiomas e informatica
- **Limite maximo:** 150 euros anuales por cada descendiente
- **Base imponible:** No supera 80.000 euros (individual) o 100.000 euros (conjunta)
- **Gastos de enseñanza escolar:** Cantidades satisfechas a centros docentes en concepto de gastos de escolaridad, en proporcion de materias de idiomas/informatica (segun horas lectivas)
- **Gastos de enseñanza extraescolar:** Cantidades satisfechas a academias, escuelas oficiales de idiomas, personas fisicas en domicilios privados o lugares similares
- **Requisitos:**
  - Aplicable respecto de descendientes por los que se tenga derecho a minimo por descendientes
  - Deduccion la aplica quien efectivamente paga los gastos
  - Con multiples contribuyentes, cada uno aplica sobre lo que pago (maximo 150 euros por descendiente)
  - Con dinero ganancial, se aplica por mitades por ambos cónyuges
- **Obligaciones formales:** Conservar facturas/justificantes/recibos durante plazo de prescripcion

### 8. Para contribuyentes con discapacidad - Gastos educativos

- **Cuantia:** 150 euros por cada contribuyente con discapacidad reconocida
- **Grado minimo:** Discapacidad igual o superior al 33%
- **Base imponible:** No supera 25.000 euros (individual) o 30.000 euros (conjunta)
- **Requisitos:**
  - Grado de discapacidad >= 33% conforme a baremo articulo 367 RD Legislativo 8/2015
  - Pensionistas SS con incapacidad permanente total/absoluta o gran invalidez se consideran con >= 33%
  - Pensionistas clases pasivas con pension de jubilacion/retiro por incapacidad se consideran con >= 33%
  - Personas con incapacidad judicial anterior al 1-1-2022 se consideran con >= 65%
- **Atención:** Ha cambiado criterio de la DGT: en tributacion conjunta, solo se aplica deduccion "Por asistencia a personas con discapacidad" (no simultaneamente)

### 9. Para contribuyentes con cónyuges o parejas de hecho con discapacidad

- **Cuantia:** 100 euros por cada cónyuge o pareja con discapacidad que cumpla requisitos
- **Grado minimo:** Discapacidad igual o superior al 65%
- **Base imponible:** No supera 25.000 euros (individual) o 30.000 euros (conjunta)
- **Requisitos:**
  - No sea declarante por tributacion individual en el ejercicio
  - Grado de discapacidad >= 65% conforme a baremo
  - Para parejas de hecho: estar inscritas en Registro de Parejas de Hecho de Andalucia o registros analogos
  - Personas con incapacidad judicial anterior al 1-1-2022 se consideran con >= 65%
- **Incompatibilidades:** No tienen derecho si su cónyuge/pareja ya aplico deduccion "Para contribuyentes con discapacidad"

### 10. Por asistencia a personas con discapacidad

#### 10.1 Con caracter general
- **Cuantia:** 100 euros por cada persona con discapacidad que otorgue derecho a minimo por discapacidad de ascendientes o descendientes
- **Base imponible:** No supera 80.000 euros (individual) o 100.000 euros (conjunta)
- **Requisitos:** Conforme a normativa estatal IRPF

#### 10.2 Cuando las personas con discapacidad precisen ayuda de terceras personas
- **Porcentaje:** 20% del importe satisfecho a SS como cuota fija del empleador
- **Limite maximo:** 500 euros anuales por contribuyente
- **Requisitos:**
  - Acreditacion de que las personas con discapacidad necesitan ayuda de terceras personas
  - Generar derecho a minimo por gastos de asistencia segun IRPF estatal
  - Ser titular del hogar familiar registrado en Tesoreria General SS
  - Afiliacion en Andalucia al Sistema Especial para Empleados del Hogar
  - Indicar Codigo Cuenta Cotizacion en casilla [0859] Anexo B.1
- **Incompatibilidades:** Incompatible con deduccion "Por ayuda domestica" para la misma persona empleada

### 11. Por ayuda domestica

- **Porcentaje:** 20% del importe satisfecho al empleador a la SS por cotizacion anual de empleado del hogar
- **Limite maximo:** 500 euros
- **Requisitos:**
  - Vivienda habitual del empleador/empleadora constituye su domicilio
  - Titular del hogar familiar registrado en Tesoreria General SS
  - Afiliacion en Andalucia al Sistema Especial para Empleados del Hogar
  - Indicar Codigo Cuenta Cotizacion en casilla [0861] Anexo B.1
  - Cumplir alguno de estos supuestos:
    - Ser madre/padre de hijos que dan derecho a minimo por descendientes Y ambos cónyuges/pareja perciban rendimientos del trabajo o actividades economicas
    - Ser de edad >= 75 anos (O su cónyuge/pareja)
  - Para cónyuges/parejas de hecho inscritas, puede aplicar indistintamente titular o su cónyuge/pareja
- **Incompatibilidades:** Incompatible con "Por asistencia a personas con discapacidad" para la misma persona empleada

### 12. Por inversion en adquisicion de acciones y participaciones sociales en empresas nuevas

#### 12.1 Inversiones generales
- **Porcentaje:** 20% de cantidades invertidas en adquisicion de acciones/participaciones
- **Limite maximo:** 4.000 euros anuales
- **Formas de sociedad:** S.A., S.A.L., S.L., S.L.L., Sociedad Cooperativa
- **Requisitos:**
  - Participacion adquirida mas la del cónyuge/parientes hasta 3er grado no supera 40% del capital/derechos de voto
  - Mantener participacion minimo 3 anos
  - No ejercer funciones ejecutivas, direccion ni relacion laboral con la entidad
  - Formalizacion en escritura pública con identidad de inversores e importe
  - Entidad cumple:
    - Domicilio social y fiscal en Andalucia
    - Desarrolla actividad economica (no gestion de patrimonio)
    - Si constitucion: minimo 1 persona con contrato laboral jornada completa en SS durante minimo 24 meses
    - Si ampliacion capital: constituida hace menos de 3 anos, plantilla media se incrementa en minimo 1 persona en dos ejercicios posteriores y se mantiene otros 24 meses

#### 12.2 Inversiones en empresas de investigacion
- **Porcentaje:** 50% de cantidades invertidas
- **Limite maximo:** 12.000 euros anuales (independiente del limite de 4.000 euros)
- **Requisitos:** Mismo tipo que 12.1 pero para empresas creadas o participadas por universidades o centros de investigacion

### 13. Para gastos de defensa juridica de la relacion laboral

- **Cuantia:** Importe satisfecho por gastos de defensa juridica en procedimientos judiciales de despido, extincion de contrato, reclamacion de cantidades
- **Limite maximo:** 200 euros (individual y conjunta)
- **Obligaciones formales:** Conservar justificantes y documentos durante plazo de prescripcion

### 14. Por donativos con finalidad ecologica

- **Porcentaje:** 10% de cantidades donadas
- **Limite maximo:** 150 euros
- **Beneficiarios:**
  - Entidades públicas de Andalucia o corporaciones locales cuya finalidad sea defensa/conservacion del medio ambiente
  - Entidades sin fines lucrativos y beneficiarias de mecenazgo segun Ley 49/2002, cuyo fin exclusivo sea defensa del medio ambiente, inscritas en registros de Andalucia
- **Obligaciones formales:** Certificacion de donacion expedida por entidad beneficiaria conforme articulo 24 Ley 49/2002

### 15. Para fomentar el ejercicio fisico y la practica deportiva

- **Porcentaje:** 15% de cuotas de pertenencia o adhesion a:
  - Gimnasios
  - Centros deportivos
  - Clubes deportivos
  - Federaciones deportivas
  - Secciones deportivas o recreacion deportiva de otras entidades
- **Limite maximo:** 100 euros anuales por contribuyente
- **Aplicable a:**
  - Contribuyente, su cónyuge, pareja de hecho inscrita
  - Personas que den derecho a minimos por descendientes y ascendientes
- **Requisitos:**
  - Haber satisfecho efectivamente las cantidades (total o parcialmente)
  - Con gastos de varios contribuyentes, cada uno aplica sobre lo que pago (respetando limite de 100 euros)
  - Dinero ganancial: ambos cónyuges aplican sobre mitad de cantidades
- **Obligaciones formales:** Conservar justificantes y documentos durante plazo de prescripcion

### 16. Por gastos veterinarios de animales de compania o perros de asistencia

- **Porcentaje:** 30% de cantidades satisfechas por gastos veterinarios
- **Limite maximo:** 100 euros anuales por contribuyente
- **Base imponible:** No supera 80.000 euros (individual) o 100.000 euros (conjunta)
- **Gastos deducibles:**
  - Vacunaciones, desparasitacion y tratamientos obligatorios conforme normativa
  - Gastos de esterilizacion del animal cuando sea preceptiva segun legislacion
- **Definiciones:**
  - Animales de compania: Animales domesticos/silvestres en cautividad mantenidos principalmente en hogar respetando bienestar y necesidades etologicas. Siempre: perros, gatos, hurones. No incluye animales de produccion salvo que pierdan fin productivo e inscritos como compania
  - Perros de asistencia: Han superado proceso de seleccion/adiestramiento en entidad especializada reconocida por administracion, con aptitudes para asistencia a personas con discapacidad, o perros de aviso para victimas de violencia de genero segun regulacion
- **Ambito temporal:**
  - General: Durante ano siguiente a adquisicion del animal
  - Adopcion: Durante 3 anos siguientes a fecha de adopcion
  - Perros de asistencia: Durante todo periodo de tenencia
- **Requisitos:**
  - Gastos satisfechos desde 1-1-2025
  - Adquisicion formalizada desde 1-1-2025 (excepto perros de asistencia)
  - Gastos justificados mediante factura de profesional/centro veterinario legalmente autorizado
  - Precisiones sobre cuentas multitulares y dinero ganancial aplican igual que otras deducciones

### 17. Para familias con enfermedad celiaca diagnosticada

- **Cuantia:** 100 euros por cada persona del nucleo familiar con enfermedad celiaca diagnosticada
- **Personas del nucleo familiar:** Contribuyente, cónyuge/pareja inscrita, personas que den derecho a minimos por ascendientes/descendientes
- **Requisitos:**
  - Acreditacion mediante informe medico oficial con diagnostico definitivo segun criterios cientificos
  - Emitido por profesionales del Sistema Sanitario Público de Andalucia (SSPA) o servicios de salud públicos (SNS), identificados con Codigo Numérico Personal (CNP)
  - O profesionales adscritos a entidad aseguradora privada, identificados con numero de colegiado
- **Distribucion:** Si multiples contribuyentes con derecho por misma persona, importe se distribuye por partes iguales

---

## PREGUNTAS CLAVE PARA EL CONTRIBUYENTE

1. Eres menor de 35 anos, mayor de 65, victima de violencia domestica o persona afectada por terrorismo?
2. Pagas alquiler de vivienda habitual en Andalucia? Es tu base imponible menor a los limites establecidos?
3. Has tenido hijos nacidos, adoptados o en acogimiento durante 2025? Vives en municipio con problemas de despoblacion?
4. Has adoptado hijos internacionalmente? Tu base imponible esta dentro de los limites de renta?
5. Eres padre o madre de familia monoparental o tienes ascendientes mayores de 75 anos?
6. Tu familia tiene titulo de familia numerosa? Cual es la categoria (general o especial)?
7. Has pagado gastos educativos por idiomas e informatica? Tienes descendientes que den derecho a minimo?
8. Tienes discapacidad reconocida o cónyuge/pareja con discapacidad? Que grado tienes acreditado?
9. Tienes personas con discapacidad a cargo que necesiten ayuda de terceras personas? Empleas personal del hogar?
10. Has realizado inversiones en empresas nuevas constituidas en Andalucia o universidades? Mantienes la participacion requerida?
11. Has tenido gastos por defensa juridica en procedimientos laborales de despido?
12. Has realizado donaciones para actividades ecologicas o de defensa del medio ambiente?
13. Pagas cuotas en gimnasios, centros deportivos o clubes deportivos? Tienes limite de renta aplicable?
14. Has adoptado animales de compania o tienes perros de asistencia? Que gastos veterinarios has pagado desde enero de 2025?
15. Tienes diagnosticada enfermedad celiaca tu o algún miembro de tu familia? Tienes informe medico oficial?

---

## FUENTES

- Manual Practico Renta 2025 Parte 2 Deducciones Autonomicas: https://sede.agenciatributaria.gob.es/Sede/ayuda/manuales-videos-folletos/manuales-practicos/irpf-2025-deducciones-autonomicas/comunidad-autonoma-andalucia.html
- Ley 5/2021, de 20 de octubre, de Tributos Cedidos de la Comunidad Autonoma de Andalucia
