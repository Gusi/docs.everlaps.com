## Qualifying and finals

![Qualifying and finals](../img/qualy-finals.png)

The race format *Qualification and Finals* defines by default the practice, re-ordering, qualifying and finals sessions, the first two of which can be removed if they are not going to be used in the race.

---

##### General

- **Name**: Race name. appears at the top of reports and as an identifier of the heats.

- **Description**: Additional information that appears at the bottom of reports.

- **Type**: Identifies the race format. In this case it will show *Qualifying and finals*.

- **Web code**: The web code is obtained at the site [Everlaps](http://everlaps.com) and permits connecting with the race published on the web site and publishing its results and enabling the sending of data to *Live Timing*.

- **Classes**: Identifies the race class so that the appropriate transponder can be chosen during manual driver registration.

---

##### Announcements

- **Short name**: Short name that the Announcer uses to identify to what race an active heat belongs. Its use is only recommended when heats from different races are mixed. (For example when two classes are run on the same day), so that drivers can identify which of the classes the active heat  belongs to.

- **Marshals**: The Announcer can call the marshals once the track is open for a heat until it starts.
	
	- **No call**: Does not call the marshals.
	- **Previous Heat anterior**: Names the drivers from the previous series to marshal. Only use if drivers from the same race marshal after running their heat.

- **Names drivers**: Establishes how the drivers are to be named by the announcer to give race position, final results etc...
	
	- **Nick name**: Uses the drivers nick name.
	- **Uses vehicle number**: Uses the vehicles number assigned at registration.
	
- **Numbering**: Establishes the numbering system for vehicles during the race.

	- **Re-number each session**: The vehicle numbers are modified each session depending on results obtained.
	- **Registration number**: The same vehicle number is kept during all the race. All drivers have their own number and it is assigned on the registration panel.

- **Vehicle**: Establishes vehicle type for announcer and lists (car or bike)

---

##### Common

- **Prologue**: The time that passes from when the heat (Start) button is pressed and the heat launches.

- **Minimum lap time**: minimum fastest lap time allowed by the race. Any time below this is interpreted as a short cut and will not be counted.
 
	!!! note ""
		It is convenient that the minimum lap time be as tight as possible, apart from detecting shortcuts it is used by the announcement system during qualifying to calculate the race positions.

- **Last lap**: Time allowed to complete the last lap once the heat has ended (or the end of individual qualifying time). According to some regulations, it should be 150% of the time calculated for a lap.

- **Finals delay**: For finals, establishes the time from the beginning of the final during which crossings are not counted. This is useful on tracks where the starting grid crosses the finishing line, avoids drivers starting behind it getting a lap counted at the very beginning of the final.

---

#### Sessions

##### Available actions

- **Add**: Allows adding a new practice session or re-ordering (if one does already not exist) or a personalised format.
- **Delete**: Allows removing a selected session.

---

##### Parameters

- **Drivers/Series**: Number of drivers per series when the distribution is done automatically with the *Generate* option on the [series](../user-guide/races/index.html#series) panel. On the series management tab the driver distribution can be changed with total liberty, so this value is not definitive.

- **Series distribution**: Establishes how the drivers are automatically distributed into heats with the value *Drivers/Series*.

	- **Complete in order**: Completes the series consecutively with the value *Drivers/Series*. Its normally used in finals to guarantee all finals have minimum number of drivers except the last. 
	 
		*For example, a race with 26 drivers with 10 drivers per series, 3 series are generated A, B and C with 10, 10 and 6 drivers respectively.*
 
	- **Uniform distribution**: Distributes by trying to find a even distribution of drivers in all the series without exceeding the value *Drivers/series*. It can be used in qualifying to even out the number of drivers on the track.

		*For example, The same race with 26 drivers with 10 per qualifying series would generate 3 series 1, 2 and 3 with 7, 7 and 8 drivers respectively.* 

- **Rounds**: The number of heats each series runs.

- **Counted**: The number of heats counted for the results of each session.

- **Duration**: Duration of each heat.

---

##### Announcements

- **Type of narration**: Establishes the type of information the system announces during the race.

	- **Race situation**: Periodically the the race situation, drivers positions and distance between them are announced.
	
		!!! note ""
			In qualifying heats, as each driver has their own chrono, it is possible that there will be slight pauses between announcements for each driver. This is completely normal and depends on the distance between the start of each drivers chrono and the reliability of the minimum lap value established for the race. 
	
	- **Position when passing finishing line**: Each time a driver crosses the finishing line the drivers position is announced. This mode is only applied to finals, since all drivers have a common chrono.
	
	- **Mixed (position when passing finishing line + race situation)**: Uses the *position when passing finishing line* and, periodically *race situation* is announced.
	
	- **No narration**: No announcements are made regarding race situation or drivers positions.

- **First narration**: Time from the start of the heat until race situation announcements start being made (generally the announcements start once the race leader passes the finish line after the first narration time has elapsed, therefore there can be a slight delay beyond that of the set time). 

- **Narration Interval**: Time between announcements once the first has been made.

- **Race time interval**: Interval between race time announcements.

- **Race time mode**: Establishes the race time mode for the time used in *Race time Interval*.

	- **Elapsed**: Uses the time elapsed from beginning of heat.
	- **Remaining**: Uses the time remaining until the end of heat.

---

##### Format

- **Session format**: Defines the configuration parameters most used to chrono, and also allows personalised adjustment of each parameter.

	- **qualifying consecutive laps**: This is normally used for re-ordering heats. Each pilots starts their own chrono with the first crossing of the finishing line, the sum of the 3 fastest consecutive laps are counted.These are established as *Laps result* value.

	- **Launched qualifying (points or best result)**: The system calls each driver in turn according to session ranking, with a configured time interval, indicted in the field *Launched start delay*. The option for points or best result are established in the field *Session points type* for the session.

	- **flying start qualifying (points or best result)**: Similar to the previous, but each driver can find their own space on the track and starts their own chrono when they cross the finishing line for the first time.

	- **Finals**: Starting grid launch and in grid order, with the start of the chrono the instant the horn sounds.
	
	- **Practice (points or best result)**: Similar to flying start qualifying, but the chrono starts with the sound of the horn instead of waiting for the first passing of the finishing line.
	
!!! note ""
	The format can be modified even thou heats of the session have already been run. The system re-calculates the results according to the new parameters and the laps recorded.

##### Personalised Format

Allows configuring each of the parameters.

- **Start chrono**: Defines when the chrono starts.

	- **Start on horn**: The chrono start on the starting horn.
	- **start on first crossing**: The chrono starts with the first crossing of the finishing line by any of the drivers in the heat.
	
- **Chrono mode**: Defines individual chrono management

	- **Individual**: Each driver starts their own chrono (qualifying).
	- **shared**: The chrono start is common to all the drivers (finals).

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

	- **Puntos**: Se establece un sistema de puntos para obtener el resultado de las sesión. Por defecto se usa el sistema estándar de eléctricos según la posición obtenida en cada tanda (0, 2, 3… para clasificatorias; 1, 2, 3... para finales)
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

Permite asignar etiquetas a la carrera. Más información en la sección de [Etiquetas](../common-tasks/tags/index.html).

- **Recalcular puntuación al filtrar resultados por etiqueta**: Si está habilitado, al generar un resultado filtrado por etiqueta se recalcula la puntuación de la sesión únicamente con los pilotos que tienen la etiqueta. El resultado podría variar con respecto a no activar la opción y hacer un filtrado sobre el resultado general, ya que al recalcular la puntuación, y dependiendo del formato de puntos, las sumas finales podrían designar posiciones de pilotos diferentes.
