Creamos el Usuario 

CREATE USER 'nuevo_usuario'@'localhost' IDENTIFIED BY 'contraseña'; 

Asignar Privilegios 

GRANT ALL PRIVILEGES ON * . * TO 'nuevo_usuario'@'localhost';

Aplicar Cambios 
FLUSH PRIVILEGES;

Estos son los comandos más utilizados en MySQL:

CREATE: permite a los usuarios crear una base de datos o una tabla
SELECT: permite a los usuarios recuperar datos
INSERT: permite a los usuarios agregar nuevas entradas en las tablas
UPDATE: permite a los usuarios modificar entradas existentes en tablas
DELETE: permite a los usuarios borrar entradas de la tabla
DROP: permite a los usuarios eliminar tablas de bases de datos completas

GRANT CREATE, SELECT ON * . * TO 'nombre_usuario'@'localhost';

REVOKE ALL PRIVILEGES ON * . * FROM 'nombre_usuario'@'localhost';

DROP USER ‘nombre_usuario’@‘localhost’;
