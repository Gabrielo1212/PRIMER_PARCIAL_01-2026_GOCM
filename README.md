
# 📊 Preparación de Insumos - Primer Parcial IA (01/2026)

## Resumen de Datos Procesados

| Dataset | Filas | Columnas | Tipo de Problema |
| 1. Ames Housing | 2,930 | 82 | Regresión |
| 2. MIMIC-III Patients | 100 | 8 | Clasificación |
| 3. NHANES Combined | 8,068 | 51 | Análisis Multivariado |
| 4. Bike Sharing | 10,886 | 12 | Regresión |
| 5. Adult Census | 32,561 | 15 | Clasificación |
| 6. Credit Approval | 690 | 16 | Clasificación |
| 7. Australian Credit | 690 | 15 | Clasificación |
| 8. Breast Cancer | 699 | 11 | Clasificación |
| 9. Meningitis | 1,200 | 14 | Clasificación / Imputación |

# Apéndice: 

### 1. Ames Housing Dataset (82 Columnas)
* **Identificadores:** `Order`, `PID` (ID único de la parcela).
* **Ubicación y Terreno:** `MS SubClass` (Tipo de construcción), `MS Zoning` (Clasificación de zona), `Lot Frontage` (Pies de calle), `Lot Area` (Tamaño del lote), `Street`, `Alley` (Acceso), `Lot Shape` (Forma), `Land Contour` (Plenitud), `Utilities` (Servicios), `Lot Config` (Configuración), `Land Slope` (Pendiente), `Neighborhood` (Barrio), `Condition 1/2` (Proximidad a vías).
* **Estructura y Calidad:** `Bldg Type` (Tipo de vivienda), `House Style` (Estilo), `Overall Qual` (Calidad 1-10), `Overall Cond` (Condición 1-10), `Year Built` (Construcción), `Year Remod/Add` (Remodelación).
* **Exterior:** `Roof Style`, `Roof Matl`, `Exterior 1st/2nd` (Materiales exteriores), `Mas Vnr Type`, `Mas Vnr Area` (Revestimiento), `Exter Qual`, `Exter Cond`.
* **Sótano (Basement):** `Foundation`, `Bsmt Qual`, `Bsmt Cond`, `Bsmt Exposure`, `BsmtFin Type 1/2`, `BsmtFin SF 1/2`, `Bsmt Unf SF` (Pies sin finalizar), `Total Bsmt SF`.
* **Interiores y Confort:** `Heating`, `Heating QC`, `Central Air`, `Electrical`, `1st Flr SF`, `2nd Flr SF`, `Low Qual Fin SF`, `Gr Liv Area` (Área habitable), `Bsmt Full/Half Bath`, `Full/Half Bath`, `Bedroom AbvGr`, `Kitchen AbvGr`, `Kitchen Qual`, `TotRms AbvGrd`, `Functional` (Funcionalidad).
* **Extras y Garaje:** `Fireplaces`, `Fireplace Qu`, `Garage Type`, `Garage Yr Blt`, `Garage Finish`, `Garage Cars`, `Garage Area`, `Garage Qual`, `Garage Cond`, `Paved Drive`, `Wood Deck SF`, `Open Porch SF`, `Enclosed Porch`, `3Ssn Porch`, `Screen Porch`, `Pool Area`, `Pool QC`, `Fence`, `Misc Feature`, `Misc Val`.
* **Venta (Target):** `Mo Sold`, `Yr Sold`, `Sale Type`, `Sale Condition`, `SalePrice` (Precio final).

### 2. MIMIC-III Patients (8 Columnas)
* `row_id`: ID de fila en la base de datos.
* `subject_id`: Identificador único del paciente.
* `gender`: Género (M/F).
* `dob`: Fecha de nacimiento (Date of Birth).
* `dod`: Fecha de fallecimiento (Date of Death).
* `dod_hosp`: Fecha de fallecimiento en el hospital.
* `dod_ssn`: Fecha de fallecimiento según seguridad social.
* `expire_flag` (Target): Supervivencia (0: Vivo, 1: Fallecido).

### 3. NHANES Combined (51 Columnas)
* **Demografía (DEMO_L):**
    * `SEQN`: Número de secuencia (ID único del participante).
    * `SDDSRVYR`: Ciclo de datos de la encuesta NHANES.
    * `RIDSTATR`: Estado del examen (1: Solo entrevistado, 2: Entrevistado y examinado).
    * `RIAGENDR`: Género (1: Masculino, 2: Femenino).
    * `RIDAGEYR`: Edad en años al momento del screening.
    * `RIDAGEMN`: Edad en meses (para participantes menores de 25 años).
    * `RIDRETH1`: Etnia/Raza Recodificada (5 categorías).
    * `RIDRETH3`: Etnia/Raza Recodificada con desglose asiático.
    * `RIDEXMON`: Periodo del año en que se realizó el examen (Nov-Abr / May-Oct).
    * `RIDEXAGM`: Edad en meses al momento del examen físico.
    * `DMQMILIZ`: ¿Ha servido activamente en las Fuerzas Armadas de EE.UU.?
    * `DMDBORN4`: País de nacimiento.
    * `DMDYRUSR`: Años de residencia en los EE.UU.
    * `DMDEDUC2`: Nivel educativo (Adultos mayores de 20 años).
    * `DMDMARTZ`: Estado civil.
    * `RIDEXPRG`: Estado de embarazo al momento del examen.
    * `DMDHHSIZ`: Número de personas viviendo en el hogar.
    * `DMDHRGND`: Género de la persona de referencia del hogar.
    * `DMDHRAGZ`: Edad de la persona de referencia del hogar.
    * `DMDHREDZ`: Nivel educativo de la persona de referencia.
    * `DMDHRMAZ`: Estado civil de la persona de referencia.
    * `DMDHSEDZ`: Educación del cónyuge de la persona de referencia.
    * `WTINT2YR`: Peso de la muestra para la entrevista (2 años).
    * `WTMEC2YR`: Peso de la muestra para el examen en el MEC (2 años).
    * `SDMVSTRA`: Pseudo-estrato de enmascaramiento para estimación de varianza.
    * `SDMVPSU`: Unidad primaria de muestreo de enmascaramiento.
    * `INDFMPIR`: Ratio de ingresos familiares frente al umbral de pobreza.

* **Examen Físico - Medidas Corporales (BMX_L):**
    * `SEQN`: Número de secuencia (ID único del participante).
    * `BMDSTATS`: Estado del examen de medidas corporales.
    * `BMXWT`: Peso (kg).
    * `BMIWT`: Comentario sobre la medición del peso (indica si hubo factores que afectaron la toma).
    * `BMXRECUM`: Longitud recumbente (cm) - Medida para infantes o personas que no pueden estar de pie.
    * `BMIRECUM`: Comentario sobre longitud recumbente.
    * `BMXHEAD`: Circunferencia de la cabeza (cm).
    * `BMIHEAD`: Comentario sobre circunferencia de cabeza.
    * `BMXHT`: Estatura (cm).
    * `BMIHT`: Comentario sobre la estatura.
    * `BMXBMI`: Índice de Masa Corporal (kg/m²).
    * `BMDBMIC`: Categoría de IMC para niños y adolescentes (Percentiles).
    * `BMXLEG`: Longitud de la parte superior de la pierna (cm).
    * `BMILEG`: Comentario sobre longitud de pierna.
    * `BMXARML`: Longitud de la parte superior del brazo (cm).
    * `BMIARML`: Comentario sobre longitud de brazo.
    * `BMXARMC`: Circunferencia del brazo (cm).
    * `BMIARMC`: Comentario sobre circunferencia de brazo.
    * `BMXWAIST`: Circunferencia de la cintura (cm).
    * `BMIWAIST`: Comentario sobre la cintura.
    * `BMXHIP`: Circunferencia de la cadera (cm).
    * `BMIHIP`: Comentario sobre la cadera.

* **Laboratorio - Colesterol Total (TCHOL_L):**
    * `LBXTC`: **Total Cholesterol** (Nivel de colesterol total medido en mg/dL).
    * `LBDTCSI`: **Total Cholesterol SI** (Nivel de colesterol total en unidades internacionales mmol/L).
    * `WTPH2YR`: Peso de la muestra para el subgrupo de ayuno/laboratorio (usado para análisis estadístico de precisión).

### 4. Bike Sharing (12 Columnas)
* `datetime`: Fecha y hora (timestamp).
* `season`: Estación (1: Primavera, 2: Verano, 3: Otoño, 4: Invierno).
* `holiday`: Si es día festivo (0/1).
* `workingday`: Si es día laboral (0/1).
* `weather`: Clima (1: Despejado a 4: Tormenta).
* `temp`: Temperatura en Celsius.
* `atemp`: Sensación térmica en Celsius.
* `humidity`: Humedad relativa.
* `windspeed`: Velocidad del viento.
* `casual`: Usuarios no registrados.
* `registered`: Usuarios registrados.
* `count` (Target): Total de rentas (casual + registered).

### 5. Adult Census (15 Columnas)
* `age`: Edad del individuo.
* `workclass`: Clase de trabajo (Private, Self-emp, Local-gov, etc.).
* `fnlwgt`: Peso final (estimación demográfica).
* `education`: Nivel de estudios (Bachelors, Masters, etc.).
* `education-num`: Años de estudio (versión numérica de la anterior).
* `marital-status`: Estado civil.
* `occupation`: Ocupación técnica.
* `relationship`: Relación familiar (Husband, Wife, Own-child, etc.).
* `race`: Etnia.
* `sex`: Sexo (Male/Female).
* `capital-gain / capital-loss`: Ganancias y pérdidas de capital.
* `hours-per-week`: Horas trabajadas por semana.
* `native-country`: País de origen.
* `income` (Target): Nivel de ingresos (>50K, <=50K).

### 6. Credit Approval (16 Columnas)
* *Nota: Las variables están anonimizadas por privacidad bancaria.*
* `A1`: Género (a, b).
* `A2`: Edad (continua).
* `A3`: Deuda (continua).
* `A4`: Estado civil (u, y, l, t).
* `A5`: Cliente bancario (g, p, gg).
* `A6`: Nivel educativo (c, d, cc, i, j, k, m, r, q, w, x, e, aa, ff).
* `A7`: Etnia (v, h, bb, j, n, z, dd, ff, o).
* `A8`: Años de empleo (continuo).
* `A9`: Prior Default (t, f).
* `A10`: Empleado (t, f).
* `A11`: Score de crédito (numérico).
* `A12`: Licencia de conducir (t, f).
* `A13`: Ciudadanía (g, p, s).
* `A14`: Código postal (numérico).
* `A15`: Ingresos (numérico).
* `A16` (Target): Decisión (+ aprobado, - rechazado).

### 7. Statlog Australian Credit (15 Columnas)
* `A1` a `A6`: Variables demográficas y financieras categóricas ya mapeadas a enteros.
* `A7`: Variable continua.
* `A8` a `A13`: Atributos financieros.
* `A14`: Variable continua.
* `A15` (Target): Clase (1: Aprobado, 0: Rechazado).

### 8. Breast Cancer Wisconsin (11 Columnas)
* `Sample code number`: ID de la muestra.
* `Clump Thickness`: Grosor del grupo (1-10).
* `Uniformity of Cell Size`: Uniformidad del tamaño celular (1-10).
* `Uniformity of Cell Shape`: Uniformidad de la forma celular (1-10).
* `Marginal Adhesion`: Adhesión marginal (1-10).
* `Single Epithelial Cell Size`: Tamaño de célula epitelial (1-10).
* `Bare Nuclei`: Núcleos desnudos (1-10).
* `Bland Chromatin`: Cromatina blanda (1-10).
* `Normal Nucleoli`: Nucléolos normales (1-10).
* `Mitoses`: Mitosis (crecimiento) (1-10).
* `Class` (Target): Diagnóstico (2: Benigno, 4: Maligno).

### 9. Meningitis Dataset (14 Columnas)
* `Patient_ID`: ID del paciente.
* `Age`: Edad.
* `Gender`: Género.
* `WBC_Count`: Conteo de glóbulos blancos en LCR.
* `Protein_Level`: Nivel de proteína en LCR.
* `Glucose_Level`: Nivel de glucosa en LCR.
* `Pathogen_Present`: Presencia de patógeno (Yes/No).
* `Diagnosis`: Tipo de meningitis (Viral, Bacterial, Fungal, Unknown).
* `Outcome`: Resultado (Recovered, Deceased).
* `Hemoglobin`: Nivel de hemoglobina en sangre.
* `WBC_Blood_Count`: Glóbulos blancos en sangre.
* `Platelets`: Conteo de plaquetas.
* `CRP_Level`: Proteína C reactiva (marcador de inflamación).
* `Risk_Level` (Target): Clasificación de riesgo (Low, Moderate, High).