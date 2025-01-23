# Visualización de Desigualdad de Género en Latinoamérica

Este cuaderno tiene como objetivo explorar y visualizar las brechas de género en países de Latinoamérica utilizando datos de la **Encuesta de Igualdad de Género del Proyecto RP**. El análisis se centra en la sección **"Toma de decisiones y asignación de recursos"**, destacando desigualdades relacionadas con ingresos, educación y empleo.

## Descripción del Dataset

La **Encuesta de Igualdad de Género del Proyecto RP** fue realizada por Facebook en colaboración con el Banco Mundial, ONU Mujeres, Equal Measures 2030 y Ladysmith. La encuesta captura la dinámica de género en los hogares durante la pandemia de COVID-19, destacando tendencias globales y regionales.

### Variables Incluidas

- **Geography**: País donde se realizó la encuesta.
- **Question Code**: Código asociado a cada pregunta.
- **Question Text**: Texto de la pregunta realizada.
- **Response Category**: Categoría de respuesta ofrecida.
- **Response Variable**: Variable cuantitativa o categórica derivada de las respuestas.
- **Gender**: Género de la persona encuestada.
- **Value**: Valor asociado a la respuesta.

### Países Analizados
México, Argentina, Bolivia, Brasil, Chile, Colombia, Costa Rica, Ecuador, El Salvador, Guatemala, Haití, Honduras, Nicaragua, Panamá, Paraguay, Perú y Uruguay.

### Fuentes de Datos
El dataset completo está disponible en: [Equality at Home](https://www.equalityathome.org/).

## Contenido del Cuaderno

### 1. Introducción
Se proporciona una breve descripción del contexto y el propósito de este análisis, junto con el detalle de las variables clave incluidas en el dataset.

### 2. Carga y Limpieza de Datos
- **Carga de Datos**: Lectura del dataset en formato CSV.
- **Filtrado de Países**: Restricción de datos a los países de Latinoamérica mencionados.
- **Transformación de Datos**: Procesamiento de variables para asegurar la consistencia del análisis.

### 3. Análisis Descriptivo
Exploración inicial para comprender las tendencias generales, incluyendo:
- Distribución de respuestas por género.
- Identificación de preguntas más relevantes para ingresos, educación y empleo.

### 4. Visualizaciones de Brechas de Género
Se utilizan gráficos para representar visualmente las brechas de género en diferentes dimensiones:
- **Gráfico 1: Distribución de Respuestas por Género y País**  
  Muestra las respuestas categorizadas por género para una pregunta seleccionada.
- **Gráfico 2: Comparación Regional de Brechas en Ingresos**  
  Una comparación entre países de Latinoamérica basada en valores promedio.
- **Gráfico 3: Brechas de Género en Educación y Empleo**  
  Visualización específica de las brechas identificadas en estas áreas.

### 5. Conclusiones
Se resumen los hallazgos principales del análisis, destacando:
- Países con mayores desigualdades.
- Dimensiones con brechas más pronunciadas.
- Impacto potencial de las desigualdades observadas.

## Requisitos Previos

Para ejecutar este cuaderno, asegúrate de tener instaladas las siguientes bibliotecas de Python:
- `pandas`
- `matplotlib`
- `seaborn`

Puedes instalarlas usando el siguiente comando:
```bash
pip install pandas matplotlib seaborn
```

## Cómo Usar el Cuaderno

1. **Descarga los datos**: Asegúrate de tener el dataset correspondiente desde [Equality at Home](https://www.equalityathome.org/).
2. **Ubica los datos**: Coloca el archivo CSV en la misma carpeta que el cuaderno o actualiza la ruta en el código según sea necesario.
3. **Ejecuta el cuaderno**: Abre el archivo `.ipynb` en Jupyter Notebook, JupyterLab o Google Colab y sigue las celdas en orden.

## Visualizaciones Incluidas

### Ejemplo de Gráficos
#### Gráfico 1: Distribución de Respuestas por Género
Muestra las diferencias en cómo hombres y mujeres respondieron a preguntas clave en el cuestionario.

#### Gráfico 2: Comparación de Ingresos
Visualización de los valores promedio relacionados con ingresos por género y país.

#### Gráfico 3: Educación y Empleo
Análisis de las desigualdades de género en acceso a educación y oportunidades laborales.

## Contribuciones

Este análisis fue creado con el propósito de destacar desigualdades de género en la región de Latinoamérica durante la pandemia de COVID-19. Si encuentras mejoras o deseas contribuir, siéntete libre de enviar un pull request o reportar un issue.

---

## Licencia

Los datos utilizados son de dominio público y están disponibles en el sitio web oficial de [Equality at Home](https://www.equalityathome.org/). Este proyecto es de código abierto bajo la licencia MIT.
