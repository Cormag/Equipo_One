Registro de eventos en linea

Se encuentra la problemática de tener control de los eventos registrados para una comunidad tecnológica de trabajo colaborativo, llamado Hacker Garage.

Todos los eventos registrados en el sistema deben poder ser consultados por medio de un canal de RSS, para poder ser agregado en un lector de RSS y otros sistemas de automatizado.

Cualquier persona al ingresar al sitio podrá ver por medio de un calendario -con distintas vistas que son por fechas, precio y categorias- los eventos registrados, y sobre todo, tendrá acceso a un botón permanente en todas las vistas para dar de alta eventos.

Si un usuario da clic en ese botón, por medio del sistema de login de Twitter podrá registrar un evento a realizarse dentro de las instalaciones del Hacker Garage y automáticamente será agregado a la base de datos del sistema.

Igualmente, cualquier usuario loggeado por medio de Disqus podrá agregar comentarios a los eventos registrados.

Un usuario que previamente ha registrado eventos (es decir que ya esta registrado en la base de datos) tendrá de manera permanente un botón con acceso a su cuenta, donde podrá listar sus eventos clasificados por aquellos que ya han sido aceptados por los administradores, aquellos que han sido rechazados, así como aquellos que están pendientes de evaluación. Las acciones a realizar con estos eventos será edición y eliminación.

El administrador (el cual es dado de alta directamente en la base de datos) podrá aceptar eventos, cancelarlos -si lo desea, agregará mensaje del motivo-, y editarlos.

Tanto el usuario registrado como el administrador podrán obtener archivos con listados de eventos, o eventos individuales en formatos XLS y/o PDF.

Datos a guardar de los eventos:
+ Nombre del evento
+ Flyer (imágen en cualquier formato con ancho de 500px sin importar el alto)
+ Texto libre (puede incluir tags html)
+ Precio
+ Capacidad (la cual puede ser una cantidad y debe aceptar ilimitada como una capacidad)
+ Categoria (curso/taller, conferencia, convivencia) pero el administrador por medio de una sección de administración debe poder dar de alta mas categorías.
+ Quien agrega el evento (que es la imágen del usuario en twitter y su arroba)
+ Fecha del evento (la cual solo puede ser una fecha superior a la fecha en que se crea el evento)
+ Fecha de creación (la cual no se muestra cuando el evento se publica, pero sirve al administrador para situaciones de BI).

Plugins y configuraciones extras serán tomadas en cuentapara mejores en calificación
+ Rewrite en Apache para la url de los eventos con el id del evento, title del evento y su fecha
+ Manejar distintos colores a las categorías de eventos en la vista de calendario
+ Crear la conexión de MySQL hacia la librería de calendario como un WebService
+ Utilizar diseños responsivos

Notas de programación
+ El manejo de las vistas de calendario se hace por medio de una librería de jQuery
+ Para conectar esa librería con los datos de la base de datos se hace por medio de JSON
+ Para el manejo de comentarios se utiliza el recurso Disqus