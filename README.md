# entorno-wordpress
Crear un entorno de desarrollo para Wordpress en una maquina virtual (Ubuntu, Nginx, Php y mySql)
# Entorno de Desarrollo

## 1 - Maquina Virtual 

Instalar [Virtual Box](https://www.virtualbox.org/)

Configurar la red de la VM en modo puente

## 2 - Sistema operativo en la VM
Descargar [Ubuntu](https://ubuntu.com/download) desde la pagina de la distro oficial y conectarlo como disco IDE a la VM.

## 3 - Instalar el webserver en el SO

Usamos [nginx](https://www.nginx.com/) en el port 80.


### Instalación 
Desde la consola de la VM corremos:

```bash
user@computer:~$ apt install nginx
```

Luego instalamos la ultima version disponible de php y los módulos que necesita wordpress para funcionar correctamente:

```bash 
user@computer:~$ sudo apt install php-fpm php-mysql php-gd php-mbstring php-xml php-json php-curl php-zip php-soap php-intl
````

## 4 - Instalar el motor de base de datos en el SO
Usamos Mysql 


### Instalación 
Desde la consola de la VM corremos:

```bash
user@computer:~$ apt install mysql-server
```

Acceso cliente mysql:

```bash
user@computer:~$ sudo mysql
```

### Crear el entorno de datos de Wordpress

```sql
SHOW DATABASES;  /* Muestra la lista de bases de datos existentes en el servidor */

CREATE DATABASE wordpress; /* Creamos la base de datos de Wordpress */

CREATE USER ‘wordpress’@‘localhost’ identifica by ‘password_123’; /* Crear el usuario que ustilizará wordpress para conectarse a la DB */

grant all privileges on wordpress.* to ‘wordpress’@‘localhost’; /* Le damos permiso total sobre la base de datos ‘wordpress’ al usuario ‘wordpress’ */
````



### Obtener wordpress 

Usando wget, descargamos la ultima version del wordpress

```bash
user@computer:~$ wget https://wordpress.org/latest.zip
user@computer:~$ unzip latest.zip
```
 

sudo apt update


## comandos linux
cd (change directory) navegar por las carpetas
	.. (carpeta atrás)
       / (carpeta host)

mkdir (make directory) crear directorio / carpeta

mv [origen] [destino] mover archivos o carpetas


https://www.namecheap.com/


