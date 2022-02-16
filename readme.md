# RT-BENE: detección de parpadeo

[Link](informe.pdf) al trabajo entero.

Resumen
=======

Se generan dos modelos para la resolución del problema de detección de
parpadeo.

El primero es un modelo ingenuo en el cual no tengo en cuenta la
distribución de datos. Se selecciona un modelo de los disponibles en el
zoo de Keras por simplicidad. Además el modelo está preentrenado en
*Imagenet.*

El segundo modelo está también basado en un modelo preentrenado de Keras
pero en este caso sí que se tiene en cuenta la distribución de las
clases en el dataset y se utilizan técnicas de aumento de datos para
corregir la sobre-representación de la clase "no parpadeo" con respecto
a "parpadeo".

En este proyecto se consigue un F1-score de 0.99 en el testset.

Introducción
============

Se utiliza el conjunto de datos RT-BENE, este consiste en 107350 parejas
de imágenes y su correspondiente etiqueta.\
Cada pareja de imágenes contiene dos imágenes RGB de tamaño 36x60
pixeles de los ojos de diferentes personas. En total, el dataset,
contiene 17 videos cada uno de una persona diferente donde se ha anotado
en cada imagen si está parpadeando o no.

El problema a solucionar es la predicción por cada par de imágenes si
estas corresponden a un parpadeo o no. Dicho problema se puede
considerar como un problema de clasificación donde hay que predecir si
para dicha entrada se corresponde una clase u otra. En este caso como
solo hay una salida se define como clasificación binaria.

