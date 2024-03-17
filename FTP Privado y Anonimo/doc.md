# ACTIVIDAD 4 - FTP PRIVADO Y ANONIMO

### EJERCICIO1 - Configura proftpd para que los usuarios accedan al directorio /home/ftp (puedes usar DefaultChdir). ¿Cual es la diferencia entre DefaultRoot y DefaultChdir?

Para comenzar a hacer el ejercicio, tendremos que instalar los servicios ProFTPd y bind9, los cuales los haremos con el comando "**sudo apt-get install proftpd**".

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_1.png)

Despues instalaremos el servicio bind9 con el comando "**sudo apt install bind9**".

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_2.png)

Luego entraremos al archivo "proftpd.conf" con el comando "**sudo nano /etc/proftpd/proftpd.conf**" para empezar a configurar ProFTP.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_3.png)

Cuando entremos, modificaREMOS la configuración añadiendole la ruta "**DefaultRoot /home/ftp**"

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_4.png)


### EJERCICIO2 - No se permitirá subir ni eliminar nada de la carpeta ftp.

Vamos a restringir las acciones en la carpeta ftp para que no se permita subir ni eliminar nada de la carpeta configurandola de esta manera.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_5.png)


### EJERCICIO3 - Configura el acceso mediante usuario anónimo 

Editaremos el archivo proftpd.conf y mostraremos los siguientes comandos.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_6.png)


### EJERCICIO4 -  Permite que el usuario anónimo pueda escribir si accede desde la red 10.6.0.x

Para permitir que el usuario anónimo pueda escribir lo haremos mediante "Limit WRITE".

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_7.png)

Finalmente, reiniciaremos el servicio para oder aplicar todos cambios que hemos realizado anteriormente con el comando "**sudo service proftpd restart**".

### COMPROBACION

Para hacer la comprobación del ejercicio instalaremos "**FileZilla**" con el comando "**sudo apt-get install filezilla**".

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_8.png)

Crearemos un nuevo usuario con el comando "**sudo adduser usuarioftp**".

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_9.png)

Y cuando ya hayamos creado el nuevo usuario nos iremos a FileZilla y una vez dentro vamos a conectarnos.
Para ello abriremos el gestor de sitios y lo rellenaremos con los datos que hemos creado.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_10.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_11.png)

Cuando le demos a conectar tendremos que poner la contraseña que le hemos establecido.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_12.png)

Por último, veremos que después de introducirle la contraseña ya nos hemos conectado correctamente.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_13.png)
