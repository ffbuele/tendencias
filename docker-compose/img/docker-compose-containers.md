# CREAR DOCKER-COMPOSE PARA PGADMIN Y POSTGRES
---
## 1.- Crear una nueva instancia en la sesión de play with Docker

![crear-instancia](/docker-compose/img/1-crear-instancia.png)

## 2.- Debe crearse una carpeta e ingresar

![crear-carpeta](/docker-compose/img/2-crear-carpeta.png)

## 3.- Una vez dentro de la carpeta o directorio, debe crear un archivo con el nombre y extensión "docker-compose.yml"

![crear-archivo](/docker-compose/img/3-crear-archivo.png)

## 4.- Dentro del archivo, debe detallarse los parametros, nombre, puertos, credenciales, etc. Luego, se guarda y sale del editor.

![escribir-parametros](/docker-compose/img/4-escribir-parametros.png)

## 5.- En la consola debe correr el siguiente comando "docker-compose up -d" para ejecutar el archivo yml

![ejercutar-archivo-yml](/docker-compose/img/5.1-ejercutar-archivo-yml.png)

![ejecucion-completa](/docker-compose/img/5.2-ejecucion-completa.png)

## 6.- Luego de que se generen los contenedores, abrir el puerto 8090 donde tenemos la interfaz del pgadmin.

![interfaz-usuario](/docker-compose/img/6-interfaz-usuario.png)

## 7.- Crear el servidor con los datos definidos en el achivo yml

![crear-servidor](/docker-compose/img/7-crear-servidor.png)

## 8.- Al final, se podrá observar el servidor en funcionamiento

![servidor-corriendo](/docker-compose/img/8-servidor-corriendo.png)
