## &fa-users; Pilotos

Permite la gestión de todos los pilotos disponibles en la base de datos del programa.

![Pilotos](img/drivers.png)

Es importante comprender algunos de los términos referentes a la gestión de pilotos:

- **Piloto**: es una persona individual que puede ser inscrita en alguna de las carreras configuradas
- **Categoría**: clasifica los diferentes modelos de vehículos
- **Ranking**: nivel de habilidad de un piloto en relación al resto
- **Etiqueta**: permite agrupar pilotos respecto a un identificador común    

Un piloto puede tener asignados diferentes valores de transponder y ranking según las categorías en las que participe, así como cualquier número de etiquetas definidas en el programa.

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

- &fa-search; **(Filtro de búsqueda)**: Realiza un filtrado de los pilotos visibles mostrando aquellos en los que alguno de sus campos (Nombre, Apellidos, Apodo, Transponder, Categoría, etc...) coinciden total o parcialmente con el texto introducido en el campo de búsqueda. 

##### Campos

- **Nombre y apellidos**: Aparecerán en los listados para identificar inequívocamente al piloto.

- **Apodo**: El apodo se usará en las locuciones para narrar las posiciones y tiempos de los pilotos, así como en el detalle de vueltas de los informes. Puede haber apodos repetidos en la base de datos, pero en una misma serie no está permitido (el programa avisará de tal situación para que sean modificados).

	!!! info ""
		Verifica que los apodos de los pilotos participantes sean pronunciables por el sistema locución antes de iniciar la carrera.

- **Correo**: El correo es la forma que utiliza el programa para emparejar inequívocamente a los pilotos entre la base de datos local y la base de datos disponible en la [web de Everlaps](http://everlaps.com), de forma que permite gestionar las inscripciones y resultados de cada piloto de manera bidireccional.

	Cuando se añaden pilotos de forma manual, es importante introducir correctamente su correo electrónico en caso de que estén ya registrados en [Everlaps](http://everlaps.com) para poder asignar sus resultados de forma correcta.

- **Etiquetas**: Muestra todas las etiquetas asignadas al piloto.

---
	
### Ficha del piloto

Muestra el detalle de todos los datos del piloto, incluyendo además de los datos personales enumerados anteriormente, las listas de transponders y rankings por categoría, las carreras activas en las que participa el piloto, y las etiquetas asignadas al mismo.

#### Transponders y rankings

TODO

- **Rank**: Se puede usar como indicador del nivel de los pilotos. Tener los pilotos clasificados por rank es muy útil a la hora de generar las series de forma rápida.

	Puede haber números de rank repetidos o no correlativos, lo importante es que cada piloto esté correctamente situado con respecto a los demás.

	!!! info ""
		El transponder y rank asignados a un piloto en cada carrera puede ser distinto al que aparece en la *lista de pilotos*.

#### Inscripciones activas

TODO

#### Etiquetas

TODO

