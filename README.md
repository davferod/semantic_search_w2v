---

# Proyecto de Búsqueda Semántica con Word2Vec y Gradio

Este proyecto implementa un sistema de búsqueda semántica utilizando **Word2Vec** para generar representaciones vectoriales de los textos y calcular la similitud entre ellos mediante **similitud de coseno**. Incluye una interfaz gráfica interactiva construida con **Gradio** para facilitar la interacción con el sistema de búsqueda.

## Tecnologías y Librerías Utilizadas

- **Python**: Lenguaje principal del proyecto.
- **Pandas**: Para la manipulación y procesamiento de datos tabulares.
- **Gensim (Word2Vec)**: Para el entrenamiento de un modelo de embeddings de palabras.
- **NumPy**: Para operaciones numéricas y manipulación de arrays.
- **scikit-learn**: Para el cálculo de similitud de coseno.
- **NLTK (Natural Language Toolkit)**: Para la tokenización de texto.
- **Gradio**: Para la creación de una interfaz gráfica de usuario que permite realizar consultas de búsqueda de manera interactiva.

## Funcionalidades del Proyecto

1. **Generación de Embeddings con Word2Vec**:
   - El script entrena un modelo de embeddings de palabras con **Word2Vec** utilizando datos de texto tokenizados.
   - Cada documento es representado como un vector que es el promedio de los embeddings de las palabras que contiene.

2. **Sistema de Búsqueda Semántica**:
   - A través de la similitud de coseno, el sistema calcula la proximidad entre la consulta de búsqueda y cada documento en la base de datos.
   - Los resultados se ordenan por relevancia según la similitud calculada.

3. **Reentrenamiento Opcional**:
   - El modelo Word2Vec se puede reentrenar dinámicamente con las palabras de las nuevas consultas para adaptarse a vocabularios y contextos cambiantes.

4. **Interfaz Gráfica con Gradio**:
   - Una interfaz amigable para el usuario, donde se puede ingresar una consulta de búsqueda y visualizar los resultados de manera ordenada por relevancia.

## Temas Abordados

Este proyecto cubre los siguientes temas de interés en **procesamiento de lenguaje natural (NLP)** y **aprendizaje automático**:

- Embeddings de palabras y representación semántica de texto.
- Técnicas de similitud de texto, especialmente similitud de coseno.
- Integración de modelos de NLP en una interfaz gráfica interactiva.
- Reentrenamiento de modelos en función de la retroalimentación del usuario.

## Cómo Ejecutar el Proyecto

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
   cd tu_repositorio
   ```

2. **Instalar las dependencias**:
   Asegúrate de tener Python instalado y luego instala las librerías necesarias:
   ```bash
   pip install pandas gensim numpy scikit-learn nltk gradio
   ```

3. **Preparar los datos**:
   - Coloca un archivo `texto.csv` en el mismo directorio del script.
   - Este archivo debe tener una columna llamada `texto` que contenga los documentos o frases para el sistema de búsqueda.

4. **Ejecutar el script**:
   ```bash
   python nombre_del_script.py
   ```

5. **Interfaz de Búsqueda**:
   Una vez ejecutado, se abrirá una interfaz en el navegador gracias a Gradio, donde podrás ingresar consultas de texto y ver los resultados ordenados por similitud.

## Ejemplo de Uso

1. Ingresa un texto en la caja de búsqueda en la interfaz de Gradio.
2. Haz clic en el botón de "Preguntar".
3. Observa los resultados de búsqueda más relevantes, clasificados según la similitud semántica con la consulta.

## Estructura del Código

- **`embed_text`**: Carga los datos y entrena el modelo Word2Vec en los textos, generando embeddings para cada documento.
- **`buscar`**: Calcula la similitud entre una consulta de búsqueda y los documentos, utilizando los embeddings generados.
- **`buscar_wrapper`**: Función auxiliar para adaptar la función de búsqueda a Gradio.
- **Interfaz de Gradio**: Proporciona un entorno interactivo para que el usuario pueda realizar búsquedas.

## Contribuciones

Si deseas mejorar el proyecto o añadir nuevas funcionalidades, siéntete libre de hacer un fork del repositorio y enviar un pull request.

---
