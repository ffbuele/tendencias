# CREAR POSTGRES, PGADMIN Y SPRING BOOT
---
## 1.- Crear una nueva instancia en la sesión de play with Docker

![crear-instancia](/postgres-springBoot/img/1-crear-instancia.png)

## 2.- Debe crearse una carpeta e ingresar, dentro de la carpeta tiene que crear el archivo "docker-compose.yml"

![crear-carpeta-y-ejecutar-docker](/postgres-springBoot/img/2-crear-carpeta-y-ejecutar-docker.png)

## 3.- Dentro del archivo, debe detallarse los parametros, nombre, puertos, credenciales, etc. Luego, se guarda y sale del editor.

![insertar-informacion-docker](/postgres-springBoot/img/3-insertar-informacion-docker.png)

## 4.- En la consola debe correr el siguiente comando "docker-compose up -d" para ejecutar el archivo yml

![ejercutar-archivo-yml](/postgres-springBoot/img/4-ejecutar-archivo-yml.png)

## 5.- Luego de que se generen los contenedores, abrir el puerto 8090 donde tenemos la interfaz del pgadmin.

![abrir-puerto-8090](/postgres-springBoot/img/5-abrir-puerto-8090.png)

## 6.- Crear el servidor con los datos definidos en el achivo yml, al seleccionar la base de datos, puede observar la que se creó 

![crear-servidor](/postgres-springBoot/img/6.1-crear-servidor.png)

![servidor-creado](/postgres-springBoot/img/6.2-servidor-creado.png)

## 7.- En la instancia del docker, en la carpeta creada, debe bajarse el archivo con git clone

![clonar-archivo-git](/postgres-springBoot/img/7-clonar-archivo-git.png)

## 8.- Dirigirse a la ruta donde está el archivo "application.yml" o "application.properties" para editarlo.

![editar-archivo-yml-git](/postgres-springBoot/img/8-editar-archivo-yml-git.png)

## 9.- Dentro del archivo, editar el datasource con los datos definidos para el contenedor de postgres, el username, password y nombre de la base de datos. 

![editar-datasource](/postgres-springBoot/img/9-editar-datasource.png)

## 10.- Al ejecutar el codigo, se generará un contenedor maven para crear el archivo jar.

![ejecutar-maven](/postgres-springBoot/img/10-ejecutar-maven.png)

## 11.- Cuando se haya ejecutado correctamente, dento de la carpeta principal del proyecto git, crear el archivo "Dockerfile".

![crear-dockerfile](/postgres-springBoot/img/11-crear-dockerfile.png)

## 12.- Escribir las siguientes lineas dentro del archivo "Dockerfile", guardar y cerrar.

![contenido-archivo-jar](/postgres-springBoot/img/12-contenido-archivo-jar.png)

## 13.- Escribir el código para crear la imagen dentro de la carpeta principal del proyecto. 

![crear-imagen-sprintBoot](/postgres-springBoot/img/13-crear-imagen-sprintBoot.png)

## 14.- Después, crear el contenedor para el spring boot.

![crear-contenedor-springBoot](/postgres-springBoot/img/14-crear-contenedor-springBoot.png)

## 15.- Una vez creado el contenedor, abrir el puerto 8081

![abrir-puerto-8081](/postgres-springBoot/img/15-abrir-puerto-8081.png)

## 16.- Por último, se abrirá una nueva ventana en el navegador, debe editar la url agregando "/users", entonces podrá observar la información del spring boot.

![agregar-users-url](/postgres-springBoot/img/16.1-agregar-users-url.png)

![visualizar-datos-sprintBoot](/postgres-springBoot/img/16.2-visualizar-datos-sprintBoot.png)