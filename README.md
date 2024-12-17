# Creación de Sistemas RAG sobre Bases de Datos Vectoriales

Este repositorio está diseñado para implementar diferentes sistemas **RAG (Retrieved Augmented Generation)** utilizando bases de datos vectoriales. El objetivo principal de este ejercicio es integrar un **Large Language Model (LLM)** y una base de datos propia para responder preguntas formuladas por el usuario, mediante la generación aumentada por recuperación.

El proyecto consta de varios apartados que cubren distintas formas de crear sistemas RAG. A continuación, se detallan los apartados que forman este ejercicio:

## Descripción

Los sistemas RAG combinan la capacidad de los modelos de lenguaje de generar respuestas coherentes y útiles con la habilidad de recuperar información relevante de una base de datos. En este caso, se utilizan diferentes fuentes de datos (páginas web, documentos PDF, MongoDB Atlas) y se combinan con modelos LLM para proporcionar respuestas precisas a las consultas de los usuarios.

## Apartados del ejercicio

Este ejercicio está compuesto por los siguientes apartados:

### 1. RAG en inglés que crea un vector store a partir de datos dunha páxina web

En este apartado, se crea un sistema RAG utilizando datos extraídos de una página web en inglés. El sistema obtiene el contenido de la página, lo divide en fragmentos y luego crea un **vector store** para realizar búsquedas semánticas y generar respuestas a las preguntas del usuario.

#### Pasos:
1. Extraer el contenido de una página web en inglés.
2. Dividir el contenido en fragmentos pequeños.
3. Crear un vector store utilizando los embeddings de HuggingFace o un modelo similar.
4. Implementar la generación de respuestas utilizando el sistema RAG.

### 2. RAG en castelán que crea un vector store a partir de un ou varios ficheiros PDF

En este apartado, se desarrolla un sistema RAG que trabaja con documentos PDF en español. El sistema procesa los archivos PDF, los convierte a texto y luego los divide en fragmentos que se almacenan en un vector store. Posteriormente, el sistema puede generar respuestas basadas en el contenido de los documentos.

#### Pasos:
1. Extraer el contenido de uno o más archivos PDF.
2. Dividir el texto extraído en fragmentos.
3. Crear un vector store utilizando los embeddings de los documentos.
4. Implementar la generación de respuestas utilizando el sistema RAG.

### 3. Crear una GUI para un dos RAGs anteriores

En este apartado, se crea una interfaz gráfica de usuario (GUI) que permite a los usuarios interactuar fácilmente con el sistema RAG. La GUI puede ser desarrollada usando bibliotecas como `Tkinter`, `Streamlit` o cualquier otra herramienta adecuada.

#### Pasos:
1. Crear una interfaz gráfica que permita al usuario ingresar consultas.
2. Visualizar las respuestas generadas por el sistema RAG.
3. Facilitar la carga de archivos (si es necesario) o la entrada de una URL.
   
### 4. RAG contra Mongo Atlas

Este apartado involucra la implementación de un sistema RAG que utiliza MongoDB Atlas como base de datos vectorial. El sistema almacena los documentos en MongoDB Atlas y utiliza el **MongoDB Atlas Vector Search** para realizar consultas semánticas y generar respuestas a preguntas específicas.

#### Pasos:
1. Conectar con MongoDB Atlas y configurar la base de datos.
2. Crear un vector store en MongoDB Atlas utilizando embeddings de HuggingFace o modelos similares.
3. Almacenar los documentos en la base de datos vectorial.
4. Realizar consultas y generar respuestas usando un modelo LLM.

## Estructura del Repositorio

El repositorio contiene los siguientes directorios y archivos:

### Descripción de los directorios:

- **/RAG-Web**: Contiene el código para la implementación de un sistema RAG que utiliza una página web en inglés como fuente de datos.
- **/RAG-PDF**: Contiene el código para crear un sistema RAG basado en archivos PDF en español.
- **/RAG-GUI**: Contiene el código para la creación de una interfaz gráfica de usuario que permite interactuar con uno de los sistemas RAG.
- **/RAG-MongoAtlas**: Contiene el código para crear un sistema RAG que utiliza MongoDB Atlas como base de datos vectorial.

## Instrucciones de Uso

1. **Instalar dependencias**:
    Para cada notebook, es necesario instalar las dependencias. Puedes hacerlo ejecutando el siguiente comando dentro de cada carpeta correspondiente:

    ```bash
    pip install -r requirements.txt
    ```

2. **Ejecutar los notebooks**:
    Los notebooks están listos para ser ejecutados. Abre los notebooks correspondientes en Jupyter Notebook o en cualquier entorno compatible para empezar a trabajar con ellos.

3. **Crear la GUI**:
    Si deseas probar la interfaz gráfica, navega a la carpeta `/RAG-GUI` y ejecuta el archivo `gui_app.py`:

    ```bash
    python gui_app.py
    ```

4. **Conectar a MongoDB Atlas**:
    Para el apartado que utiliza MongoDB Atlas, asegúrate de tener configurada una cuenta en MongoDB Atlas y reemplaza los valores de conexión en el código. Además, habilita la funcionalidad de búsqueda vectorial en tu base de datos de Atlas.


Usa el archivo rag.yml para exportar el environment ya creado y poder utilizarlo
conda env create --file rag.yml
