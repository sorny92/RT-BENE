RT-BENE: detección de parpadeo

pandoc -f odt -t markdown README.odt -o readme.md

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
clases en el dataset y se utiliza aumentación de datos para corregir la
sobre-representación de la clase "no parpadeo" con respecto a
"parpadeo".

En este proyecto se consigue un F1-score de 0.99 en el testset.

Introducción
============

Métodos
=======

Resultados
==========

Conclusiones
============
