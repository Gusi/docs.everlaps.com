# Inicio rápido

Se describen a continuación los pasos básicos para poder instalar y generar una carrera en Everlaps. Para información más detallada consulta el resto de la documentación.

---

### Acciones básicas

1.  Introduce los datos de los pilotos en [:fontawesome-solid-users: **Pilotos**](./user-guide/drivers.md)

2.  Crea una nueva carrera en [:fontawesome-solid-road: **Carreras**](./user-guide/races.md), configura opciones generales y de [:fontawesome-solid-flag: **Sesión**](./race-formats/qualify-finals.md)

3.  Inscribe los pilotos participantes en [:fontawesome-solid-user: **Inscripciones**](./user-guide/races.md#inscripciones)

4.  :fontawesome-solid-circle-check: **Genera** e :fontawesome-solid-print: **imprime** las series de pilotos en [:fontawesome-solid-table-cells: **Series**](./user-guide/races.md#series)

	*Vuelve aquí al finalizar cada sesión para generar las series de la siguiente. Por ejemplo, para generar las series finales tras completar las clasificatorias*

5.  :fontawesome-regular-circle-check: **Confirma** las series de pilotos en [:fontawesome-solid-table-cells: **Series**](./user-guide/races.md#series)

	*Se generarán las mangas de la carrera*

6.  [:fontawesome-solid-upload: **Activa**](./user-guide/heats.md#mangas_1) y arranca ([:fontawesome-solid-circle-check: **Start**](./user-guide/heats.md#control-de-la-manga-activa)) las mangas sucesivamente en [:fontawesome-regular-clock: **Mangas**](./user-guide/heats.md)

7.  Sanciona y corrige si es necesario, e :fontawesome-solid-print: **Imprime** los resultados

---

### Instalación del programa

Requisitos:

- Windows Vista / 7 / 8 / 10

- Microsoft .NET Framework 4.5 o superior

- Módulo de voz compatible con SAPI 5 (Ivona, Loquendo, ...)

- Decodificador compatible AMB/MyLaps con conexión Serie o Ethernet

- Recomendado: Lector de ficheros PDF ([Foxit Reader](http://www.foxitsoftware.com/Secure_PDF_Reader/), [Adobe Reader](http://get.adobe.com/reader/), ...)

!!! warning "Opciones de ahorro de energía de Windows"
	Durante el cronometraje es importante que desactives las opciones de ahorro de energía del ordenador (entrada en suspensión, apagado del disco duro, etc...), ya que pueden interrumpir el funcionamiento del equipo durante los períodos de inactividad.  

---

### Instalación de las voces

Requiere instalar un módulo de voz externo (puede ser de pago, coste no incluído en la licencia Everlaps). Se recomienda el uso de [Ivona](http://www.ivona.com).

Una vez instaladas las voces se podrán seleccionar en [:fontawesome-solid-gear: **Ajustes**](./user-guide/config.md)

---

### Conexión del decodificador

Conectar decodificador AMB/MyLaps al ordenador y configurarlo según las instrucciones del fabricante.

Según el tipo de conexión, habrá que introducir los parámetros correctos en [:fontawesome-solid-gear: **Ajustes**](./user-guide/config.md)

- Conexión Serie: indicar puerto del ordenador en donde está conectado el decodificador (COM1, COM2, ...)

- Conexión Ethernet: indicar la dirección IP del decodificador (ejemplo: 192.168.1.2)


!!! warning "Conexión por cable de red (Ethernet)"
	
	- Si conectas el decodificador directamente al ordenador, es posible que necesites un [cable de red cruzado](http://es.wikipedia.org/wiki/RJ-45#Cable_cruzado). Si existe un switch o router intermedio no es necesario.
	
	- El decodificador y el ordenador deben estar en la **misma subred IP** (por ejemplo el ordenador en 192.168.0.1 y el decodificador en 192.168.0.2). Si no consigues que la conexión funcione quizá tengas que desactivar la opción de configuración automática DHCP en el decodificador e introducir la dirección IP manualmente utilizando los botones y la pantalla LCD del mismo.
	
	
	
