# USFQ - MMIA-6021 Taller de NLP: Traductor Inglés-Español con Flask y NLLB

Este repositorio contiene los materiales y código del taller de Procesamiento de Lenguaje Natural (NLP) donde implementamos una aplicación web de traducción utilizando el modelo NLLB (No Language Left Behind) de Meta y Flask.

## 📋 Descripción

Esta aplicación permite traducir texto entre inglés y español utilizando el modelo NLLB de Meta, uno de los modelos de traducción de código abierto más avanzados. La interfaz web está construida con Flask, permitiendo a los usuarios interactuar fácilmente con el modelo.

## 🚀 Características

- Traducción bidireccional entre inglés y español
- Interfaz web simple y accesible
- Cambio de dirección de traducción con un solo clic
- Basado en el modelo NLLB-200 de Meta (versión ligera de 600M parámetros)
- Soporte para textos largos (hasta 400 tokens)

## 💻 Tecnologías utilizadas

- **Python 3.12+**
- **Flask**: Framework web ligero
- **Flask-CORS**: Para manejo de Cross-Origin Resource Sharing
- **Transformers (Hugging Face)**: Para acceder al modelo NLLB
- **PyTorch**: Como backend para el modelo
- **Jupyter Notebook**: Para desarrollo y demostración

## 🛠️ Instalación

1. Clona este repositorio:
   
   ```bash
   git clone https://github.com/tu-usuario/taller-nlp-traductor.git
   cd taller-nlp-traductor
   ```

2. Crea un entorno virtual:
   
   ```bash
   python -m venv flask_venv
   source flask_venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. Instala las dependencias:
   
   ```bash
   pip install flask flask-cors transformers torch
   
   # Tambien puede ser: pip install -r requirements.txt
   ```

4. Asegúrate de crear la carpeta "templates" y añadir el archivo HTML:
   
   ```bash
   mkdir templates
   # Crea el archivo templates/page.html con tu interfaz
   ```

## 📊 Uso

1. Inicia la aplicación desde Jupyter Notebook:
   
   ```python
   # Ejecuta el notebook flask_translate.ipynb
   ```

2. Abre tu navegador y accede a: `http://localhost:5555`

3. Escribe el texto a traducir y haz clic en el botón de traducción.

4. Para cambiar la dirección de traducción (español→inglés o inglés→español), utiliza el botón correspondiente.
   
   ![93119c34-26be-4dba-90d7-1cc19679e28c](https://github.com/Erwin-d3v/MMIA6021-NLP-Taller-3/blob/main/screen_capture.png)

## 🔄 Flujo de trabajo

1. El usuario ingresa texto en el idioma de origen
2. La aplicación envía el texto al servidor Flask
3. El modelo NLLB procesa la traducción
4. El resultado se muestra en la interfaz web

## 🔧 Personalización

Puedes modificar el modelo utilizado cambiando la variable `model_name`:

```python
# Versión compacta (predeterminada)
model_name = "facebook/nllb-200-distilled-600M"

# Para mejor calidad (requiere más recursos)
# model_name = "facebook/nllb-200-3.3B"
```

## ⚠️ Consideraciones

- Esta es una aplicación de desarrollo, no está optimizada para producción
- El primer uso de traducción puede tardar unos segundos mientras se carga el modelo
- Para un despliegue en producción, considera usar un servidor WSGI como Gunicorn o uWSGI

## 📝 Notas del taller

Este proyecto forma parte de un taller de NLP para demostrar:

- Cómo implementar modelos de transformers en aplicaciones web
- La integración de Flask con modelos de ML
- El uso de la biblioteca transformers de Hugging Face
- Ejemplos prácticos de aplicaciones NLP

## 🔗 Referencias

- [Modelo NLLB de Meta](https://ai.meta.com/research/no-language-left-behind/)
- [Documentación de Hugging Face Transformers](https://huggingface.co/docs/transformers/)
- [Flask Documentation](https://flask.palletsprojects.com/)

## 👥 Contribuciones

Las contribuciones son bienvenidas. Si encuentras algún error o tienes una mejora, no dudes en abrir un issue o enviar un pull request.
