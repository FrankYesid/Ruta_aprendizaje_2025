# 📊 Toyota Stock Dataset Analysis (1980-2024)

Este proyecto realiza el análisis y preprocesamiento de datos históricos de las acciones de Toyota Motor Corporation (ticker: TM) utilizando Python. Además, integra **Sweetviz** para generar informes automatizados de análisis exploratorio y utiliza visualizaciones avanzadas para entender las tendencias y distribuciones de los datos.

## 📁 Contenido del Dataset

El dataset contiene información diaria de trading desde 1980 hasta 2024 con las siguientes columnas:

| Columna     | Descripción                                                                 |
|-------------|-----------------------------------------------------------------------------|
| Date        | Fecha de la transacción en formato YYYY-MM-DD.                             |
| Adj Close   | Precio de cierre ajustado considerando dividendos o splits.               |
| Close       | Precio de cierre oficial del día.                                          |
| High        | Precio más alto del día.                                                  |
| Low         | Precio más bajo del día.                                                  |
| Open        | Precio de apertura del día.                                               |
| Volume      | Número total de acciones negociadas.                                      |

---

## 🔧 Pasos Realizados

### 1️⃣ **Carga de Datos**
- Se lee el archivo CSV que contiene los datos históricos utilizando `pandas`.
- Los datos originales se visualizan y revisan para asegurar que la estructura esté correcta.

### 2️⃣ **Informe Automatizado con Sweetviz**
- Se utiliza **Sweetviz** para generar un informe exploratorio detallado que incluye estadísticas descriptivas, gráficos comparativos y la detección de valores faltantes o inconsistencias.
- El informe se guarda como un archivo HTML (`sweetviz_report.html`) y se puede abrir en cualquier navegador.

```python
import sweetviz as sv
report = sv.analyze(data)
report.show_html('sweetviz_report.html')
```

### 3️⃣ **Pipeline de Preprocesamiento**
Un pipeline automatizado se implementa para realizar los siguientes pasos:

#### 🔹 Transformación de Fechas
- Convierte la columna `Date` al formato de fecha (`datetime`).
- Extrae las columnas de **año**, **mes** y **día** para facilitar el análisis temporal.

#### 🔹 Eliminación de Valores Atípicos
- Se calcula el rango intercuartil (IQR) y se eliminan las filas con valores fuera del rango permitido.

#### 🔹 Estandarización de Datos
- Los valores numéricos se escalan utilizando `StandardScaler` de scikit-learn.

```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler

pipeline = Pipeline([
    ('date_transformer', DateTransformer()),
    ('outlier_remover', OutlierRemover()),
    ('scaler', StandardScaler())
])
data_cleaned = pipeline.fit_transform(data)
```

### 4️⃣ **Visualización de Datos**
Se crean gráficos para explorar las tendencias y distribuciones de los datos:

#### 📈 Tendencia de Precios Ajustados
- Gráfica de líneas que muestra la evolución de los precios ajustados (`Adj Close`) a lo largo del tiempo.

#### 📊 Distribución de Precios
- Gráfica de caja que compara las distribuciones de las columnas `Adj Close`, `Close`, `High`, `Low` y `Open`.

```python
sns.lineplot(data=data_cleaned, x='Date', y='Adj Close')
sns.boxplot(data=data_cleaned[['Adj Close', 'Close', 'High', 'Low', 'Open']])
```

### 5️⃣ **Resumen de Datos Limpios**
- Se imprimen estadísticas descriptivas finales para validar la completitud y coherencia de los datos procesados.

---

## 🚀 Resultados

1. **Informe Sweetviz**: Un reporte HTML interactivo con estadísticas detalladas y gráficos.
2. **Datos Limpiados**: Un conjunto de datos listo para análisis o modelado predictivo.
3. **Visualizaciones**: Gráficos que permiten entender la evolución histórica y la distribución de los precios.

---

## 💻 Cómo Usar

1. Clona este repositorio.
2. Instala las dependencias necesarias:
   ```bash
   pip install pandas numpy sweetviz matplotlib seaborn scikit-learn
   ```
3. Ejecuta el cuaderno Jupyter (`Toyota_Stock_Analysis.ipynb`).
4. Abre el informe de Sweetviz:
   - Busca el archivo `sweetviz_report.html` generado en tu directorio de trabajo.

---

## 📂 Estructura del Proyecto

```plaintext
Toyota_Stock_Analysis/
├── toyota_stock.csv         # Dataset original
├── Toyota_Stock_Analysis.ipynb  # Cuaderno de análisis
├── sweetviz_report.html     # Informe HTML de Sweetviz
├── README.md                # Descripción del proyecto
```

---

## 📊 Aplicaciones

Este proyecto se puede utilizar para:
- Modelado predictivo de precios de acciones.
- Exploración de tendencias financieras a lo largo de varias décadas.
- Optimización de portafolios de inversión.
- Análisis de la volatilidad de los mercados financieros.
- Identificación de patrones en la evolución de los precios de las acciones.
