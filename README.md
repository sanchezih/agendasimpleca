

# AgendaSimpleCA
AgendaSimpleCA es una aplicacion que permite dar de alta, modificar y eliminar datos de personas.
Esta hecha con Java, JSP y MySQL.

## Variables de entorno
El host en donde corra la aplicacion debera tener configuradas las siguientes variables de entorno:

```
CA_MYSQL_SERVER_IP=127.0.0.1
CA_MYSQL_SERVER_USERNAME=aplicadauser
CA_MYSQL_SERVER_PASSWORD=Unapassword1234!
CA_MYSQL_SERVER_PORT=3306
```

## Motor MySQL

### Script de inicializacion 
```
-- Creacion de la base de datos
DROP DATABASE IF EXISTS agendasimpleca;
CREATE DATABASE agendasimpleca;
USE agendasimpleca;

-- Creacion de la tabla users
CREATE TABLE users (
     id        INT NOT NULL auto_increment,
     firstname VARCHAR(45) DEFAULT NULL,
     lastname  VARCHAR(45) DEFAULT NULL,
     dob       DATE DEFAULT NULL,
     email     VARCHAR(100) DEFAULT NULL,
     PRIMARY KEY (id)
  );

-- Inicializacion
INSERT INTO users (firstname, lastname, dob, email) VALUES ('Maria', 'Fernandez', '1988-07-07', 'maria@fernandez.com');
INSERT INTO users (firstname, lastname, dob, email) VALUES('Jorge', 'Leone', '1982-10-07', 'jorge@leone.com'); 
```
