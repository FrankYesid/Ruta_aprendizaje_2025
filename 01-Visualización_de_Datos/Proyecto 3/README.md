Aquí tienes una estructura sugerida para el archivo `README.md` explicando el código del cuaderno:

---

# Narrativa de Datos: Evolución del COVID-19 en LATAM

Este proyecto utiliza datos históricos del COVID-19 en América Latina (LATAM) para explorar la evolución de casos, muertes y vacunaciones a lo largo del tiempo. El objetivo principal es visualizar los datos de manera clara y proporcionar insights sobre la pandemia en la región.

## Archivos del Proyecto

- **`covid_latam(raw).csv`**: Datos crudos que contienen información sobre casos acumulados, muertes y otros indicadores relevantes para 32 países de LATAM.
- **`Daily_covid_cases_latam.csv`**: Datos de casos diarios de COVID por millón de habitantes.
- **`Daily_covid_deaths_latam.csv`**: Datos de muertes diarias confirmadas por COVID por millón de habitantes.
- **`daily_covid_vaccinations_latam.csv`**: Datos de vacunaciones diarias confirmadas de COVID por cada 100 habitantes.

## Requisitos Previos

1. Python 3.8 o superior.
2. Librerías necesarias:
   - `pandas`
   - `matplotlib`
   - `seaborn`

Puedes instalar estas librerías ejecutando:  
```bash
pip install pandas matplotlib seaborn
```

## Estructura del Código

### 1. **Carga de Datos**

El código carga cuatro datasets principales desde la carpeta `./data`:
- Datos crudos del COVID-19.
- Datos diarios de casos, muertes y vacunaciones.

### 2. **Análisis de un País Específico**

El análisis se enfoca inicialmente en un país (por defecto, Argentina). Se filtran los datos para ese país y se convierten las fechas al formato `datetime` para facilitar la visualización.

### 3. **Visualización de Datos**

Se generan tres gráficos principales:

#### Gráfico 1: Evolución de Casos y Muertes Acumulados
- Muestra la evolución de los casos y muertes acumuladas en el país seleccionado.
- Colores:
  - Azul: Casos acumulados.
  - Rojo: Muertes acumuladas.

#### Gráfico 2: Vacunaciones Diarias
- Muestra las vacunaciones diarias en el país seleccionado usando un gráfico de barras.

#### Gráfico 3: Comparativa entre Países (Top 5 Casos Acumulados)
- Compara los 5 países con más casos acumulados en LATAM utilizando un gráfico de barras.

### 4. **Configuración de Gráficos**
El código utiliza:
- **Seaborn**: Para configurar estilos de gráficos.
- **Matplotlib**: Para generar gráficos personalizados.

## Cómo Ejecutar el Código

1. Asegúrate de que los archivos de datos estén ubicados en la carpeta `./data`.
2. Ejecuta el script o cuaderno Jupyter.
3. Los gráficos se generarán automáticamente.

## Resultados Esperados

El script genera las siguientes visualizaciones:
1. Evolución de casos y muertes acumulados en un país.
2. Vacunaciones diarias en un país.
3. Comparación entre los 5 países con más casos acumulados en LATAM.

## Contribuciones

Si deseas contribuir a este proyecto, envía un pull request con mejoras en los gráficos o análisis adicionales.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

--- 
