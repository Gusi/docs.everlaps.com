# :fontawesome-solid-user: Inscripciones con la carrera en marcha

En Everlaps es muy sencillo modificar las inscripciones y/o series sin tener que regenerar la distribución existente.

---

### Inscripción de pilotos después de haber generado las series y mangas

Cuando un piloto llega tarde a la carrera y ésta ya ha comenzado, es posible añadirlo de forma sencilla sin tener que volver a regenerar las series o las mangas.

1. Si el piloto no existe en la base de datos, lo damos de alta en la [lista de pilotos](../user-guide/drivers.md)
2. Se selecciona la [carrera](../user-guide/races.md) en la que se quiere inscribir al piloto
3. Se localiza al piloto en la [lista de pilotos disponibles](../user-guide/races.md#pilotos-disponibles)
4. Se [inscribe](../user-guide/races.md#inscripciones) al piloto en la carrera
5. Nos situamos en la pestaña de [series](../user-guide/races.md#series) y elegimos la sesión en donde vamos a añadir el piloto
6. Se localiza el piloto en el panel de [pilotos sin serie](../user-guide/races.md#pilotos-sin-serie)
7. Se arrastra el piloto a la serie en la que se quiere añadir, siempre que no sea la serie a la que pertenezca la manga activa
8. Si hubiese que inscribir a varios pilotos, también se podría generar una **nueva serie** y arrastrar allí a todos los pilotos. Luego habría que pulsar en el botón *Confirmar* para generar las mangas correspondientes a la nueva serie.

### Borrado de pilotos que no van a participar en la sesión o la carrera

Una vez generada las series, es posible eliminar pilotos (arrastrándolos al panel de [pilotos sin serie](../user-guide/races.md#pilotos-sin-serie)) siempre que no existan resultados de ninguna manga perteneciente a esa serie.

De forma similar, si se desea desinscribir al piloto de la carrera, se puede eliminar su inscripción siempre y cuando el piloto no pertenezca a ninguna serie de entre las sesiones de la carrera.

Si algún piloto está inscrito en alguna manga que ha sido disputada, pero se desea evitar que el piloto participe en las siguientes sesiones, se puede marcar como *excluído* en la [lista de inscripciones](../user-guide/races.md#inscripciones).
