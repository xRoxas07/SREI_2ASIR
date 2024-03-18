# ACTIVIDAD 6: PROFTPD - TLS

### EJERCICIO 1:  Instala filezilla

Primero instalaremos el filezilla si no lo tenemos

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/FTP%20Privado%20y%20Anonimo/Imagenes/Screenshot_8.png)


### EJERCICIO 2: Configura filezilla para usar una conexión TLS y comprueba que funciona correctamente.

Despues, nos iremos al archivo de configuración con "**sudo nano /etc/proftpd/proftpd.conf**" y lo editaremos de la siguiente manera


![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_1.png)

Luego vamos a editar el archivo de configuración "**modules.conf**" con el comando "**sudo nano /etc/proftpd/modules.conf**"


![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_2.png)

El siguiente paso que haremos será instalaremos el servicio "**proftpd-mod-crypto**" con el comando "**sudo apt install proftpd-mod-crypto**"


![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_3.png)

Cuando este instalado, entraremos en el archivo de configuracion "**tls.conf**" con "**sudo nano /etc/proftpd/tls.conf**" y lo editaremos de la siguiente manera.


![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_4.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_5.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_6.png)

Una vez editado toda la configuracion reiniciaremos el servicio "**proftpd**" con"**sudo systemctl restart proftpd**" para aplicar todos los cambios.

Ahora cuando reiniciemos, nos iremos al archivo de configuracion de "**tls.conf**" y usaremos un comando para generar un certificado de seguridad.

![image](https://github.com/Josex02/SREI-ASIR2/assets/91255971/2214b1bc-a21a-467b-9057-3506f9f2ddc2)

Lo usaremos como comando de la misma forma que te muestro en la imagen

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_7.png)

Cuando hayamos hecho correctamente los pasos anteriores, nos dirigiremos a "**filezilla**" y nos conectaremos con la siguiente configuracion.

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_8.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_9.png)

![image](https://github.com/xRoxas07/SREI_2ASIR/blob/main/ProFTPD%20-%20TLS/Imagenes/Screenshot_10.png)

![image](https://github.com/Josex02/SREI-ASIR2/assets/91255971/0c434463-c0cc-47b4-87b4-59c955111c79)
