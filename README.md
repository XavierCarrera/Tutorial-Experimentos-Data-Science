#Diseño de Experimentos en Data Science

##Introducción: Observaciones y Experimentos

La diferencia entre observaciones y experimentos es muy importante en estadística, por lo cual tiene un impacto importante en Data Science. Sin importar si usamos datos observacionales o experimentales, las conclusiones puede variar según como diseños un experimento.

Supongamos que conoces a un grupo de boomers (nacidos entre 1960 y 1975) que gustan de escuchar a *The Rolling Stones*. ¿Sería correcto asumir que toda la generación boomer es fanática de *The Rolling Stones*? Por supuesto que no, porque aunque los boomers comparten muchas características generacionales no podemos asumir que sus gustos son idénticos. 

En este caso, para llegar a conclusiones más solidas tenemos que diseñar un experimento que observe a la población en su totalidad. Digamos que hacemos un experimento en donde hablamos con 100 boomers de nuestra ciudad. De ellos, a 91% les gustan *The Rolling Stones*. ¿Podríamos decir que este es un experimento bien diseñado? Nuevamente no. En este caso, aunque mejor que en el primer experimento, no podemos dibujar conclusiones ya que 100 boomers de nuestra ciudad sigue siendo un número muy pequeño para representar a todos los boomers del mundo y solo hemos entrevistado a personas locales.

Es en estos casos que debemos hacer una distinción entre observaciones y experimentos.

Una **observación** es el registro de un valor particular en un punto de tiempo determinado. Por ejemplo, un valor cuantititativo como cuando medías a los 10 años o un valor cualitativo como tu sabor favorito de helado. En un **estudio observacional** colectamos muchas observaciones que consideramos importantes. Sin embargo,no podemos cambiar nada sobre la situación o variables involucradas en el estudio.

En cambio, un **experimento** involucra la aplicación de tratamientos especiales para seleccionar grupos a lo que le sigue una observación de valores específicos. Los experimentos siempre involucran una manipulación directa o inderecta de la situación con el fin de encontrar una relación entre dos variables.

Por ejemplo, podríamos hacer un experimento que involucre dividir personas en dos grupos. Un grupo recibirá un cereal azucarado y el otro un cereal bajo en azúcar. Después podemos medir sus niveles de actividad por las siguientes horas. El experimento nos puede ayudar a identificar la relación entre la ingesta de azúcar y los niveles de actividad. En este caso, estaríamos **alterando los niveles de las variables** (cantidad de azucar consumida).

En este caso, hay que examinar el concepto de **significancia estadística**. Aquí no hacemos referencia a la importancia o diferencia en los resultados, sino a la posibilidad de que un resultado haya sido causado por aletoriedad. 

Digamos que queremos saber si una moneda esta truqueada hacía resultar en cara cada vez que se tira. Si tiramos la moneda dos veces, el hecho de que en ambos casos haya salido cara significa que en realidad la moneda este truqueada. Por ende, no podemos decir que sea estadisticademente significativo. Si tiraramos la moneda 100 veces y todas fueran cara, en ese caso hablaríamos de significancia estadística porque es muy poco probable que eso suceda.

##Probabilidad Bayesiana

El Teorema de Bayes nos señala que dado una Hipótesis *H* y evidencia *E*:

    [La evidencia que H sea cierto dado que E sucedió] = [La probabilidad que suceda H] ⋅ [La probabilidad de que E sea cierto dado que H sea cierto] / [La probabilidad natural de E]
    
Matemáticamente ser vería así:

    P(H|E) = P(H) ⋅ P(E|H) / P(E)
    
Consideremos el siguiente escenario: hay una extraña enfermedadq ue afecta al 1% de la población. Hay una prueba que detecta precisamente el 99% de los casos. Es decir, si tienes la enfermedad la detectará correctamente el 99% de veces y si no la tienes, no la detectará el 99% de las veces.

Si sales positiva/o en la prueba, que probabilida hay que la prueba este en lo correcto?

Veamos como sustituiriamos cada uno de los valores para calcular las probablidades:

    P(Tener la enfermedad dado la prueba) = P(tener la posibilidad de dar positivo dado que tienes la enfermedad) ⋅ P(tener la enfermedad) / P(tener una prueba positiva)
    
    P(D|T) = 0.99 ⋅ 0.01 / 0.0198
    P(D|T) = 0.5
    
Por tanto, la posibilidad de tener la enfermedad es del 50%. Veámoslo así: de una población de 10,000, esperamos que 100 tengan la enfermedad y 9,900 no. De los 100 que tienen la enfermedad, 99 darán positivo. De los 9,900 que dan negativo, el 1% (99) tienen la enfermedad. Por tanto, en total 198 tienen la enfermedad.

##Diseño de Experimentos
   
