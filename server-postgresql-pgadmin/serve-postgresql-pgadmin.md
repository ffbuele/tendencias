
# **CONTENEDORES DE SERVIDOR Y PGADMIN**
---
## **1.-** Primero debe abrir el Play With Docker y crear una nueva instancia

![open-container](/server-postgresql-pgadmin/img/1-open-container.png)

## **2.-** Luego escribir el código donde se detalla el nombre, contraseña y el puerto del contenedor del Postgres

![create-postgres-container](/server-postgresql-pgadmin/img/2-create-postgres-container.png)

## **3.-** De igual manera, escribir el código para el contenedor del pgAdmin, se detalla usuario, contraseña y su puerto correspondiente. En este caso, el puerto es 8090

![create-pgadmin-container](/server-postgresql-pgadmin/img/3-create-pgadmin-container.png)

## **4.-** Crear una red con su respectivo nombre.

![create-network](/server-postgresql-pgadmin/img/4-create-network.png)

## **5.-** Luego, conectar la red con el contenedor de Postgres, se debe escribir el nombre de la red y de la base de datos Postgres

![connect-network-postgres](/server-postgresql-pgadmin/img/5-connect-network-postgres.png)

## **6.-** También, conectar la red con el contenedor de pgAdmin.

![connect-network-pgadmin](/server-postgresql-pgadmin/img/6-connect-network-pgadmin.png)

## **7.-** Se puede inspeccionar las redes IPs con el comando "docker inspect nombreRed"

![inspect-network](/server-postgresql-pgadmin/img/7-inspect-network.png)

## **8.-** Al abrir el puerto 8090, se abre una nueva ventana con la interfaz gráfica de pgAdmin. Al ingresar el usuario y contraseña podrá acceder al panel administrativo

![open-port-pgadmin-8090](/server-postgresql-pgadmin/img/8-open-port-pgadmin-8090.png)
![ingresar-credenciales-pgadmin](/server-postgresql-pgadmin/img/9-ingresar-credenciales-pgadmin.png)

## **9.-** Debe agregar un servidor, para ello hace click en añadir server, donde va a configurar el nombre, ingresar el nombre del contenedor, usuario y contraseña para que pueda crearse el mismo.

![settings-server](/server-postgresql-pgadmin/img/10-settings-server.png)

## **10.-** Al final, tendrá la interfaz del servidor.

![server-created](/server-postgresql-pgadmin/img/11-server-created.png)
