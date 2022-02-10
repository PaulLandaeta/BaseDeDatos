# Creacion de Usuarios

Para la creacion de usuarios en MySQL usamos el siguiente comando: 

`CREATE USER 'nuevo_usuario'@'localhost' IDENTIFIED BY 'contraseña';` 

donde nuevo_usuario es el nombre del usuario y contraseña la contraseña del usuario 

Ejemplo crear el usuario paul con la contraseña 123456

`CREATE USER 'paul'@'localhost' IDENTIFIED BY '123456';` 

###### Asignar Privilegios 

Una vez creado el usuario es necesario asignar privilegios para lo cual se usa el siguiente comando.

 `GRANT ALL PRIVILEGES ON * . * TO 'nuevo_usuario'@'localhost';`

Siguiendo el ejemplo para asignar todos los privilegios al usuario paul se debe usar el siguiente comando 

 `GRANT ALL PRIVILEGES ON * . * TO 'paul'@'localhost';`

###### Aplicar Cambios 

Una vez asignado los privilegios es necesario aplicar los cambios inmediatamente para ello se aplica el siguiente comando: 

`FLUSH PRIVILEGES;`

##### Privilegios 

Rara vez se crea usuarios con todos los privilegios de administración por lo cual es necesario crear usuarios con privilegios especificos. 

Estos son los comandos más utilizados en MySQL:

**CREATE**: permite a los usuarios crear una base de datos o una tabla
**SELECT**: permite a los usuarios recuperar datos
**INSERT**: permite a los usuarios agregar nuevas entradas en las tablas
**UPDATE**: permite a los usuarios modificar entradas existentes en tablas
**DELETE**: permite a los usuarios borrar entradas de la tabla
**DROP**: permite a los usuarios eliminar tablas de bases de datos completas

Como vemos en el siguiente comando solo daremos los privilegios de crear y seleccionar al usuario paul.

`GRANT CREATE, SELECT ON * . * TO 'paul'@'localhost';`

###### Revocar 

Algunas veces es necesario revocar privilegios a ciertos usuarios para ello tenemos el siguiente comando

`REVOKE ALL PRIVILEGES ON * . * FROM 'nombre_usuario'@'localhost';`

###### Eliminar Usuario

Para eliminar un usuario creado se puede utilizar el comando Drop User. 

`DROP USER ‘nombre_usuario’@‘localhost’;`

siguiendo el ejemplo y queremos eliminar el user paul: 

`DROP USER ‘paul’@‘localhost’;`

