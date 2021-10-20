# Edge-Computing
Este repositorio contiene los archivos de codigo para el segundo proyecto del curso Taller de Sistemas Embebidos, 
en el cual se utiliza un programa escrito en python para detección de emociones por medio de la cámara.

Funcionamiento:

Para la ejecución de dicho código se hace uso de las bibliotecas numpy, tensorflow, time, datatime, y opencv.
Para el funcionamiento de la detección de emociones se hace uso de un modelo preentrenado en tensorflow lite
correspondiente al archivo "model.tflite".

Para ejecutar el programa es necesario abrir el archivo Emotions.py y tener una cámara disponible para poder realizar la
detección. Con esto definido, solo se debe ejecutar dicho archivo para llevar a cabo el programa y obtener un archivo excel 
donde se registran las emociones obtenidas y su tiempo de obtención, esto para su posterior análisis y procesamiento.

- EmotionTFlite.py: archivo principal para la ejecución del reconocimiento de emociones donde este realiza el llamado a los 
  otros 2 archivos incorporados en el repositorio
  
- Conversion.py: archivo para realizar la conversión de un modelo preentrenado a un modelo que utilice tensorflow lite.

- model.h5: Modelo preentrenado para el reconocimiento de emociones. A este archivo se le realiza la conversión a .tflite.

- model.tflite: Modelo preentrenado convertido en .tflite y optimizado para su ejecución

- haarcascade_frontalface_default.xml: archivo clasificador necesario para la ejecución del programa.

Ademá, se agregan las recetas utilizadas en la capas del Yocto Project, lo cual es necesario para crear la imagen. Una vez 
integrada las capas y las modificaciones necesarias en la recetas se utiliza 2 comandos para cocinar la imagen:

- source oe-init-env
- time bitbake core-image-sato

Una vez realizado esto, se cocina la imagen en la tarjeta SD para la integración en la Raspberry, donde se debe ubicar el archivo
.rpi-sdimg, el cual se encuentra en la dirección /build/tmp/deploy/images/raspberrypi3/. Una vez localizado, se realiza el siguiente comando:

- sudo dd if=./core-image-sato-raspberrypi3.rpi-sdimg of=/dev/sdb

Con esto, ya se puede probar el código dentro de la Raspberry Pi 2

El código fuente es obtenido de:
A. Balaji, "Emotion-detection", 2021. [Online]. Disponible en: https://github.com/atulapra/Emotion-detection
