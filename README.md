# Edge-Computing
Este repositorio contiene los archivos de codigo para el segundo proyecto del curso Taller de Sistemas Embebidos, 
en el cual se utiliza un programa escrito en python para detección de emociones por medio de la cámara.

Funcionamiento:

Para la ejecución de dicho código se hace uso de las bibliotecas numpy, tensorflow, time, datatime, y opencv.
Para el funcionamiento de la detección de emociones se hace uso de un modelo preentrenado en tensorflow lite
correspondiente al archivo "model.tflite".

Para ejecutar el programa es necesario abrir el archivo emotions.py y tener una cámara disponible para poder realizar la
detección. Con esto definido, solo se debe ejecutar dicho archivo para llevar a cabo el programa y obtener un archivo excel 
donde se registran las emociones obtenidas y su tiempo de obtención, esto para su posterior análisis y procesamiento.

- EmotionTFlite.py: archivo principal para la ejecución del reconocimiento de emociones donde este realiza el llamado a los 
  otros 2 archivos incorporados en el repositorio

- model.tflite: Modelo preentrenado convertido en .tflite y optimizado para su ejecución

- haarcascade_frontalface_default.xml: archivo clasificador necesario para la ejecución del programa.

El código fuente es obtenido de:
A. Balaji, "Emotion-detection", 2021. [Online]. Disponible en: \url{https://github.com/atulapra/Emotion-detection}
