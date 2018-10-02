## &fa-clock-o; Mangas

Desde aquí se controla el progreso de las carreras, activando las mangas en el orden establecido por el cronometrador, y generando los informes de resultados correspondientes.

![Mangas](../img/heats.png)

---

### Control de la manga activa

Al activar una manga, se muestra el panel que permite controlar el estado de la manga.

![Control de manga](../img/heat-control.png)

##### Acciones

- **Start**: Inicia la manga con el tiempo de margen establecido en [*prólogo*](../race-formats/qualify-finals.md#campos-de-formato), en las opciones de carrera. Cada minuto se avisará del tiempo restante, nombre de manga, pilotos y recogecoches. Se darán los últimos avisos 30, 20 y 10 segundos antes de la salida.

- **30/10**: Inicia la manga con 30 o 10 segundos de margen.

- **Go**: Inicia la manga de forma inmediata.

- **Grid**: Cuando la manga está activada pero todavía no ha arrancado se puede forzar una lectura del nombre de la manga, pilotos y recogecoches.

- **Stop**: Detiene la manga en curso. Los resultados de la manga quedarán congelados en el momento de la detención.

- **Finish**: Detiene y finaliza la manga en curso. Los resultados quedan congelados y además el sistema de locución notifica el final de la manga y sus resultados, la manga se desactiva, y en caso de tener configurada la impresión automática de resultados, se envían a la impresora los datos correspondientes.

	!!! note ""
		Después del sonido de fin de manga, el programa espera el tiempo configurado de *última vuelta* hasta que todos los pilotos que han pasado al menos una vez por línea de meta completan su última vuelta. Si un piloto ha roto el coche y abandonado la manga, el programa seguirá esperando por este piloto hasta que se consuma el tiempo de *última vuelta*. En este caso el botón de *Finish* es especialmente útil porque permitiría finalizar la manga sin alterar el resultado y ahorrar el tiempo de espera por un coche que ya no está en pista.

- &fa-gear; (*Parámetros de manga*): Muestra los parámetros actuales de la manga activa (duración, tiempo de vuelta mínima, tiempo de última vuelta, etc...)

!!! warning "Modificaciones sobre una manga activa"
	Cuando una manga se activa, se realiza una copia aislada de todos los datos que intervienen en la manga, como son los transponders de los pilotos, nombres, duración, formato, etc... para garantizar la integridad del programa frente a posibles modificaciones erróneas durante el transcurso de la manga. 
	
	En el caso de que se modifique alguno de los valores de configuración de los pilotos, carrera o sesión a la que pertenece la manga (apodos, duración, tiempo de prólogo, etc...) es necesario desactivar y volver a activar la manga para que estos valores se apliquen, excepto para los siguientes datos que son **modificados en caliente** incluso cuando la manga está activada:
	
	- **Transponder**: Se puede modificar desde la lista de inscripciones de la carrera, o desde el panel de [situación de la manga activa](#situacion-de-la-manga-activa) utilizando el botón derecho y el diálogo de cambio de transponder.
	- **Tiempo de vuelta mínima**: Se puede modificar en cualquier momento
	- **Tiempo de última vuelta**: Se puede modificar excepto cuando la manga entra en el estado de *última vuelta*
		
	NOTA: En el modo de [entrenamiento libre](../race-formats/free-practice) es posible incorporar pilotos en caliente, así como modificar los apodos, ya que este formato de carrera realiza un acceso directo a la base de datos.

---

### &fa-list-alt; Mangas

##### Acciones

- &fa-upload; (*Activar manga seleccionada*): Activa la manga seleccionada, mostrando el panel de control e inicializando el resto de paneles de *Situación de la manga activa* y *Resultados*. 

	!!! note ""
		Si la manga que se activa contiene ya vueltas y resultados porque se inició anteriormente, se mostrará un aviso notificando de la situación, y antes de iniciar la manga se volverá a mostrar otro mensaje de aviso, antes de que **los datos guardados sean eliminados** completamente.

- &fa-download; (*Desactivar manga activa*): Desactiva la manga activa si no está en progreso, en cuyo caso habrá que esperar a la finalización de la manga, o detenerla con los botones de *Stop* o *Finish*

- &fa-play-circle; (*Activar/Desactivar modo automático*): Activa o desactiva el [modo automático](#auto). El botón puede estar en uno de estos 3 estados:
	
	- &fa-play-circle; (estático): El modo automático esta desconectado.
	
	- &fa-play-circle:spin; (rotando): Modo automático conectado y en espera de lanzar la siguiente manga. Se mostrará el tiempo restante y se avisará por megafonía cada minuto.
	
	- &fa-play-circle; (parpadeando): La manga está activada y el modo automático está a la espera de su finalización para lanzar la siguiente manga después del tiempo de espera configurado.
	
	!!! note ""
		Con el modo automático activado, si el usuario activa la manga manualmente, o si detiene la manga una vez que ha sido activada automáticamente, debe iniciar la manga **de forma manual**. El modo automático continuará una vez que la manga activada finalice o se desactive manualmente.

- &fa-eye; (*Mostrar/Ocultar mangas finalizadas*): Muestra u oculta las mangas finalizadas de las carreras activas en ese momento.
		
- &fa-print; (*Imprimir resultados*): Imprime los resultados correspondiente a la manga seleccionada.

	!!! note ""
		En cualquier momento es posible imprimir el resultado de manga, tanda o sesión, incluso en mitad del progreso de una manga. El resultado que se mostrará corresponderá con la situación de la manga en ese momento.
	
	- **Manga**: Genera el informe de la manga seleccionada.
	
	- **Tanda**: Genera el informe de la tanda a la que pertenece la manga seleccionada, incluyendo todas las mangas que pertenecen a la tanda.
	
	- **Sesión**: Genera el informe de la sesión a la que pertenece la manga seleccionada, incluyendo las tandas desde la primera hasta la tanda a la que pertenece la manga.

- **Eliminar**: Borra la manga seleccionada, incluyendo todas sus vueltas y resultados.

##### Menú contextual

Sobre cualquier manga, a excepción de la manga activa, se puede utilizar el botón derecho para acceder al menú contextual con las siguientes opciones:

- **Modificar estado...**
	- **Por disputar**: Las mangas pendientes de disputar, aunque tengan resultados registrados, no intervienen en el resultado de la sesión.
	- **Finalizada**: En estado finalizado, la manga interviene en los resultados de sesión. Aunque la manga no contenga resultados se puede marcar como finalizada, lo cual habilita por ejemplo activar las mangas de la tanda siguientes en caso de ser necesario.
- **Generar contenedores de vueltas vacíos**: Genera los contenedores que aparecen en el panel de vueltas y que permiten hacer correcciones sobre los resultados de los pilotos en esa manga. Es útil cuando se desea introducir resultados directamente sin haber disputado la manga, o si se añade un piloto a la serie después de que ésta se haya disputado, y se desea establecer manualmente su resultado de vueltas y tiempo. 

---

### &fa-caret-square-o-right; Auto

![Auto](../img/auto.png)

Controla el lanzado automático de mangas para la carrera activa.

#### Planificación

Permite planificar el lanzamiento de las mangas en base a los parámetros siguientes:

- **Fecha de inicio**: Configura la fecha de ejecución de la carrera. Útil si se realiza la planificación en días previos.

- **Hora de inicio**: Hora de lanzamiento de la primera manga.

- **Tiempo entre mangas**: Tiempo entre el lanzamiento de mangas consecutivas. 

	*Por ejemplo, una final de 7 minutos, con 2 minutos de prólogo y 30 segundos de última vuelta tiene una duración mínima de 9:30 minutos. Teniendo en cuenta el tiempo que los pilotos necesitan para bajar y subir al pódium, un tiempo entre mangas adecuado para este caso podría ser 11 o 12 minutos.*

- **Tiempo entre tandas**: Tiempo entre el lanzamiento de mangas pertenecientes a la misma serie pero de tandas consecutivas. 

	*Por ejemplo, si queremos asegurar que cada serie tiene 40 minutos entre mangas para poder cargar correctamente las baterías, éste es el valor que debemos especificar. El sistema lo respetará como valor mínimo, aunque debido al número de mangas y el tiempo entre ellas, el tiempo entre tandas planificado podría ser mayor.*

- **Tiempo entre sesiones**: Tiempo entre el inicio de dos sesiones diferentes. 

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
	Con el botón derecho sobre cualquier piloto de este panel, es posible acceder al diálogo de cambio de transponder en caliente. Ver [Cambio de transponder](../common-tasks/change-transponders.md) para más información.

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

La pantalla de vueltas muestra el orden cronológico de las pasadas de cada piloto. Desde aquí y una vez finalizada y desactivada la manga, es posible realizar correcciones sobre el resultado de cada piloto. Ver [sanciones y correcciones](../common-tasks/punishments-corrections.md) para más información.

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
