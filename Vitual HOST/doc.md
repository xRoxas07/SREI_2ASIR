# ACTIVIDAD 5: VIRTUAL HOST

### EJERCICIO 1: Crea un directorio para el usuario virtual “informatica” en /home/ftp/informatica

Primero, vamos a crear un nuevo directorio llamado "informatica" con el comando "**sudo mkdir /home/ftp/informatica**"
 
![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_1.png)


### EJERCICIO 2: Cambia el propietario del directorio creado anteriormente mediante “chown” al usuario ftp

Para cambiar el propietario del directorio creado anteriormente mediante “chown” al usuario ftp usaremos el comando "**sudo chown -R ftp /home/ftp/informatica**"


![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_2.png)



### EJERCICIO 3: Crea un usuario virtual “informatica” mediante “ftpasswd”

Creamos un usuario virtual llamado "**informatica**" mediante "**ftpasswd**" usando "**sudo ftpasswd --passwd --file=/etc/proftpd/ftpd.passwd --name=informatica --uid=1001 --gid=1001 --home=/home/ftp/informatica --shell=/bin/false**" cunado ejecutemos el comando nos pedira que le agregemos una contraseña (en mi caso le he añadido la contraseña "linux").

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_3.png)



### EJERCICIO 4: Haz los cambios necesarios en el fichero de configuración de proftpd

Entreremos al archivo de configuracion de "**proftd**" y haremos siguientes los cambios.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_4.png)



### EJERCICIO 5: Crea un sitio virtual para “informatica.marisma.local”

Para este ejercicio, vamos a crearemos el sistio virtual para "**informatica.marisma.local**" con el "**comando sudo nano /etc/apache2/sites-available/informatica.marisma.local.conf**"

Y lo editaremos el archivo de esta manera.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_5.png)



### EJERCICIO 6: Modifica el fichero de zona del DNS para que resuelva adecuadamente

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_6.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_7.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_8.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_9.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/Vitual%20HOST/Imagenes/Screenshot_10.png)
