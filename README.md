# **TENDENCIAS TECNOLÓGICAS**
Tendencias tecnologicas - Prof. Marco Guaman
***
## Crear una cuenta en Docker.hub
![docker-cta](https://user-images.githubusercontent.com/91167225/197310621-94c1bfc4-7904-499f-a6a2-0073798c756e.jpg)

## Luego de crear la cuenta, abrimos la página PLay with Docker. Enlazamos la cuenta y clicqueamos en start
![play-docker](https://user-images.githubusercontent.com/91167225/197310674-fbe0d4f8-3108-4b4a-b1fe-eea5efefa0d5.jpg)

## Al ingresar, creamos una nueva instancia donde se abrirá una terminal para ingresar los códigos
![create-instance](https://user-images.githubusercontent.com/91167225/197310833-3c2d7771-1292-464d-92f6-12ea810e88d0.jpg)

## Se ingresa el código para correr el servidor web
![code-serve](https://user-images.githubusercontent.com/91167225/197310915-535b82b0-71a6-46be-9f18-b6c53d3e6cc1.jpg)

## Para conocer el estatus del servidor, se ingresa "docker ps"
![code-status](https://user-images.githubusercontent.com/91167225/197310945-c6c4ffbd-1d64-42a9-8d8d-113c1672b656.jpg)

## Para ingresar al puerto creado, se da click en open port y se ingresa el numero del puerto
![open-port](https://user-images.githubusercontent.com/91167225/197311013-f206dfca-1a14-497e-8d11-fda9a74451b2.jpg)

## Por último, redigirá a una nueva ventana donde se puede observar el contenedor creado
![new-window-ngnix](https://user-images.githubusercontent.com/91167225/197311083-af28c1e6-38c8-48a0-b450-5b64d093e674.jpg)

-----
-----

# **SERVER WEB - INSERT NEW INDEX.HTML**
***
## Creamos una nueva instancia, donde insertaremos el codigo para correr un servidor
docker run --name nombreServer -p 80:80 -d nginx


## Luego creamos un archivo HTML. Ingresamos el codigo "vi nombreArchivo.html"


## En la terminal, escribimos el codigo o el texto a visualizarse en el archivo. Para salir y guardar, teclamos "ESC" y escrbimos ":wq" y ENTER


## Ahora, debe insertar el archivo con el siguiente comando
docker cp nombreArchivo.html nombreServer:/usr/share/nginx/html/nombreArchivo.html

## Abrimos el server ingresando el número del puerto

## Al abriser una nueva ventana, agregamos en la URL "/nombreArchivo.html"

## Finalmente se nos abrirá el documento creado con la información ingresada

