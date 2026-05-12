📚 Gestión de Biblioteca - Java JDBC
Aplicación de consola en Java diseñada para la administración de un inventario bibliográfico. El proyecto utiliza MySQL como motor de persistencia y sigue el patrón de diseño DAO (Data Access Object) para garantizar una arquitectura escalable y organizada.

🚀 Funcionalidades
El sistema implementa un CRUD completo sobre la tabla de libros:

Insertar Libro: Registro de nuevos títulos con gestión de disponibilidad.

Mostrar Catálogo: Listado completo de los registros almacenados.

Buscar por Autor: Filtro dinámico mediante coincidencias parciales (LIKE).

Actualizar Precio: Modificación de valores numéricos mediante identificadores únicos.

Eliminar Libro: Borrado físico de registros de la base de datos.

🛠️ Tecnologías Utilizadas
Lenguaje: Java 17+

Base de Datos: MySQL 8.0

Driver: MySQL Connector/J

Seguridad: Uso de PreparedStatement para prevenir Inyección SQL.

📊 Estructura de Datos
El proyecto se basa en la tabla libros con la siguiente definición:

id: Clave primaria autoincremental.

titulo / autor / genero: Campos de texto (VARCHAR).

precio: Valor decimal de alta precisión (6,2).

disponible: Estado booleano del ejemplar.

⚙️ Configuración rápida
Base de datos: Ejecuta el script SQL proporcionado en el repositorio para crear biblioteca_db y poblar las tablas iniciales.

Driver: Importa el conector de MySQL a las librerías de tu proyecto (Maven/Gradle o JAR manual).

Credenciales: Ajusta el usuario y contraseña en la clase ConexionBD.java.

Ejecución: Inicia la aplicación desde la clase Main.java y sigue las instrucciones del menú en consola.
