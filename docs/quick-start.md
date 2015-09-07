## Inicio rápido

Se describen a continuación los pasos básicos para poder instalar y generar una carrera en Everlaps. Para información más detallada consulta el resto de la documentación.

---

### Acciones básicas

1.  Introduce los datos de los pilotos en [&fa-users; **Pilotos**](./user-guide/drivers/index.html)

2.  Crea una nueva carrera en [&fa-road; **Carreras**](./user-guide/races/index.html), configura opciones generales y de [&fa-flag; **Sesión**](./race-formats/qualify-finals/index.html)

3.  Inscribe los pilotos participantes en [&fa-user; **Inscripciones**](./user-guide/races/index.html#inscripciones)

4.  &fa-check-circle; **Genera** e &fa-print; **imprime** las series de pilotos en [&fa-th; **Series**](./user-guide/races/index.html#series)

	*Vuelve aquí al finalizar cada sesión para generar las series de la siguiente. Por ejemplo, para generar las series finales tras completar las clasificatorias*

5.  &fa-check-circle-o; **Confirma** las series de pilotos en [&fa-th; **Series**](./user-guide/races/index.html#series)

	*Se generarán las mangas de la carrera*

6.  [&fa-upload; **Activa**](./user-guide/heats/index.html#mangas_1) y arranca ([&fa-check-circle; **Start**](./user-guide/heats/index.html#control-de-la-manga-activa)) las mangas sucesivamente en [&fa-clock-o; **Mangas**](./user-guide/heats/index.html)

7.  Sanciona y corrige si es necesario, e &fa-print; **Imprime** los resultados

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

Una vez instaladas las voces se podrán seleccionar en [&fa-gear; **Ajustes**](./user-guide/config/index.html)

---

### Conexión del decodificador

Conectar decodificador AMB/MyLaps al ordenador y configurarlo según las instrucciones del fabricante.

Según el tipo de conexión, habrá que introducir los parámetros correctos en [&fa-gear; **Ajustes**](./user-guide/config/index.html)

- Conexión Serie: indicar puerto del ordenador en donde está conectado el decodificador (COM1, COM2, ...)

- Conexión Ethernet: indicar la dirección IP del decodificador (ejemplo: 192.168.1.2)


!!! warning "Conexión por cable de red (Ethernet)"
	
	- Si conectas el decodificador directamente al ordenador, es posible que necesites un [cable de red cruzado](http://es.wikipedia.org/wiki/RJ-45#Cable_cruzado). Si existe un switch o router intermedio no es necesario.
	
	- El decodificador y el ordenador deben estar en la **misma subred IP** (por ejemplo el ordenador en 192.168.0.1 y el decodificador en 192.168.0.2). Si no consigues que la conexión funcione quizá tengas que desactivar la opción de configuración automática DHCP en el decodificador e introducir la dirección IP manualmente utilizando los botones y la pantalla LCD del mismo.
	
	
	
