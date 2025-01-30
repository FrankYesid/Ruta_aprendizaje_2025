# Análisis de Sentimiento del Engagement de Noticias

Este proyecto tiene como objetivo preprocesar datos de redes sociales para realizar un análisis de sentimiento. Se trabaja con bases de datos provenientes de diversas fuentes de noticias para analizar su interacción y engagement en redes sociales.

## 📂 Estructura del Proyecto

```
.
├── data/                    # Carpeta que contiene los archivos CSV con los datos de las noticias
│   ├── al_jazeera.csv       # Datos de la agencia de noticias Al Jazeera
│   ├── bbc.csv              # Datos de la BBC
│   ├── cnn.csv              # Datos de CNN
│   ├── reuters.csv          # Datos de Reuters
├── notebooks/               # Cuadernos de Jupyter con el análisis
│   ├── analisis_sentimiento_noticias.ipynb  # Cuaderno principal con el flujo de trabajo
├── src/                     # Código fuente para procesamiento de datos
│   ├── preprocessing.py     # Funciones para limpiar y procesar los textos
│   ├── visualization.py     # Funciones para generar visualizaciones
├── README.md                # Documento actual
```

## 📜 Descripción del Proceso

### 1️⃣ Carga de Datos
Se cargan los archivos CSV que contienen publicaciones de redes sociales relacionadas con diferentes agencias de noticias. Cada archivo tiene las siguientes columnas:

- **text**: Contenido de la publicación.
- **likes**: Cantidad de "me gusta" recibidos.
- **comments**: Número de comentarios.
- **shares**: Veces que se compartió la publicación.

### 2️⃣ Lectura y Exploración de Datos
Se realiza una inspección inicial para entender la estructura y calidad de los datos:
- Vista previa de los primeros registros.
- Dimensiones de los datasets.
- Identificación de valores nulos y tipos de datos.

### 3️⃣ Procesamiento de Texto
Para preparar los textos para el análisis de sentimiento, se aplican las siguientes técnicas:
- Eliminación de caracteres especiales y URLs.
- Conversión a minúsculas.
- Eliminación de palabras vacías (stopwords).
- Tokenización y lematización.

### 4️⃣ Análisis Descriptivo
Se analizan las estadísticas generales de engagement:
- Distribución de "likes", "comments" y "shares".
- Comparación entre las diferentes agencias de noticias.
- Relación entre el sentimiento del texto y la cantidad de interacciones.

### 5️⃣ Visualización de Datos
Se generan diversas gráficas para interpretar los patrones encontrados:
- Histogramas de interacciones.
- Nubes de palabras por agencia de noticias.
- Distribución de sentimiento de los textos.

### 6️⃣ Análisis de Sentimiento
Se utiliza un modelo de NLP para clasificar los textos en:
- Positivos 😊
- Neutrales 😐
- Negativos 😠

Se comparan los resultados entre las distintas agencias de noticias y se estudia la influencia del sentimiento en la cantidad de interacciones.

## 📊 Resultados Esperados
- Identificación de patrones en la respuesta de los usuarios a diferentes tipos de noticias.
- Relación entre el sentimiento de las publicaciones y su nivel de engagement.
- Comparación entre las distintas agencias de noticias en términos de interacción en redes sociales.

## 🚀 Ejecución del Proyecto
Para ejecutar el código en local:
1. Clonar el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd <NOMBRE_DEL_PROYECTO>
   ```
2. Instalar dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Ejecutar el notebook en Jupyter:
   ```bash
   jupyter notebook notebooks/analisis_sentimiento_noticias.ipynb
   ```

## 📢 Contribuciones
Si deseas contribuir al proyecto, no dudes en hacer un fork y enviar un pull request.

---

📌 **Autor:** Frank Yesid
📅 **Fecha:** 2025
📍 **Repositorio:** [GitHub - Análisis de Sentimiento en Noticias](#)

