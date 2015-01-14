## &fa-users; Pilotos

Desde aquí se gestionan todos los pilotos disponibles en la base de datos del programa. Un piloto es una persona individual que puede ser inscrita en alguna de las carreras configuradas.

![Pilotos](img/drivers.png)

---

### Lista de pilotos

Permite la introducción, modificación y borrado de los pilotos disponibles.

##### Acciones

- **Añadir**: Inserta una nueva entrada en la lista para poder rellenar los campos correspondientes del piloto.

- **Eliminar**: Borra de la base de datos el piloto o pilotos seleccionados.

- **Importar**: Permite cargar una lista de pilotos desde un fichero.

	!!! info ""
		Al importar la lista de pilotos solamente se añaden aquellos que aparecen en el archivo pero no pertenecen todavía a la base de datos. De los pilotos ya existentes se respetan sus valores de transponder y rank.

- **Exportar**: Permite el volcado a fichero de la lista completa de pilotos.

- &fa-search; **(Filtro de búsqueda)**: Realiza un filtrado de los pilotos visibles mostrando aquellos en los que alguno de sus campos (Nombre, Apellidos, Apodo, Transponder, etc...) coinciden total o parcialmente con el texto introducido en el campo de búsqueda. 

##### Campos

- **Nombre y apellidos**: Aparecerán en los listados para identificar inequívocamente al piloto.

- **Apodo**: El apodo se usará en las locuciones para narrar las posiciones y tiempos de los pilotos, así como en el detalle de vueltas de los informes. Puede haber apodos repetidos en la base de datos, pero en una misma serie no está permitido (el programa avisará de tal situación para que sean modificados).

	!!! info ""
		Verifica que los apodos de los pilotos participantes sean pronunciables por el sistema locución antes de iniciar la carrera.

- **Correo**: El correo es la forma que utiliza el programa para emparejar inequívocamente a los pilotos entre la base de datos local y la base de datos disponible en la [web de Everlaps](http://everlaps.com), de forma que permite gestionar las inscripciones y resultados de cada piloto de manera bidireccional.

	Cuando se añaden pilotos de forma manual, es importante introducir correctamente su correo electrónico en caso de que estén ya registrados en [Everlaps](http://everlaps.com) para poder asignar sus resultados de forma correcta.

- **Rank**: Se puede usar como indicador del nivel de los pilotos. Tener los pilotos clasificados por rank es muy útil a la hora de generar las series de forma rápida.

	Puede haber números de rank repetidos o no correlativos, lo importante es que cada piloto esté correctamente situado con respecto a los demás.

	!!! info ""
		El transponder y rank asignados a un piloto en cada carrera puede ser distinto al que aparece en la *lista de pilotos*.

---
	
### Ficha del piloto

Muestra un resumen de los campos asignados al piloto seleccionado en la lista de pilotos. 

En próximas versiones se permitirá la asignación de múltiples transponders a un mismo piloto, así como la asignación de etiquetas que permitirán una mejor gestión de los pilotos disponibles cuando la base de datos es relativamente grande.