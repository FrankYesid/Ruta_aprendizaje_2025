```markdown
# Extracción de Texto de Imágenes con OCR

Este proyecto utiliza la biblioteca OpenCV y Tesseract OCR para extraer texto de imágenes, aplicar técnicas de preprocesamiento y almacenar los resultados de manera ordenada. 

## Descripción

El objetivo del proyecto es procesar imágenes que contienen texto, extraer la información textual y organizarla para su análisis posterior. Las principales etapas incluyen:

1. **Lectura de la Imagen**: Carga de la imagen desde el sistema de archivos.
2. **Preprocesamiento**: Conversión a escala de grises y aplicación de umbral para resaltar áreas de texto.
3. **Segmentación de Texto**: Identificación de bloques de texto mediante contornos.
4. **Extracción de Texto**: Uso de Tesseract OCR para convertir los bloques de texto en cadenas legibles.
5. **Ordenamiento y Almacenamiento**: Ordenar el texto extraído y guardarlo en un archivo de texto.

## Requisitos Previos

1. Python 3.7 o superior.
2. Instalación de las siguientes bibliotecas:
   - OpenCV
   - Pytesseract
   - Matplotlib

3. Tesseract OCR debe estar instalado en el sistema:
   - [Descargar Tesseract OCR](https://github.com/tesseract-ocr/tesseract)

## Instalación

1. Clonar este repositorio:
   ```bash
   git clone https://github.com/FrankYesid/Ruta_aprendizaje_2025.git
   cd Ruta_aprendizaje_2025/02-Tratamiento_de_Datos/Proyecto_3
   ```

2. Crear un entorno virtual e instalar las dependencias:
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Configurar la ruta de instalación de Tesseract en el script:
   ```python
   pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
   ```

## Estructura del Proyecto

```
extraccion-ocr/
├── resources/
│   └── text_images/
│       └── paragraph4.jpeg   # Imagen de ejemplo para OCR
├── extraccion_texto_ocr.ipynb  # Cuaderno Jupyter con el código completo
├── recognized.txt            # Salida de texto extraído
├── README.md                 # Documentación del proyecto
└── requirements.txt          # Dependencias necesarias
```

## Cómo Usar

1. Abre el cuaderno `extraccion_texto_ocr.ipynb` en Jupyter Notebook.
2. Sigue las secciones paso a paso:
   - Carga de la imagen.
   - Preprocesamiento de la imagen.
   - Extracción y segmentación del texto.
   - Almacenamiento del texto extraído en un archivo `.txt`.

3. Ejecuta las celdas y visualiza los resultados en tiempo real.

## Resultados Esperados

- Visualización del proceso de preprocesamiento: imágenes en escala de grises, umbral aplicado, y áreas de texto resaltadas.
- Archivo `recognized.txt` con el texto extraído y ordenado.

## Ejemplo de Salida

El contenido del archivo `recognized.txt` podría ser similar a:
```
Texto extraído bloque 1
Texto extraído bloque 2
...
```

## Visualización

Al ejecutar el código, se mostrarán ventanas con:
- Imagen original en escala de grises.
- Imagen procesada con las áreas de texto resaltadas.

## Notas Adicionales

- El rendimiento del OCR puede variar dependiendo de la calidad de la imagen. Se recomienda usar imágenes de alta resolución.
- Ajusta los parámetros de preprocesamiento según las características de tus imágenes para mejores resultados.

---

¡Explora este proyecto y personalízalo para tus necesidades de análisis de texto!
```
