# Análisis de Datos del Triatlón Ironman

## Introducción
El triatlón Ironman es una de las competencias deportivas más desafiantes del mundo. Los participantes deben completar 3.86 km de natación, 180 km de ciclismo y 42.2 km de carrera a pie dentro de un tiempo límite de 17 horas. Este proyecto se centra en analizar datos históricos de competencias Ironman, con un enfoque en la visualización y comprensión de patrones en el desempeño de los atletas.

Este análisis utiliza un conjunto de datos que contiene información sobre competiciones Ironman, como el año, la posición, el nombre del atleta, el país de origen, el tiempo total, y el género.

---

## Estructura del Cuaderno

El cuaderno Jupyter está dividido en las siguientes secciones:

### 1. **Carga y Descripción de Datos**
- Se cargan los datos desde el archivo CSV proporcionado.
- Exploración inicial de las columnas disponibles:
  - `Year`: Año de la competición.
  - `Place`: Posición final del atleta.
  - `Athlete`: Nombre del atleta.
  - `Country`: País de origen del atleta.
  - `Time`: Tiempo total del atleta en formato HH:MM:SS.
  - `Gender`: Género del atleta.
- Se realiza una limpieza de los datos:
  - Conversión de tiempos a formato numérico.
  - Eliminación de valores nulos y duplicados.

### 2. **Estadísticas Generales**
- Resumen descriptivo de las principales métricas, como:
  - Tiempos promedio por año.
  - Distribución de posiciones por género.
  - Comparación del desempeño por país.

### 3. **Visualizaciones de Datos**

#### 3.1. **Distribución de Tiempos**
- Histogramas para visualizar la distribución de los tiempos totales.
- Gráficos separados por género para identificar diferencias en los tiempos promedio.

#### 3.2. **Mapas de Calor**
- Mapas de calor para identificar patrones geográficos en los resultados:
  - Desempeño promedio por país.
  - Concentración de posiciones destacadas por región.

#### 3.3. **Evolución Temporal**
- Gráficos de línea para mostrar:
  - Tendencias de tiempos promedio a lo largo de los años.
  - Evolución del desempeño por género.

#### 3.4. **Comparaciones entre Países**
- Gráficos de barras apiladas para comparar la proporción de atletas destacados por país y género.

#### 3.5. **Relaciones entre Variables**
- Scatter plots y diagramas de correlación para explorar relaciones entre el tiempo total y otros factores, como posición o género.

---

## Herramientas y Librerías Utilizadas

El análisis fue desarrollado utilizando las siguientes librerías de Python:

- **Pandas**: Manipulación y limpieza de datos.
- **Matplotlib**: Gráficos básicos y avanzados.
- **Seaborn**: Visualizaciones estilizadas y mapas de calor.
- **Plotly**: Gráficos interactivos para exploración de datos.
- **Geopandas**: Creación de mapas geográficos para visualización.

---

## Cómo Usar el Cuaderno

1. **Pre-requisitos**:
   - Python 3.8 o superior.
   - Instalación de librerías necesarias:
     ```bash
     pip install pandas matplotlib seaborn plotly geopandas
     ```

2. **Ejecutar el Cuaderno**:
   - Descarga el archivo `Ironman_Analysis.ipynb`.
   - Coloca el archivo de datos CSV en la misma carpeta que el cuaderno.
   - Abre el cuaderno con Jupyter Notebook o Jupyter Lab y ejecuta las celdas en orden.

---

## Conclusiones

El análisis de los datos del Ironman reveló:
- Diferencias significativas en el desempeño entre géneros.
- Patrones geográficos que destacan países con mayor cantidad de atletas de alto rendimiento.
- Tendencias temporales que sugieren una mejora general en los tiempos promedio a lo largo de los años.

Este proyecto ofrece una base sólida para futuros análisis más detallados, como el impacto de variables externas (clima, altitud, etc.) en el desempeño de los atletas.

---

Puedes encontrar la fuente original del dataset en:
[https://data.world/makeovermonday/2019w42](https://data.world/makeovermonday/2019w42).
