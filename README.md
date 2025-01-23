# Conexión base de datos relacional

## ¿Qué es JDBC y cuáles son sus componentes?

JDBC (Java Database Connectivity) es una API estándar de Java que permite conectar aplicaciones Java a bases de datos relacionales y realizar operaciones sobre ellas, como ejecutar consultas SQL y actualizar datos. Es parte del paquete estándar de Java (Java SE) y está diseñado para proporcionar una interfaz uniforme para interactuar con diferentes sistemas de bases de datos, independientemente de su proveedor. JDBC actúa como un puente entre la aplicación Java y la base de datos, facilitando la comunicación mediante comandos SQL.

JDBC se basa en el uso de controladores específicos de cada base de datos que implementan la interfaz definida por JDBC. Esto permite que las aplicaciones Java puedan conectarse a cualquier base de datos para la que exista un controlador compatible, brindando flexibilidad y portabilidad.

**Componentes de JDBC**

- **Driver Manager**: Administra una lista de controladores de bases de datos y facilita la conexión a una base de datos seleccionando el controlador adecuado.

- **Driver**: Actúa como intermediario entre la aplicación Java y la base de datos. Traduce las llamadas JDBC en comandos específicos del proveedor de la base de datos.

- **Connection**: Representa una conexión activa con una base de datos. Se utiliza para ejecutar consultas y comandos SQL.

- **Statement**: Permite ejecutar sentencias SQL simples (como consultas, inserciones, etc.).

- **PreparedStatement**: Subclase de Statement que precompila consultas para un mejor rendimiento y protección contra ataques de inyección SQL.

- **CallableStatement**: Subclase de Statement utilizada para ejecutar procedimientos almacenados.

- **ResultSet**: Representa un conjunto de resultados devueltos por una consulta SQL. Se utiliza para leer los datos obtenidos.

- **SQLException**: Clase para manejar errores relacionados con bases de datos durante el uso de JDBC.


| **Característica**      | **Slick** | **Doobie**                                    | 
|---------------------------|------------------|------------------------------------------------ |
| `Descripción`  | Una librería de mapeo objeto-relacional (ORM) funcional que abstrae las consultas SQL. |Un enfoque más liviano y funcional para interactuar con bases de datos directamente usando SQL. |                                                    |
| `Paradigma`   | ORM funcional con soporte para consultas DSL en Scala.         | Basado en SQL puro, sin abstracciones ORM. | 
| `Uso principal` | Abstracción de datos, ideal para trabajar con estructuras de datos complejas.          | Acceso directo y eficiente a bases de datos con control explícito de las consultas. |       
| `Curva de aprendizaje`| Mayor, debido a la abstracción del ORM y el DSL propio. |Moderada, especialmente si ya se tiene experiencia en SQL. | 
| `Soporte para SQL personalizado` | Limitado, ya que utiliza su propio lenguaje DSL, aunque permite consultas SQL sin procesar. | Completo, ya que las consultas se escriben en SQL puro. | 
| `Gestión de conexiones` | Usa un motor interno para manejar conexiones automáticamente.          |  Permite un control explícito del manejo de conexiones.|  
| `Interoperabilidad con JDBC`                | Abstrae completamente JDBC.        | Trabaja directamente sobre JDBC.        |                
