# Clasificatorias y finales

![Clasificatorias y finales](../img/qualy-finals.png)

El formato de carrera de *Clasificatorias y Finales* define por defecto las sesiones de entrenamiento, recolocación, clasificatorias y finales, de las cuales las dos primeras pueden eliminarse si no se van a utilizar durante la carrera.

---

##### General

- **Nombre**: Identifica la carrera. Aparece en la parte superior de los informes y como identificador de las mangas.

- **Descripción**: Información adicional que aparece en el pie de página de los informes.

- **Tipo**: Identifica el formato de carrera. En este caso mostrará siempre *Clasificatorisa y finales*.

- **Código web**: El código web se obtiene de la página web de [Everlaps](http://everlaps.com) y permite relacionar la carrera publicada en la página web para que se puedan publicar los resultados y habilitar el envío de datos al sistema de *Live Timing*.

- **Categoría**: Identifica la categoría de la carrera para elegir el transponder más adecuado durante las inscripciones manuales de pilotos.

---

##### Locución

- **Nombre corto**: Nombre que usa la locución para indicar a qué carrera pertenece la manga activa. Sólo se recomienda su uso cuando se intercalan mangas de varias carreras distintas (por ejemplo cuando corren dos categorías el mismo día), para que los pilotos puedan identificar a cual de las categorías corresponde la manga en curso.

- **Recoge-coches**: El sistema de locución permite avisar a los recogecoches desde que se abre la pista hasta el inicio de la manga.
	
	- **No llamar**: No nombrar a los recogecoches.
	- **Manga anterior**: Nombra a los recogecoches de la serie anterior de la misma carrera. Utilizar sólo si los pilotos de la misma carrera recogen justo después de correr su manga.

- **Nombrar pilotos**: Establece cómo ha de nombrar el sistema de locución a los pilotos para dar su posición en carrera, resultados finales, etc...
	
	- **Usar apodo**: Utiliza el apodo del piloto.
	- **Usar número de vehículo**: Utiliza el número de vehíulo asignado en la inscripción.
	
- **Numeración**: Establece el sistema de numeración de los vehículos durante la carrera.

	- **Renumerar cada sesión**: En cada sesión se modifica el número de cada vehículo en función de su posición obtenida.
	- **Numeración fija**: Se mantiene el mismo número de vehículo durante toda la carrera. Todos los pilotos deben tener su número único asignado en el panel de inscripciones.

- **Vehículo**: Establece el nombre de vehículo en las locuciones y listados (Coche o Moto)

---

##### Común

- **Prólogo**: Tiempo que transcurre desde que se pulsa el botón de inicio de manga (Start), hasta que ésta arranca.

- **Vuelta mínima**: Tiempo de la vuelta más rápida permitida para la carrera. Cualquier tiempo por debajo de este valor se interpreta como un atajo y no se contabiliza.
 
	!!! note
		Es conveniente que el valor de vuelta mínima sea lo más ajustado posible, ya que aparte de para detectar atajos en carrera, es utilizado por el sistema de locución durante las clasificatorias para efectuar los cálculos de situación real de carrera.

- **Última vuelta**: Tiempo para dar la última vuelta desde que se marca el final de manga (o el final del tiempo individual en clasificadoras). Según algunos reglamentos, debe ser el 150% de la vuelta calculada para el trazado.

- **Demora en finales**: Para las finales, establece un tiempo desde el inicio de la manga durante el cual las pasadas por línea de meta no se contabilizan. Ésto es útil para los circuitos en dónde la parrilla de salida atraviesa la línea de meta para evitar que los pilotos que salgan por detrás de la línea de meta reciban una vuelta más tras el comienzo de la manga.

---

#### Sesiones

##### Acciones disponibles

- **Añadir**: Permite añadir una nueva sesión de entrenamiento, recolocación (si no existe) o de formato personalizado.
- **Eliminar**: Permite eliminar la sesión seleccionada.

---

##### Parámetros

- **Pilotos/Serie**: Número de pilotos que se desea en cada serie cuando la distribución se realiza de forma automática con la opción *Generar* del panel de [series](../user-guide/races.md#series). En la pestaña de gestión de series se puede alterar con total libertad la distribución de pilotos, por lo cual este valor no es definitivo.

- **Distribución de series**: Establece cómo se distribuyen de forma automática los pilotos en las series según el valor de *Pilotos/Serie*.

	- **Completar en orden**: Completa las series de forma consecutiva con el valor de *Pilotos/Serie*. Se suele utilizar en finales para garantizar que todas las series tienen el máximo número de pilotos excepto la última. 
	 
		*Por ejemplo, en una carrera de 26 pilotos con 10 pilotos por serie se generarían 3 series A, B y C con 10, 10 y 6 pilotos respectivamente.*
 
	- **Distribución uniforme**: Realiza una distribución buscando un número similar de pilotos en todas las series sin exceder el valor de *pilotos/serie*. Se suele utilizar en clasificatorias para homogeneizar el número de pilotos en pista.

		*Por ejemplo, la misma carrera de 26 pilotos y 10 pilotos por serie en clasificatorias generaría 3 series 1, 2 y 3 con 7, 7 y 8 pilotos respectivamente.* 

- **Tandas**: Número de mangas que corre cada serie.

- **Puntúan**: Número de mangas que puntúan para el resultado de la sesión.

- **Duración**: Tiempo de duración de las mangas.

---

##### Locución

- **Tipo de narración**: Establece el tipo de información que el sistema de locución generará durante la carrera.

	- **Situación de carrera**: Cada cierto tiempo se informa de la situación de carrera con las posiciones de los pilotos y la distancia entre ellos.
	
		!!! note
			En las mangas clasificatorias, al llevar cada piloto su propio cronómetro, es posible que se efectúen ligeras pausas entre las locuciones de situación de cada piloto. Esto es perfectamente normal y depende de la distancia que haya entre el inicio del cronómetro de cada piloto y la fiabilidad del valor de vuelta mínima establecido para la carrera.
	
	- **Posición a paso por meta**: Cada vez que un piloto realiza un paso por meta se nombra la posición del piloto. Este modo sólo es aplicable a las finales, ya que todos los pilotos comparten el mismo cronómetro.
	
	- **Mixto (posición a paso por meta + situación de carrera)**: Utiliza el sistema de *posición a paso por meta* y, cada cierto tiempo, se informa de la *situación de carrera*.
	
	- **Sin narración**: No se efectúa ninguna narración acerca del estado de la carrera o posición de los pilotos.

- **Primera narración**: Tiempo desde el inicio de la manga hasta que comienza el procedimiento de locución de situación de carrera (generalmente el procedimiento se inicia con la pasada por meta del líder una vez transcurrido el tiempo para iniciar la narración, por lo cual puede haber una ligera demora hasta que comienza realmente la locución). 

- **Intervalo narración**: Tiempo que transcurre entre locuciones una vez realizada la primera narración.

- **Intervalo tiempo**: Intervalo entre narraciones del tiempo actual de carrera.

- **Modo tiempo**: Establece el valor de tiempo utilizado para la narración establecida en el *Intervalo tiempo*.

	- **Transcurrido**: Utiliza el tiempo transcurrido desde el inicio de la manga.
	- **Restante**: Utiliza el tiempo restante para el final de la manga.

---

##### Formato

- **Formato de sesión**: Define los parámetros de configuración de sesión más habituales en el cronometraje, y también se permite un ajuste personalizado de cada uno de los parámetros.

	- **Clasificatoria vueltas consecutivas**: Se suele usar para las mangas de recolocación. Cada piloto inicia su crono en el primer paso por meta y se contabiliza la suma total de las 3 mejores vueltas consecutivas. El valor de vueltas se establece en el campo *Vueltas resultado*.

	- **Clasificatoria lanzada (puntos o mejor resultado)**: El sistema va llamando a cada uno de los pilotos según el orden de clasificación de la sesión, con un intervalo configurable de tiempo, indicado en el campo *Retardo salida lanzada*. Las opciones de puntos o mejor resultado establecen la configuración de *Tipo de puntuación* para la sesión.

	- **Clasificatoria volante (puntos o mejor resultado)**: Similar a la anterior, pero cada piloto busca su hueco en el circuito e inicia su crono en el primer paso por meta.

	- **Finales**: Salida desde parado y en orden de parrilla, con el arranque del cronómetro en el instante de sonido de la bocina.
	
	- **Entrenos (puntos o mejor resultado)**: Similar a la clasificatoria volante, pero el crono se inicia con el sonido de la bocina en vez de esperar a la primera pasada.
	
!!! note
	Se puede modificar el formato en cualquier momento aunque ya se hayan disputado mangas de la sesión. El sistema recalcula los resultados en función de los nuevos parámetros y de las vueltas almacenadas.

##### Formato personalizado

Permite configurar cada uno de los parámetros.

- **Arranque crono**: Define cuándo arranca el cronómetro.

	- **Con la bocina**: El crono arranca con la bocina de salida.
	- **Con la primera pasada**: El crono arranca con la primera pasada por línea de meta de cualquiera de los pilotos que disputan la manga.
	
- **Modo crono**: Define la gestión del cronómetro por piloto

	- **Individual**: Cada piloto inicia su propio cronómetro de tiempo (clasificatorias).
	- **Compartido**: El arranque del cronómetro es compartido por todos los pilotos (finales).

- **Cronos retrasados**: Define cuando arrancan los cronos de los pilotos que no han realizado su primera pasada por meta.

	- **Primera vuelta completada**: El crono arranca al paso por meta del primer piloto que completa su primera vuelta.
	- **Después del tiempo de retraso**: El crono arranca después de que pase el tiempo definido en *Tiempo cronos retrasados* desde que se inició la manga.

- **Tiempo cronos retrasados**: Para el modo *Después del tiempo de retraso*, indica el tiempo que transcurre hasta que se arranca el crono de los pilotos que no han realizado su primera pasada por meta.

- **Modo de inicio**: Define el formato en el que los pilotos inician la manga.

	- **Parrilla**: El sistema ejecuta una cuenta atrás, y después de un tiempo aleatorio tras llegar a 3, comienza la manga.
	- **Lanzada**: El sistema va dando la salida uno a uno a los pilotos.
	- **Volante**: Se ejecuta una cuenta atrás completa para que cada piloto busque su espacio en la pista.

- **Tiempo mínimo cuenta atrás**: Sólo para el modo de inicio *Parrilla*, tiempo mínimo de espera después del último número de cuenta atrás, antes de la bocina de salida.

- **Tiempo aleatorio cuenta atrás**: Sólo para el modo de inicio *Parrilla*, tiempo aleatorio de espera después del tiempo mínimo de cuenta atrás, antes de la bocina de salida. *Por ejemplo, una configuración de tiempo mínimo de 2 segundos, y tiempo aleatorio de 3 segundos, supone que después de la cuenta atrás de 10 a 3, el programa esperará entre 2 y 5 segundos antes de dar la salida.*

- **Retardo salida lanzada**: Para el modo de *Salida lanzada*, indica el espacio tiempo entre las llamadas a los pilotos.

- **Orden salida lanzada**: Define si en cada tanda se recalcula el orden de salida a razón de la posición actual en la sesión.

	- **Reordenar cada tanda**: Efectúa la reordenación. Es el funcionamiento habitual cuando se usa la salida lanzada.
	- **Orden fijo**: Mantiene el orden de salida constante en todas las tandas.

- **Tipo de resultado**: Define los valores que se contabilizan para el resultado de la sesión:

	- **Vueltas / Tiempo**: Se contabiliza el número de vueltas totales y el tiempo en realizarlas.
	- **Vueltas consecutivas**: Se contabiliza el menor tiempo de suma de N vueltas consecutivas (Recolocación).
	- **Vueltas fijas**: Se contabiliza el tiempo empleado en completar las vueltas indicadas (tipo Fórmula 1).

- **Vueltas resultado**: Número de vueltas a tener en cuenta para los modos de *Vueltas consecutivas* y *Vueltas fijas*.

- **Alcance de resultado**: Define el grupo de competidores para el resultado de la sesión.

	- **Global**: Se tienen en cuenta los resultados de los todos los pilotos para la clasificación final (Clasificatorias).
	- **Por serie**: Se tienen en cuenta solo los resultados de los pilotos pertenecientes a la misma serie (Finales).

- **Tipo de puntuación**: Establece el sistema de puntuación de la sesión

	- **Puntos**: Se establece un sistema de puntos para obtener el resultado de las sesión. Por defecto se usa el sistema estándar de eléctricos según la posición obtenida en cada tanda (0, 2, 3… para clasificatorias: 1, 2, 3... para finales)
	- **Mejor resultado**: Se elige el mejor resultado en vueltas/tiempo sin importar la posición.

- **Sistema de puntos**: Establece el sistema de puntuación de entre los soportados por el programa.

- **Series con tandas completas**: Establece una división en cuanto al número de mangas que puntúan para cada serie. Esto es útil para, por ejemplo en finales, permitir que la serie A corra 3 finales puntuando 2 de ellas, y las series de la B en adelante sólo una única final.

	- **Todas las series**: Todas las series puntúan exactamente con el mismo número de mangas. No existe distinción entre series respecto al número de tandas y mangas puntuables.
	
	- **Primeras series**: Las primeras series puntúan el número de mangas establecido en la configuración general de la sesión y el resto el valor establecido en *Tandas en series inferiores*.
	
		- **Hasta la serie**: Define hasta que serie (inclusive) se disputan todas las mangas de forma normal. Por ejemplo si sólo se quieren 3 finales para la serie A, este valor debe ser 1.
		- **Tandas en series inferiores**: Número de tandas que puntúan para las series inferiores. Por ejemplo 1 para que las series por debajo de la A puntúen sólo una manga.

---

##### Desempates

Permite establecer la forma de solucionar los empates, en caso de que varios pilotos obtengan exactamente la misma puntuación en el global de las mangas a contabilizar para la sesión.

- **Formato de desempate**
	- **Por defecto**: Se utilizan únicamente las mangas válidas, comparando primero por posición, y en caso de proseguir el empate, por resultado.
	- **Personalizado**: Permite establecer todas las propiedades de resolución de empates.
	
##### Formato personalizado de desempates

- **Mangas descartadas en desempate**: Cuántas mangas descartadas se utilizarán para resolver el desempate. El valor 0 indica que no se utilizará ninguna manga descartada.
- **Uso de mangas descartadas**: Establece en qué momento se utilizan los resultados de las mangas descartadas.
	- **Antes de la comparación individual de mangas válidas**: Se utiliza la comparación individual de las mangas descartadas ANTES de la comparación individual de las mangas válidas.
	- **Después de la comparación individual de mangas válidas**: Se utiliza la comparación individual de las mangas descargadas DESPUÉS de la comparación individual de las mangas válidas. 
	
		*Por ejemplo, en una clasificatorias de 5 tandas en donde puntúan las 3 mejores y no pudiendo resolver el desempate se utilizaría la cuarta mejor manga de los pilotos, y en caso de seguir el empate, la quinta mejor manga, antes de comparar las posiciones de las tres mejores mangas.*

- **Desempate por posición**: Establece el modo de comparación individual por posición obtenida en cada una de las mangas (sólo si el resultado es por puntos)
	- **Mejor posición**: Utiliza el modo de comparación por posición obtenida.
	- **No usar**: No utilizar el desempate por posición.
- **Desempate por resultado**: Establece el modo de comparación individual por resultado en vueltas/tiempo para cada una de las mangas.
	- **Mejor resultado**: Se realiza la comparación individual de mangas por el resultado en vueltas/tiempo.
	- **Resultados combinados**: El desempate se realiza por la suma de vueltas y tiempo de todas las mangas válidas.
	
!!! note "Resolución de empates por comparación individual"
	En el caso de que varios pilotos obtengan el mismo resultado en puntos (o vueltas/tiempo), se establece el siguiente proceso de resolución:

	- Gana el piloto con una mejor posición en su mejor manga. Si persiste el empate se compara la segunda mejor manga, y así sucesivamente hasta el número de mangas que puntúan (sólo si el resultado es por puntos)
	- Si siguen empatados, gana el piloto con mejor resultado (vueltas/tiempo) en su mejor manga. Si persiste el empate se compara la segunda mejor manga, y así sucesivamente hasta el número de mangas que puntúan. 

---

#### Etiquetas

Permite asignar etiquetas a la carrera. Más información en la sección de [Etiquetas](../common-tasks/tags.md).

- **Recalcular puntuación al filtrar resultados por etiqueta**: Si está habilitado, al generar un resultado filtrado por etiqueta se recalcula la puntuación de la sesión únicamente con los pilotos que tienen la etiqueta. El resultado podría variar con respecto a no activar la opción y hacer un filtrado sobre el resultado general, ya que al recalcular la puntuación, y dependiendo del formato de puntos, las sumas finales podrían designar posiciones de pilotos diferentes.
