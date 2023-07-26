# Object-Detection-Android-app

Modificación y actualización frente a errores del codigo del repositorio tomado de : [Movil-Object-Detection](https://github.com/FerJeffQ/Movil-Object-Detection) en donde toda la explicacion esta en el video de [Youtube](https://www.youtube.com/watch?v=zLV6LiqTIOA) , el dataset es tomado de [roboflow](https://public.roboflow.com/object-detection/oxford-pets) e imagenes y anotaciones en [Drive](https://drive.google.com/drive/folders/13wDSgwha6WNhiQFHXr2zIjnxaaVAl-TY).


<p align="center">
  <a href="https://www.youtube.com/watch?v=zLV6LiqTIOA">
    <img src="https://i.ytimg.com/vi/zLV6LiqTIOA/hqdefault.jpg?sqp=-oaymwEcCOADEI4CSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLBkNRiSwgA9c4bnJLeOJLvIcGdeFw" alt="Como crear tu propio DETECTOR DE OBJETOS para Android | Tensorflow Tutorial">
  </a>
</p>




<p align="justify">
    En el cual se detectan gatos y perros como se ve en la siguiente imagen 
</p>

<p align="center">
  <img src="README-images\app-tensorflowlite.jpg" width="350" height="700" alt="StepLast">
</p>

<p align="justify">
    Para implementar la aplicacion en android es necesario tener Android Studio , en se debe de descarcarg la carpeta "android_tensoflowlite" o realizar git clone a este repositorio 
</p>
<p align="justify">
    Abrir con Android Studio el proyecto pero en "build.gradle" para que se carguen todas las dependencias 
</p>

<p align="center">
  <img src="README-images\open-project.PNG"  alt="StepLast">
</p>

<p align="justify">
    Verifica el modelo que deseas utilizar en la carpeta "assets" en este caso el de gatos y perros se nombró "model_fp16_meta.tflite"  y que en el archivo ObjectDetectorHelper en la linea 85 tengan el mismo  nombre , si deseas usar otro modelo realizado seria ponerlo en la carpeta assets y poner el nombre del archivo en la linea 85 de ObjectDetectorHelper
</p>

<p align="center">
  <img src="README-images\android-model.PNG"   alt="StepLast">
</p>

<p align="justify">
    Para dar Run al proyecto recuerda que el celular debe estar en modo desarrolador y tener depuracion de USB , si no sabes como hacerlo aqui dejo un enlace </p>
    
[video habilita modo desarrolador y tener depuracion de USB , si no sabes como hacerlo aqui dejo un enlace](https://www.youtube.com/watch?v=yXpTkSpnmfM)

----
### Para usar 5 clases o diferentes clases 
<p align="justify">
    Modificar "labelmap.txt" e insertar la clases a detectar por ejemplo si son 5 clases 'cat', 'dog', 'Chair', 'Sofa', 'Table'  seria el archivo labelmap.txt de esta manera </p>
  
<p align="center">
  <img src="README-images\labels.PNG"   alt="StepLast">
</p>



<p align="justify">
    Según el numero de datos de validación , modificar la caja 11 del codigo .ipynb por ese valor de numero de datos de validación</p>

<p align="center">
  <img src="README-images\datos-validation.PNG"   alt="StepLast">
</p>

<p align="justify">
    Modificar el archivo "pipeline_nuevo.config" en la linea 3 , por el numero de clases a detectar </p>

<p align="center">
  <img src="README-images\class-num.PNG"   alt="StepLast">

<p align="justify">
    Recuerda que si vas a usar Tensorboard , habilita cookies</p>
</p>

<p align="center">
  <img src="README-images\tensorboard.PNG"   alt="StepLast">

  <p align="justify">
    Puedes usar en el colab el archivo "requirements.txt" para dependencia usadas en este notebook </p>
</p>