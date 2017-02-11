## &fa-bolt; Cambiar transponders

A la hora de modificar el transponder de un piloto, es importante entender cómo gestiona Everlaps la asignación de transponders.

### Transponder en la lista de pilotos (transponders y rankings)

Por un lado, en la [lista de pilotos](../user-guide/drivers/index.html), se establecen los transponders pertenecientes a cada piloto. Estos valores se utilizan para facilitar la asignación o cambio de transponder en las inscripciones. **Modificar un transponder en esta lista no tiene ningún efecto sobre las inscripciones actuales del piloto** (excepto en el modo de [entrenamiento libre](../race-formats/free-practice/index.html), ya que en cada pasada por meta se consultan los transponders pertenecientes a cada piloto).

### Transponder en la lista de inscripciones de una carrera

El transponder asignado a un piloto en una carrera, es independiente del número asignado en la lista de pilotos y del resto de carreras. 

Se puede modificar el transponder rápidamente seleccionándolo de la lista de transponders pertenecientes al piloto, o se puede introducir manualmente un nuevo número de transponder (en cuyo caso será añadido automáticamente a la lista de transponders del piloto en la categoría a la que pertenece la carrera). 

Si el cambio se realiza sobre una inscripción que pertenece a la manga activa, se mostrará un diálogo para confirmar el cambio de transponder en caliente. 

Cuando la lista de inscripciones de una carrera se importa desde la web de Everlaps (donde previamente todos los participantes se han inscrito para la carrera indicando su número de transponder) los números asignados a los pilotos para esa carrera son los que ellos han introducido al inscribirse.

## Cambio de transponder en caliente

Para cambiar el número de transponder de un piloto, según se ha explicado en la sección anterior, lo ideal es hacerlo desde la [lista de inscripciones](../user-guide/races/index.html#inscripciones) de esa carrera. 

Sin embargo existe otro modo si la manga ya ha sido activada. Desde la vista de [situación de la manga activa](../user-guide/heats/index.html#situacion-de-la-manga-activa), en donde aparece la lista de los pilotos participantes en la manga en curso, es posible mostrar el diálogo de *Cambiar transponder* utilizando el botón derecho del ratón sobre el piloto al que se desea modificar el transponder.

![Cambiar transponder](../img/changetransponder.png)

El diálogo muestra el nombre y número de coche del piloto seleccionado, así como su transponder actual, pudiendo introducir el nuevo número de transponder. 

Si el piloto ya ha **efectuado alguna pasada** por línea de meta desde que la manga se activó, en la parte inferior del diálogo aparecerán los transponders que han realizado alguna pasada y que no pertenecen a ningún piloto de la manga activa, siendo posible seleccionar el transponder correspondiente de la lista y asignárselo al piloto. La lista de transponders inválidos aparecen en color gris, excepto el último transponder que pasado por línea de meta, que aparece en color verde. De esta forma es más sencillo identificar a quién pertenecen los números de los transponders inválidos.

!!! note ""
	Durante el prólogo de la manga (desde que se activa hasta que se da la salida) a los pilotos que hayan realizado al menos una pasada por línea de meta se les marca con un &fa-check; en la vista de [situación de la manga activa](../user-guide/heats/index.html#situacion-de-la-manga-activa), indicando que el piloto está en pista. 
	
	Si existen pilotos con un transponder incorrecto, serán aquellos que *no* tengan el &fa-check; verde.

