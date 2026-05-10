# 📊 Análisis de Comportamiento de Clientes — E-commerce

> **Proyecto de análisis exploratorio enfocado en comprender los factores que impulsan el gasto de clientes en un entorno de comercio electrónico**, utilizando estadística descriptiva, correlaciones y regresión lineal.

---

## 🎯 Objetivo del proyecto

Identificar los principales factores que explican el comportamiento de gasto de los clientes, con el fin de generar **insights accionables** para estrategias de marketing, retención y conversión.

---

## 🧰 Tecnologías y herramientas

| Herramienta | Uso |
|---|---|
| `Python 3.14` | Lenguaje principal |
| `Pandas` | Manipulación y análisis de datos |
| `NumPy` | Cálculos numéricos |
| `Matplotlib` | Visualizaciones personalizadas |
| `Seaborn` | Visualizaciones estadísticas |
| `Statsmodels` | Modelo de regresión lineal OLS |

---

## 📁 Estructura del proyecto

```
analisis-clientes-ecommerce/
│
├── ProyectoModulo4F.ipynb    # Notebook principal con análisis completo
├── README.md                 # Documentación del proyecto
├── compras_vs_monto_total.png
└── compras_vs_monto_total.pdf
```

---

## 📋 Dataset

Dataset sintético de **200 clientes** generado con semilla fija (`seed=42`) para garantizar **reproducibilidad completa**.

| Variable | Tipo | Descripción |
|---|---|---|
| `visitas_web` | Cuantitativa discreta | Número de visitas al sitio web |
| `Compras` | Cuantitativa discreta | Número de compras realizadas |
| `monto_total` | Cuantitativa continua | Gasto total en USD |
| `devoluciones` | Cuantitativa discreta | Número de devoluciones |
| `reseñas` | Ordinal (1–5) | Calificación del cliente |
| `genero` | Categórica | Masculino / Femenino |

> ✅ Dataset sin valores faltantes ni valores atípicos detectados.

---

## 🔍 Etapas del análisis

### 1. Análisis Exploratorio de Datos (EDA)
- Clasificación de variables (continuas, discretas, categóricas)
- Detección de valores faltantes e inconsistencias
- Exploración visual inicial con pairplot

### 2. Estadística Descriptiva
- Medidas de tendencia central: media, mediana, moda
- Medidas de dispersión: varianza, desviación estándar
- Análisis de cuartiles y distribución con histogramas y boxplots
- Detección de outliers con método IQR

### 3. Análisis de Correlación
- Matriz de correlación de Pearson
- Heatmap de correlaciones
- Identificación y justificación de correlaciones significativas

### 4. Regresión Lineal
- Modelo OLS con `statsmodels`
- Evaluación con R², MSE y MAE
- Verificación de supuestos: homocedasticidad y normalidad de residuos

### 5. Visualización Avanzada (Seaborn + Matplotlib)
- Pairplot segmentado por género
- Violinplots por categoría
- Jointplots con línea de regresión
- FacetGrid por género
- Scatterplots con anotaciones

---

## 📈 Resultados clave

```
Pearson R  — Compras vs monto_total:    0.939  🔴 Correlación muy fuerte
Pearson R  — visitas_web vs Compras:    0.918  🔴 Correlación muy fuerte
Pearson R  — devoluciones vs reseñas:   0.065  ⚪ Sin correlación relevante

R² del modelo OLS:  0.879
→ El número de compras explica el 87.9% de la variabilidad del gasto total.

Coeficiente de Compras: 70.44
→ Cada compra adicional incrementa el gasto total en ~$70.44.
```

---

## 💡 Insights de negocio

- **El tráfico web convierte:** A mayor número de visitas al sitio, mayor cantidad de compras realizadas (r ≈ 0.92). Invertir en adquisición de tráfico tiene impacto directo en ventas.

- **La frecuencia de compra es el principal driver de ingresos:** El número de compras es el predictor más fuerte del gasto total (R² = 0.88). Estrategias de fidelización y recompra son prioritarias.

- **Las devoluciones son proporcionales al volumen:** Clientes con más compras también hacen más devoluciones — no es un comportamiento negativo, sino una consecuencia del volumen.

- **El género no segmenta el comportamiento:** No se detectaron diferencias significativas entre géneros en compras ni en gasto total. Las campañas pueden ser universales en lugar de segmentadas por género.

- **Las reseñas no predicen el gasto:** Alta satisfacción general (mayoría de calificaciones en 4–5), pero sin correlación con el comportamiento de compra.

---

## ▶️ Cómo ejecutar el proyecto

```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/analisis-clientes-ecommerce.git
cd analisis-clientes-ecommerce

# 2. Instalar dependencias
pip install numpy pandas matplotlib seaborn statsmodels

# 3. Abrir el notebook
jupyter notebook ProyectoModulo4F.ipynb
```

> No se requieren datos externos. El dataset se genera automáticamente al ejecutar la primera celda.

---

## 👤 Autor

** Martin Rojas **
Analista de Datos | Python · SQL · Visualización · Estadística

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](linkedin.com/in/martín-rojas-páez)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-181717?style=flat&logo=github)](github.com/Martineliasz)

---

*Proyecto desarrollado como parte del portafolio profesional de análisis de datos.*
