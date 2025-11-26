# 🧮 SQL Financial Transactions Analysis
**Portafolio Data Analyst | 2025**  
Análisis SQL de transacciones financieras utilizando múltiples tablas relacionadas

---

## 🎯 1. Objetivo del proyecto
Realizar un análisis SQL integral sobre datos transaccionales financieros para:

- Explorar comportamiento de usuarios  
- Identificar patrones en métodos de pago y montos  
- Obtener KPIs clave mediante consultas avanzadas  
- Analizar la relación entre usuarios, tarjetas, MCCs y transacciones  
- Evaluar actividad sospechosa o atípica (fraud flags)

El propósito es demostrar habilidades prácticas en SQL para análisis real aplicado a negocio.

---

## 📁 2. Tablas utilizadas
El análisis se realizó a partir de varias fuentes relacionadas:

- 🧍 **users_data** — Información general de usuarios  
- 💳 **cards_data** — Detalle de tarjetas asignadas  
- 🛒 **transactions_data / transactions_sample** — Transacciones financieras  
- 🏷️ **mcc_codes** — Códigos MCC y categorías comerciales  
- ⚠️ **train_fraud_labels** — Etiquetas de posibles fraudes  
- 🧩 **fintech_transactions** — Archivo consolidado

---

## 🛠️ 3. Herramientas utilizadas
- 🗄️ **SQL** (consultas, joins, agregaciones, filtros, subqueries)  
- 🐍 Python para ejecutar SQL desde notebook  
- 📓 Jupyter Notebook  
- 🗂️ GitHub  

---

## 🔎 4. Proceso analítico

### 🧹 4.1 Preparación
- Conectores a SQL desde Python  
- Exploración de estructura de tablas  
- Validación de llaves, duplicados y consistencia  

### 📈 4.2 Consultas principales realizadas
Incluyen, entre otras:

- **Conteo total de transacciones**  
- **Monto total transaccionado por usuario**  
- **Agrupación por método de pago**  
- **Top categorías MCC por volumen de operaciones**  
- **Promedio, máximo y mínimo de montos por día**  
- **Transacciones por país y usuario**  
- **Segmentación por tipo de tarjeta**  
- **Cruce de transacciones con etiquetas de fraude**

### 🧩 4.3 Joins y unificaciones
Se realizaron múltiples combinaciones entre tablas:

- `LEFT JOIN` para unir usuarios con transacciones  
- `INNER JOIN` para MCC y categorías  
- `JOIN` con tarjetas asociadas  
- `JOIN` con labels de fraude para análisis avanzado  

### 🚨 4.4 Indicadores adicionales detectados
- Usuarios con patrones atípicos  
- Transacciones inusualmente altas  
- Categorías de riesgo  
- Frecuencia por usuario vs. ticket promedio  

---

## 📌 5. Principales hallazgos
- 📊 **Los usuarios realizan transacciones principalmente en categorías MCC como retail, servicios y restaurantes.**  
- 💳 **Los métodos de pago más usados** corresponden a tarjetas de débito y crédito.  
- 💵 **El ticket promedio** presenta variaciones importantes por categoría MCC.  
- 🌎 **La actividad geográfica** muestra concentraciones según país/ciudad.  
- ⚠️ **Los registros cruzados con etiquetas de fraude** detectan patrones anómalos útiles para modelos de clasificación.  

*(Los hallazgos pueden variar según la versión del dataset utilizado.)*

---

## 💡 6. Insights accionables
- Utilizar MCC categories para **segmentar usuarios y ofrecer promociones orientadas**.  
- Identificar usuarios con alta frecuencia + monto elevado para **campañas premium**.  
- Analizar patrones asociados a etiquetas de fraude para **alimentar modelos predictivos**.  
- Detectar categorías con bajo ticket promedio para **evaluar oportunidades comerciales**.  
- Evaluar flujos transaccionales por país para **expansión o ajustes operativos**.

---

## 🗄️ 7. Consultas SQL destacadas
El notebook incluye consultas como:

- `SELECT COUNT(*) FROM transactions_data;`  
- Agrupaciones por MCC y método de pago  
- Subqueries para obtener máximos/mínimos  
- Joins entre 4+ tablas  
- Cálculo de KPIs de negocio vía SQL puro  

Todas están explicadas en el notebook:  
`03 Analisis SQL de transacciones financieras.ipynb`

---

## 📂 8. Estructura del repositorio
├── 03_sql_financial_analysis.ipynb
├── data/
│ ├── cards_data.csv
│ ├── users_data.csv
│ ├── transactions_data.csv
│ ├── transactions_sample.csv
│ ├── mcc_codes.csv
│ ├── fintech_transactions.db
│ └── train_fraud_labels.json
├── README.md

---

## 👤 9. Autor
**Josué Téllez**  
Data Analyst — Portafolio 2025
