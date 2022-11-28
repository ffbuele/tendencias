# <font color="red"> <center> DESPLIEGUE DE APP FRONT-END </center> </font>
---

## 1.- Crear Docker-compose

Dentro de una instancia, debe crear una carpeta (ffbuele) e ingresar, luego, nuevamente crear otra carpeta (db) donde estará el back-end e ingresar. Dentro de "bd" debe crear el archivo "docker-compose.yml".

<center> <img src="./img/1-docker-compose.png" style="max-width: 68%"> </center>

## 2.- Docker-compose.yml

Al crear el archivo docker-compose, en su contenido debe especificarse la version de los contenedores, nombres, puertos, usuarios, contraseñas, entre otros, para generar el contenedor del pgAdmin y postgres.

<center> <img src="./img/2.1-contenido-docker-compose.png" style="max-width: 68%"> </center>

Al guardar y salir del archivo, debe ejecutarlo para generar los contenedores.

<center> <img src="./img/2.2-ejecutar-docker-compose.png" style="max-width: 68%"> </center>

## 3.- Crear servidor Postgres

Para continuar con el tutorial, antes debe abrir el puerto 8090 e ingresar al pgAdmin.

<center> <img src="./img/3.1-puerto-8090.png" style="max-width: 68%"> </center>

Seguidamente, crear un nuevo servidor con los datos detallados para el contenedor postgres

<center> <img src="./img/3.2-crear-servidor.png" style="max-width: 68%"> </center>

Al crearlo, obtendrá el servidor creado correctamente.

<center> <img src="./img/3.3-servidor-creado.png" style="max-width: 68%"> </center>

## 4.- Git del Back-end

En la carpeta "db", se debe clonar el git donde está la app para el back-end para luego editar varios archivos que servirán para la conexión con la base de datos y front-end.

<center> <img src="./img/4-clonar-be.png" style="max-width: 68%"> </center>

## 5.- Editar application.

Se debe buscar el archivo "application.yml" o "application.properties" para editar los campos de datasource y enableCors.

<center> <img src="./img/5.1-editar-application.png" style="max-width: 68%"> </center>

Al ingresar al editor, se debe editar el datasource con los datos del contenedor Postgres (url, usuario y contraseña), y en el enableCors poner la dirección URL del puerto 3000. 

<center> <img src="./img/5.2-datos-editados-application.png" style="max-width: 68%"> </center>

## 6.- Editar Cors del back-end

Se debe buscar el archivo de la configuración de los Cors para editarlo.

<center> <img src="./img/6.1-editar-Cors.png" style="max-width: 68%"> </center>

Al ingresar al editor del archivo, debe actualizar la ruta del "allowebOrigins" por la ruta del puerto 3000 del Play with Docker

<center> <img src="./img/6.2-cors-originis-url.png" style="max-width: 68%"> </center>

## 7.- Editar controlador

Como en los casos anteriores, debe buscar el archivo del controlador, ubicado en la carpeta controller y abrirlo con el editor.

<center> <img src="./img/7.1-editar-controlador.png" style="max-width: 68%"> </center>

Dentro del editor, debe buscar donde se establecen los "origins" para actualizar la ruta, por la ruta generada para el puerto 3000 en Play with Docker.

<center> <img src="./img/7.2-controller-editado-url.png" style="max-width: 68%"> </center>

## 8.- Contenedor Maven

Para generar el archivo ".jar", antes debemos generador el contenedor maven con el siguiente comando, donde se debe tener en cuenta el nombre de la red de los contenedores y la ubicación del archivo, porque donde se escriba mal el código, **no se nos generará de manera correcta el contenedor**.

<center> <img src="./img/8-contenedor-maven.png" style="max-width: 68%"> </center>

## 9.- Dockerfile pare el Back-end

Dentro de la carpeta principal del git, se debe crear el archivo "Dockerfile", el cuál permite crear la imagen para la app del back-end.

<center> <img src="./img/9.1-crear-be-dockerfile.png" style="max-width: 68%"> </center>

Dentro del archivo, debe estar escrito el siguiente contenido. Despues, guardar y cerrar el editor del archivo.

<center> <img src="./img/9.2-contenido-dockerfile-be.png" style="max-width: 68%"> </center>

## 10.- Crear imagen y contenedor del Back-end

Es necesario dos comandos para crear tanto la imagen como el contenedor de la app back-end, estos son:

- "docker build -t nombreImagen ."
- "docker run -d --name nombreContenedor --network redDeContenedores -p 8081:8081 nombreImagen"

Luego de haber ejecutado los dos comandos, se creará el puerto 8081, el cuál es la conexión con la base de datos.

<center> <img src="./img/10-crear-imagen-y-contenedor-be.png" style="max-width: 68%"> </center>

## 11.- Git del Front-end

Es similar al proceso del back-end. Ahora se debe salir de la carpeta "db" para ubicarnos el la carpeta principal "ffbuele" del proyecto general.

Se debe clonar el repositorio de la app del front-end.

<center> <img src="./img/11-clonar-git-fe.png" style="max-width: 68%"> </center>

## 12.- Editar servicio

Luego de haber clonado el repositorio, tiene que ingresar a la carpeta. 

<center> <img src="./img/12.1-editar-userService.png" style="max-width: 68%"> </center>

El servicio de la app de front-end permite la conexión con la app del back-end para leer la información de la base de datos. Por tanto, se debe editar la URL por la ruta que nos genera el Play with Docker para el puerto 8081.

<center> <img src="./img/12.2-userService-editado-url.png" style="max-width: 68%"> </center>

## 13.- Dockerfile para el Front-end.

En la carpeta principal del repositorio de front-end, se debe crear el archivo "Dockerfile" para crear la imagen dentro de docker.

<center> <img src="./img/13.1-crear-dockerfile-fe.png" style="max-width: 68%"> </center>

El contenido del "Dockerfile" debe tener el siguiente texto que permitirá ejecutarse y crear la imagen para la app front-end. Luego, tiene que guardar y cerrar.

<center> <img src="./img/13.2-contenido-dockerfile-fe.png" style="max-width: 68%"> </center>

## 14.- Crear imagen para Front-end

Para crear la iamgen es necesario el siguiente comando:
- "docker build -t nombreImagen:latest ."
 
El mismo debe ser ejecutado dentro de la carpeta principal del proyecto de front-end.

<center> <img src="./img/14-crear-imgen-fe.png" style="max-width: 68%"> </center>

## 15.- Generar contenedor para Front-end

Una vez creada la imagen para la app front-end, se debe escribrir el siguiente comando:
- "docker run -d --name nombreContenedor --network redDeContenedores -p 3000:3000 nombreImagen" 

Al ejecutar el código se creará el contenedor con el puerto donde estará albergado la app front-end.

<center> <img src="./img/15-ejecutar-contenedor-fe.png" style="max-width: 68%"> </center>

## 16.- Puerto 3000 - App Front-End.

Para concluir el tutorial, se debe abrir el puerto 3000 en el  Docker. Se abrirá una nueva ventana donde se podrá observar la app del front-end.

<center> <img src="./img/16.1-abrir-puerto-3000.png" style="max-width: 68%"> </center>

Al navegar a "Usuarios", debemos observar la información recopilada de la base de datos. 

Si se puede observar correctamente la información de los usuarios, se ha realizado correctamente el tutorial, concluyendo todo el proceso satisfactoriamente.

<center> <img src="./img/16.2-react-fe-datosDB.png" style="max-width: 68%"> </center>