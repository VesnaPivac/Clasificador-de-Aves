# Clasificador de Aves con Transfer Learning

Este proyecto tiene como objetivo implementar transfer learning utilizando un dataset de aves obtenido de Kaggle. El dataset, disponible en Kaggle [BIRDS 525 SPECIES- IMAGE CLASSIFICATION](https://www.kaggle.com/datasets/gpiosenka/100-bird-species?resource=download&select=birds.csv), será utilizado para crear un entregable para la materia de Redes Neuronales Profundas de la Maestría en Ciencia de Datos en la Universidad de Sonora.

## Descripción del Proyecto
El clasificador de aves utiliza técnicas de transfer learning para adaptar un modelo preentrenado a la clasificación de aves en múltiples categorías. Este proyecto representa un enfoque end-to-end (E2E), desde la adquisición y preparación de datos hasta la implementación y evaluación del modelo.

## Estructura de los Datasets
El proyecto utiliza tres conjuntos de datos de aves con la siguiente estructura:
- **Conjunto de Entrenamiento**: Contiene 85835 archivos pertenecientes a 525 clases diferentes de aves.
- **Conjunto de Prueba**: Incluye 3035 archivos distribuidos en las mismas 525 clases utilizadas en el conjunto de entrenamiento.
- **Conjunto de Validación**: Posee 2625 archivos pertenecientes a 525 clases de aves

## Estructura del Repositorio
- **index.html**: Archivo HTML que contiene la estructura y código para la página web del clasificador de aves. Se encarga de cargar el modelo TensorFlow.js y permite la interacción con la cámara para clasificar imágenes en tiempo real.
- **model.json**: Archivo que contiene la arquitectura del modelo EfficientNetV2B3.
- **functions.js**: Archivo JavaScript con funciones para el procesamiento de cámaras y predicción de aves en tiempo real.
- **clases.json**: Archivo JSON con las clases de aves utilizadas para la clasificación.
- **PF-ClasificadorAvesFinal.ipynb**: Libreta Jupyter (Jupyter Notebook) donde se realizó el desarrollo del modelo de clasificación de aves. Incluye el código para entrenar el modelo, cargar datos, preprocesamiento y evaluación del modelo.
- **README.md**: Este archivo que proporciona información sobre el proyecto y su estructura.

## Uso del Proyecto
Clona el repositorio en tu máquina local.
Instala las dependencias necesarias (TensorFlow, etc.).
Ejecuta el archivo index.html en un navegador para acceder al clasificador de aves en tiempo real.
Explora la libreta PF-ClasificadorAvesFinal.ipynb para ver el proceso de desarrollo del modelo y la conversión a TensorFlow.js.

## Implementación
### Para la versión web:
1. En el directorio del proyecto, ejecuta el siguiente comando en la línea de comandos:
   ```bash
    python -m http.server 8000
   ```
   Esto iniciará un servidor local en el puerto 8000.
2. Abre tu navegador web y accede a la siguiente ruta: http://localhost:8000/index.html
    Esto te llevará a la interfaz web de la aplicación.

<p align="center">
  <img src="https://github.com/VesnaPivac/Clasificador-de-Aves/raw/main/index.jpg" alt="Texto Alternativo">
</p>

### Para la versión móvil:
1. Crea una cuenta en [ngrok](https://ngrok.com/).
2. Después de crear tu cuenta, copia tu token de autenticación proporcionado por ngrok.
3. En la consola de comandos, ejecuta el siguiente comando para configurar tu token de autenticación en ngrok:
  ```bash
  ngrok config add-authtoken <token>
  ```
  Asegúrate de reemplazar `<token>` con tu token de autenticación.
4. Luego, ejecuta el siguiente comando para iniciar el túnel y exponer tu servidor local:
  ```bash
  ngrok http 8000
  ```
  Esto generará un enlace de acceso público que podrás usar en dispositivos móviles.
5. Copia el enlace de "forwarding" proporcionado por ngrok y accede a él desde tu dispositivo móvil para comenzar a utilizar la aplicación.







<br>

*Basado en el repositorio [Exportación Perros Gatos](https://github.com/ringa-tech/clasificador-perros-gatos/tree/main) de Ringa Tech.*
