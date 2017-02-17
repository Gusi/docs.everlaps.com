## &fa-clock-o; Heats

Heats progress is controlled from here, heats will be activated in the order established by the timekeeper, and generating the corresponding results sheets.

![Heats](../img/heats.png)

---

### Controlling the active heat

Once the heat is activated, the heat can be controlled from the panel.

![Control de manga](../img/heat-control.png)

##### Actions

- **Start**: Starts the heat with the prologue time established in [*prologue*](../race-formats/qualify-finals/index.html#campos-de-formato), In the race options. A warning will be given every minute of time left,name of heat, drivers and marshals. The last warnings will be at 30, 20 and 10 seconds before start.

- **30/10**: Starts the heat with a 30 or 10 second prologue time.

- **Go**: Immediate start.

- **Grid**: When the heat is active but has not started, this forces announcement of name of heat, drivers and Marshals.

- **Stop**: Stops a running heat. The heats results will are frozen at the moment of the halt.

- **Finish**: Stops and finalizes a running heat. The heats results are frozen and the announcement system reports end of heat and its results, The heat become in-active and if automatic results printing is configured the corresponding data is sent to the printer.

	!!! note ""
		After the end of heat sound, the program waits the pre-configured *Last lap* time, until all drivers that have passed the finishing line at least once finish their last lap. If a driver breaks and abandons the heat, the program will keep waiting for this driver until the *Last lap* time is up. In this case the *Finish* button is useful to terminate a heat without altering the results and saving time waiting for a car no longer on the track.

- &fa-gear; (*Heat parameters*): Shows the actual parameters of the active heat (duration, minimum lap time, last lap time, etc...)

!!! warning "Modifying an active heat"
	When a heat is activated, a safe copy of the heat data is made, transponder numbers, driver names, duration, format, etc... to guarantee the integrity of the program from possible erroneous modifications during the course of the heat. 
	
	To modify any of the drivers configuration values, heats to which they belong, race or session (Nick name, duration, standby time etc...) It will be necessary to deactivate the active heat, and re-activate it so that the new values are applied, except for the following data which can be **changed on the fly** even when the heat is active:
	
	- **Transponder**: Can be modified in the race registration list, or from the [Active heat situation](#situacion-de-la-manga-activa) panel, right clicking and using the change transponder option.
	- **Minimum lap time**: Can be changed at any time.
	- **Last lap time**: Can be changed before the heat has entered *last lap* time.
		
	NOTE: In [free practice](../race-formats/free-practice) it is possible to add new drivers on the fly, and modify nick names since this session format can access the database directly.

---

### &fa-list-alt; Heats

##### Actions

- &fa-upload; (*Activate selected heat*): Activates the selected heat, Showing the control panel and initialising the other panels *Heat situation* and *Results*. 

	!!! note ""
		If a heat that is activated already contains laps and results because it was started previously, a warning will be shown, and before the heat is re-started another warning will be shown, before **the saved data is deleted** completely.

- &fa-download; (*De-activate the selected heat*): De-activates the active heat if it is not in progress, in which case the heat will need to run its course or by pressing *Stop* or *Finish*

- &fa-play-circle; (*Activate/De-activate automatic mode*): Activates or de-activates [automatic mode](#auto). The icon can be in one of 3 states:
	
	- &fa-play-circle; (static): Automatic mode is disabled.
	
	- &fa-play-circle:spin; (spinning): Automatic is enabled and in standby to start the next heat. Remaining time will be shown and announcements made every minute.
	
	- &fa-play-circle; (blinking): The heat is active and in automatic and waiting to finalise before next heat is  started after the pre-configured prologue time.
	
	!!! note ""
		With automatic enabled, if a user starts the heat manually, or stops the heat once it has been activated in automatic, it will need to be re-started **manually**. Automatic mode will continue once the active heat finishes or is de-activated manually.

- &fa-eye; (*Show/Hide finalised heats*): Shows or hides finalised active heats.
		
- &fa-print; (*Print results*): Prints the results which correspond to the selected heat.

	!!! note ""
		It is possible to print heat, round or session, even in the middle of a heat. The results shown will correspond with the heat results up until that moment.
	
	- **Race**: Generates report for selected heat.
	
	- **Round**: Generates report for the round to which the selected heat belongs, including all the heats which belong to that round.
	
	- **Session**: Generates report for the session, to which the selected heat belongs, including all the rounds from the first up until the round that the heat belongs to.

- **Delete**: Removes the selected heat, including all laps and results.

##### Contextual menu

Right clicking on any heat except the active heat will access the contextual menu, with the following options:

- **Modify state...**
	- **To be started**: Heats waiting to be started, even if they may have results registered, are not included in the session results.
	- **Finished**: Finished heats, The heat will be included in session results. Even if they have no results can be marked as finished, which will allow heats from the next round to be activated if necessary.
- **Generate empty lap boxes**: Generates boxes in the lap counting panel that allow result corrections to be made for the drivers in that heat. It is useful when results need to be input without running the heat, or if drivers are added to a heat after the heat has been run, and manual results need to be established for laps and time. 

---

### &fa-caret-square-o-right; Auto

![Auto](../img/auto.png)

Controls automatic launching of heats for the active race meeting.

#### Scheduling

Enables scheduling of the heats according to the following parameters:

- **Start date**: Configure the start date for the race meeting. Useful if the race meeting is scheduled a few days in advance.

- **Start time**: Start time of the first heat.

- **Time between heats**: Start time between consecutive heats. 

	*For example, a 7 minute final, with a 2 minute  prologue and a  30 second last lap time has a minimum duration of 9.5 minutes. Taking into account the time drivers need to access the rostrum, an adequate time between heats could be almost 11 o 12 minutes.*

- **Time between rounds**: Time between the start of heat belonging to the same series but belonging to consecutive rounds. 

	*For ample, assuring that each series has 40 minute between heats so that batteries can be correctly charged, this is the value that should be specified. The system will use it as the minimum value, although depending on the number of heats and the time between them, the scheduled time could be greater.*

- **Time between sessions**: Time between the start of different sessions. 

	*Por ejemplo puede ser útil para establecer una separación mínima entre las sesiones de entrenamiento controlado y las de recolocación.*

- **Planificar mangas**: Ejecuta la planificación de las mangas restantes según los parámetros establecidos.

#### Ejecución

Los parámetros de ejecución se aplican justo antes de lanzar la siguiente manga y permiten controlar, en el caso de que la planificación original sufra algún retraso, cómo se va recuperando el tiempo para seguir la planificación original. 

- **Separación mínima mangas**: Tiempo mínimo entre el final de una manga y el lanzamiento de la siguiente. 

	*Teniendo en cuenta que los pilotos de la manga que termina deben abandonar el pódium, y subir los de la siguiente manga, un valor adecuado podría ser entre 1 o 2 minutos.*

- **Separación mínima cambio de tanda**: Tiempo mínimo entre el final de una manga y el lanzamiento de la siguiente, cuando las mangas pertenecen a tandas distintas. 

- **Separación mínima cambio de sesión**: Tiempo mínimo entre el final de una manga y el lanzamiento de la siguiente, cuando las mangas pertenecen a sesiones distintas.

- **Incluir mangas sin planificar**: Si está marcada, al lanzar el modo automático se incluyen aquellas mangas que no estuviesen planificadas de antemano, respetando únicamente los valores de *Ejecución* entre ellas. También habilita lanzar el modo automático directamente **sin planificar ninguna manga**.

---

### Situación de la manga activa

Este panel refleja el estado actual de la manga en curso, y mantiene el resultado hasta que se activa la siguiente manga.

Los campos mantienen su nombre siempre en inglés para que coincidan exactamente con la visualización del *Live Timing* en el navegador web.

- &fa-trophy; (*Posición*): Posición de carrera del piloto en la manga.
- &fa-flag-o; (*Finalizado*): Si aparece la bandera &fa-flag-checkered; significa que el piloto ha finalizado la manga.
- &fa-check; (*Verificado*): Un icono &fa-check; verde indica que el piloto ha realizado alguna pasada por línea de meta durante el tiempo de prólogo de la manga. Es útil para verificar, justo antes del inicio del cronómetro, que todos los pilotos tienen su transponder asignado correctamente.
- &fa-car; (*Número de coche*): Número del coche del piloto.
- **Driver**: Apodo del piloto.
- **Laps/Time**: Vueltas y tiempo que lleva el piloto en el momento concreto.
- **Prediction**: En mangas clasificatorias, indica el resultado previsto en vueltas y tiempo al finalizar la manga.
- **Gap**: Diferencia en tiempo o vueltas con respecto a la cabeza de carrera.
- **Diff**: Diferencia en tiempo o vueltas con respecto al piloto anterior.
- **Last**: Tiempo de la última vuelta.
- **Best**: Tiempo de la mejor vuelta.
- **Progress**: Barra de progreso que indica aproximadamente la situación de vuelta del piloto. Cuando la barra se completa, el piloto debería estar pasando por línea de meta si no ha sufrido ningún percance.

!!! note "Cambio de transponder en caliente"
	Con el botón derecho sobre cualquier piloto de este panel, es posible acceder al diálogo de cambio de transponder en caliente. Ver [Cambio de transponder](../common-tasks/change-transponders/index.html) para más información.

---


### &fa-list; Pasadas

Muestra el detalle de cada una de las pasadas de los pilotos en orden cronológico. En caso de que alguna pasada no sea aceptada, se mostrará con un color y estado distintos. Los posibles estados de una pasada pueden ser:

- **OK**: La pasada es correcta y se contabiliza para la manga.
- **Corregido**: La pasada se contabiliza pero el tiempo se ha corregido ya que se ha arrancado el crono del piloto con anterioridad.
- **Prohibido**: Pasada de un transponder no perteneciente a ningún piloto de la manga activa.
- **Expirado**: La pasada se realiza fuera del tiempo de última vuelta y no se contabiliza.
- **Atajado**: Se detecta como un atajo (tiempo de vuelta inferior al establecido en *Vuelta mínima*) y no se contabiliza.
- **Finalizado**: El piloto ya ha finalizado y no se contabiliza la pasada.
- **Denegado**: En carreras de relevos, si el piloto no tenía permiso de salir todavía a pista se rechaza la pasada.
- **Baja señal**: La pasada no pasó el filtro de señal o hits establecido en la configuración del decodificador.
- **Margen de inicio**: No se contabiliza porque la pasada se ha producido en una final antes de que finalice el *Tiempo de demora en finales*.

!!! note ""
	En el campo de tiempo de vuelta, el **color naranja** indica que el tiempo de esa vuelta el mayor que el doble de tiempo mínimo por vuelta establecido, lo cual puede indicar una vuelta no contabilizada para ese piloto por no haber pasado correctamente por línea de meta.

##### Menú contextual

Una vez que la manga termina, es posible asignar o denegar pasadas utilizando el botón derecho sobre la pasada correspondiente.

- **Modificar estado...**: Al modificar el estado de una pasada se recalcula el resultado del piloto en la manga y los tiempos de vuelta correspondientes.
	- **OK**: La pasada se asigna al piloto cuyo transponder coincida con el de la pasada.
	- **Denegado**: La vuelta seleccionada se marca como denegado y no se contabiliza.
	
- **Asignar todas**: Asigna todas las vueltas marcadas como *prohibidas* o *recuperadas* al piloto cuyo transponder coincida con el de la pasada.

- **Revisar tiempos de vuelta**: Comprueba que no haya atajos o pasadas fuera de tiempo contabilizadas como válidas. 
	
	*Este proceso se realiza automáticamente cada vez que se modifica el estado de alguna pasada o se añaden todas las pasadas de un piloto.*

- **Decodificador**: Permite recuperar pasadas directamente del decodificador AMB *sólamente si está conectado por cable Ethernet*.
	- **Recuperar pasadas perdidas**: Analiza las pasadas existentes y recupera aquellas que pudiesen haberse perdido debido a algún problema de comunicación con el decodificador.
	- **Recuperar últimas 10 pasadas**: Recupera 10 pasadas existentes justo después de la última pasada almacenada para la manga. Esta acción se puede repetir tantas veces como se quiera en caso de ser necesario.

---

### &fa-mail-forward; Vueltas

![Vueltas](../img/laps.png)

La pantalla de vueltas muestra el orden cronológico de las pasadas de cada piloto. Desde aquí y una vez finalizada y desactivada la manga, es posible realizar correcciones sobre el resultado de cada piloto. Ver [sanciones y correcciones](../common-tasks/punishments-corrections/index.html) para más información.

Las vueltas pueden ordenarse según el tiempo de vuelta o el orden cronológico, pulsando con el ratón sobre el título de la columna correspondiente (*Pasada* o *Vuelta*).

!!! note ""
	Al igual que en el panel de pasadas, en el campo de tiempo de vuelta el color naranja indica que el tiempo de esa vuelta el mayor que el doble de tiempo mínimo por vuelta establecido, lo cual puede indicar una vuelta no contabilizada para ese piloto por no haber pasado correctamente por línea de meta.

---

### &fa-flag; Resultados

![Resultados](../img/heatresults.png)

Muestra los resultados de manga o tanda para la manga seleccionada. Es muy útil en el caso de aplicar correcciones o sanciones a un piloto, ya que permite ver el resultado de cómo quedaría la manga o tanda antes de imprimirla.

- **Ver resultados de**:

	- **Manga**: Muestra los resultados de la manga seleccionada.
	- **Tanda**: Muestra los resultados de la tanda completa a la que pertenece la manga seleccionada.
	
- **Imprimir**: Imprime el resultado de manga o tanda que se está visualizando.
