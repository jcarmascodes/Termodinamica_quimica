# Ecuaciones de estado


---


Este es un archivo en donde se explica lo relacionado en las ecuaciones de estado, sólo consideraciones matemáticas detrás de ellos, así como algunas ecuaciones en donde se pueden obtener nuevas variables a partir de los resultados de las ecuaciobes polinomicas. También incluye una explicación acerca de las condiciones se deben usar ciertas ecuaciones de estado para obtener resultados más cerca de la realidad, tanto de compuestos puros, mezclas e incluso el cálculo de propiedades residuales.


**NOTA:**  
Como parte de la actualización del README, las ecuaciones así como los procedimientos para resolver cada caso de cada uno están descritos tanto en los archivos experimentales como en los ejemplos de funcionamiento, para hacer un simplificación en la redacción del mismo.


Incluye además soluciones a problemas a los códigos e instrucciones para modificaciones en el código para nuevos parámetros y propiedades termodinámicas que se puedan calcular a partir de las ecuaciones de estado.


**NOTA IMPORTANTE:** Para utilizar los códigos correspondientes al tópico es necesario tener las librerías de numpy y tabulate para iniciar los programas tanto los notebook jupyter (.ipynb) y archivo python (.py). Aunque es recomendado el uso de los archivos notebook como de este documento en donde se explica el funcionamiento de los códigos así como las formulas de cada ecuación de estado.


---


## _¿QUÉ ES UNA ECUACIÓN DE ESTADO?_


---
En los campos de física y química las ecuaciones de estado es una ecuación termodinamica que relaciona entre las diferentes variables termodinámicas que determinan cada estado de equilibrio de un sistema bajo diferentes condiciones físicas del mismo y los posibles valores que puedan tener.  

$\newline$

Las ecuaciones de estado en su forma en general están descritas de la siguiente manera:  


$$f(p,T,V)=0$$


En donde $p$ es la presión del sistema, $T$ es la temperatura del sistema y $V$ es el volumen del sistema. Sin embargo, para que sean manejables las variables sólo dos variables son independientes:


$$p=f(T,V)$$  


$$V=f(T,p)$$


Las ecuaciones de estado está directamente relacionada con la regla de fases de Gibbs , es decir, el número de variables independientes depende del número de sustancias y fases en el sistema. Una ecuación de estado entonces es el modelado de las condiciones del sistema mediante modelos que reflejan las relaciones que mostraron anteriormente; entonces cada ecuación de estado son modelos que se aplican en la escala microscópico o mediante aproximaciones empíricas a partir de datos experimentales, por lo que estos pueden ser considerados como ecuaciones fenomenológicas.  


$\newline$


La ecuaciones de estado puede utilizarse para evaluar muchas propiedades importantes tanto de sustancias puras como de mezclas como las siguientes: 1. _densidades entre las fases líquida y vapor_; 2. _presión de vapor_; 3. _propiedades críticas de las mezclas_; 4. _relaciones de equilibrio vapor-líquido_; 5. _desviación de la entalpía con respecto a la idealidad_; y 6. _desviación de la entropía con respecto a la idealidad_.  

$\newline$

![IMA_edo-01](https://github.com/user-attachments/assets/dae06bba-0a42-4b5b-b5c8-819cb7d9a635)


Imagen 1: La utilización de las ecuaciones de estado es útil para la creación de diagramas de fase en donde se puede identificar los cambios del estado físico de un compuesto puro o en mezcla, es utilizado en la rama ingeniería de procesos relacionado con la ingeniería química y otras área de estudio.  

$\newline$

En la actualidad no hay ecuación de estado que pueda describir con exactitud el comportamiento de todas las sustancias en todas las condiciones, sin embargo, es necesario saber cuáles ecuaciones se adaptan mejor a las condiciones en las que se encuentre las diferentes sustancias. Otro detalle a considerar es que cada ecuación de estado son aproximaciones del comportamiento del sistema por lo que está asociada a un cierto grado de exactitud con respecto a las mediciones de las condiciones reales.


---


