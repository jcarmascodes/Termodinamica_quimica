# Ecuaciones de estado


---


Este es un archivo en donde se explica lo relacionado en las ecuaciones de estado, sólo consideraciones matemáticas detrás de ellos, así como algunas ecuaciones en donde se pueden obtener nuevas variables a partir de los resultados de las ecuaciobes polinomicas. También incluye una explicación acerca de las condiciones se deben usar ciertas ecuaciones de estado para obtener resultados más cerca de la realidad, tanto de compuestos puros, mezclas e incluso el cálculo de propiedades residuales.


#### **________NOTA IMPORTANTE________**


* Para utilizar los códigos correspondientes al tópico es necesario tener las librerías de numpy y tabulate para iniciar el programa en el archivo notebook jupyter (.ipynb).
* Es recomendable utilizar programas que puedan visualizar y editar los archivos notebook como lo es entorno _Anaconda_, _Google Colab_, _Visual Studio Code_ y similares, en caso de que se requiera ejecutar este código exclusivamente en un archivo de python (.py) es necesario realizar las adecuaciones necesarios para para unificar todas las partes de los códigos.
* Para consultar información especifica para resolución de posibles problemas con los códigos (tablas de resultados, librerías, etc.) revise el apartado de información adicional al final del _README_.


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


## _CONSTANTE UNIVERSAL DE LOS GASES: RELACIÓN ENTRE LA ESCALA MICROSCÓPICA Y MACROSCÓPICA_


---


A diferencia de realizar medidas a como lo hariamos con instrumentos básicos como la balanza o recipientes usando objetos manipulables, es decir, a una escala macroscópica. 

$\newline$

<img width="750" height="588" alt="png-clipart-matter-macroscopic-scale-chemistry-molecule-length-scale-others-glass-angle" src="https://github.com/user-attachments/assets/d995030c-2cec-4ca9-91bd-de45cca118dd" />



Imagen 2: En la escala macroscópica es referido a los objetos que están una escala que se puede medir y manipular utilizando los instrumentos que se usan de manera convencional como lo es tornillo o la bota, pero cuando es referido la escala microscópica en termodinámica se habla a escala molecular como lo es una estructura formando una red molecular ya sea por la interacciones por enlaces metálicos como red de entrecruzamiento en los polímeros.

$\newline$

Pero, sin embargo, a nivel molecular es totalmente diferente debido a las limitaciones de poder medir diferentes variables físicas con los instrumentos de forma convencional a esa escala que se denomina como microscópico. En cambio, hay otras variables con sus respectivas magnitudes físicas que se necesita convertir de la escala microscópica a la macroscópica, por ejemplo, la energía que se necesita en la transformación de especies químicas a otras o incluso medir otras variables termodinámicas relacionadas con las interacciones tanto moleculares e intermoleculares entre las mismas; por ello mediante el uso de constantes físicas ayudaron a establecer relaciones matemáticas y conceptuales para tener una comprensión de las interacciones moleculares y cómo se podía medir esas transformaciones que conlleva a la transformación de esa información de una escala microscópica a una escala macroscópica.


Entre las diferentes constantes se encuentran la constante de Boltzmann ($k_{B}$) que relaciona las magnitudes de la escala molecular en términos de energía y la variación este mismo , el número de Avogadro ($N_{A}$) que relaciona una magnitud númerica de una escala molecular a una escala que se puede medir como la masa y el volumen de compuestos. Sin embargo, cuando se trata de fluidos es necesario tener ambas relaciones para medir las propiedades y medidas termodinámicas por ello en la definición de la constante universal de los gases se incluye la siguiente relación:


$$R = N_{A} k_{B}  $$
    

$$R = (6.023 x 10^{23} mol^{-1}) (1.3806 x 10^{-23} \dfrac{J}{K})$$


$$R = 8.3145\dfrac{J}{mol K}$$


A partir de esta variable, se realizaron otras conversiones a otras unidades medida entre las del Sistema Internacional como las del Sistema Inglés y con ello se han realizado diferentes ecuaciones para describir el comportamiento de sistemas químicos y físicos, incluyendo las que se ocupan en las ecuaciones de estado y ecuaciones aplicados a la ingeniería química.


---


### INFORMACIÓN ADICIONAL


1. TABLAS DE LOS RESULTADOS (LIBRERIA [_tabulate_](https://pypi.org/project/tabulate/))


En cada uno de los códigos de este apartado se utilizan tablas de resultados que se imprimen en la terminal de salida del compilador usando la librería de _tabulate_ en donde se utiliza la siguiente estructura de código.

``` python
ENC_RES = ["VARIABLE", "RESULTADO"] #LINEA 1
VAR_TAB2_RES = ['VARIABLE 1 (U1)','VARIABLE 2 (U2)','VARIABLE 3 (U3)','VARIABLE 4 (U4)'] #LINEA 2
R_VAR_EGI = [var1_EGI, var2_EGI, var3_EGI, var4_EGI] #LINEA 3
FIL_R_EGI = [] #LINEA 4
for i in range(4): #LINEA 5A
    FIL_R_EGI.append([VAR_TAB2_RES[i],R_VAR_EGI[i]]) #LINEA 5B
print(tb.tabulate(FIL_R_EGI, headers=ENC_RES, tablefmt="fancy_grid", floatfmt=".6f", stralign="center", numalign="center")) #LINEA 6
```

En línea 1 (`ENC_RES`) se muestra la variable en donde se puede nombrar o llamar variables de texto dentro de un arreglo para etiquetar las columnas de la tabla, es decir, entre más elementos haya dentro del mismo habrá más columnas.


En las líneas 2 y 3; se muestran tanto la variable de los títulos de las filas (`VAR_TAB2_RES`) y además de la variable en donde se guardan los datos que irá por cada columna a medida que avanza entre filas (`R_VAR_EGI`).


En la línea 4 se inicia el arreglo que se encargará de recibir todos los datos de las columnas por cada fila, detalle que se observa en las líneas 5A y 5B que realiza un ciclo iterativo con los datos que estén disponibles de las columnas por cada fila que quiera imprimir en la salida. Por úiltimo, en la línea 6 para que se imprima la tabla es necesario llamar la librería con los datos del contenido de la tabla (`FIL_R_EGI`) y los datos de los encabezados de la misma (`ENC_RES`) mediante la variable de `headers`. Para personalizar el diseño de tabla así como la distribución de texto se utilizan las variables `tablefmt` (diseño de tabla), `floatfmt` (formato númerico y decimal), `straling` (distribución de formato del texto) y `numaling` (distribución de formato de los números. 


En caso, de que se requiera una modificación en diseño y personalización de las tablas consulte la documentación de la librería [_tabulate_ ](https://pypi.org/project/tabulate/)


2. MODIFICACIONES DE VARIABLES


En el cálculo de las ecuaciones de estado se necesita de un constante que relaciona todos las variables macroscópicas como volumen, temperatura y presión para obtener otras variables térmidinámicas que dependen en gran medida de la materia y energía de un sistema en especifico, lo cual en varias ecuaciones de estado está presente como lo es la constante universal de los gases ($R$); sin embargo, esta constante esta relacionada entre las medidas de un sistema a escala microscópicas a uno macroscópico y viceversa que relaciona con magnitudes físicas como lo es del número de Avogadro ($N_{A}$) y el constante de Boltzmann ($k_{B}$), los diferentes ecuaciones de estado hacen correcciones a la constante $R$ y otras variables del sistema macroscópico tomando en cuenta las interacciones intermoleculares dentro del fluido.


Por eso es importante que los datos que ingresen los datos en unidades que esten conformes a las variables que deban obtener, por ejemplo si se usa una constante $R$ en específico es necesario ajustar las unidades macróscopicas del sistema (temperatura, volumen y presión) en unidades que tengan una congruencia con la misma constante.


Por ejemplo, si usamos el valor de $R$ de 0.08205 $\dfrac{L\;atm}{mol\;K}$ es necesario que las unidades macroscópicas (temperatura, volumen y presión) sean congruentes con las unidades en este caso Kelvin (K), Litros (L) y atmósferas (atm) para obtener las unidades adecuadas para las variables que se pueda obtener como por ejemplo, la cantidad de moles y de masa de un gas. En caso, de que los datos que se requieran obtener son las relacionadas con energía como lo es la entalpía ($H$), entropía (S) y energía libre de Gibbs (G) se utiliza una constante $R$ que incluya este mismo como por ejemplo el utilizada con las unidades del SI como lo es 8.3145 $\dfrac{J}{mol\;K}$, además de ser adecuado para realizar las conversiones a otras unidades incluyendo las del sistema inglés.
