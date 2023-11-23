Busca información sobre las siguientes directivas y el valor que toman por defecto y el lugar donde se encuentra definida.

**Directivas de identificación**

ServerName: Valor por defecto: Ninguno (debe ser configurado explícitamente).
            Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales (por ejemplo, en un archivo .conf de un sitio).
            Función: Define el nombre del servidor y el puerto para las solicitudes entrantes. Es esencial para la generación de URLs absolutas y puede afectar la redirección y la resolución DNS.
            
ServerAdmin:Valor por defecto: webmaster@localhost
            Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales. 
            Función: Especifica la dirección de correo electrónico del administrador del servidor. Se utiliza para generar mensajes de error y notificaciones de problemas.
            
ServerTokens:Valor por defecto: Full (muestra la información completa sobre el servidor).
             Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
             Función: Controla la información que se muestra en los encabezados de respuesta del servidor y en los mensajes de error. Puede tomar valores como "Full" (mostrar toda la información), "OS" (mostrar solo el nombre del sistema operativo) o "Min" (mostrar solo Apache).

**Directivas de localización de ficheros**

DocumentRoot: Valor por defecto: Depende de la instalación, comúnmente /var/www/html.
              Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
              Función: Especifica el directorio raíz donde se encuentran los documentos que se sirven a través del servidor. Todas las rutas relativas a los documentos se consideran en relación con este directorio.
              
ErrorLog:	Valor por defecto: logs/error_log dentro del directorio definido por ServerRoot.
          Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
          Función: Define la ubicación del archivo de registro de errores del servidor. Registra mensajes de error, advertencias y otra información relevante.
          
CustomLog:  Valor por defecto: No hay un valor por defecto, pero se usa comúnmente logs/access_log.
            Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
            Función: Especifica la ubicación y el formato del archivo de registro de acceso personalizado del servidor. Registra información sobre las solicitudes entrantes y las respuestas servidas.
            
ServerRoot:Valor por defecto: Depende de la instalación, comúnmente /etc/httpd o /usr/local/apache.
           Ubicación: Archivo de configuración principal (httpd.conf).
           Función: Define el directorio raíz del servidor web. Todos los caminos relativos utilizados en la configuración se consideran relativos a este directorio.

**Directivas de control de la conexión**

Timeout: Valor por defecto: 300 segundos (5 minutos).
         Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
         Función: Establece el tiempo máximo (en segundos) que el servidor espera para recibir una solicitud completa antes de responder con un error.
         
KeepAlive: Valor por defecto: Off (deshabilitado).
           Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
           Función: Habilita o deshabilita la funcionalidad Keep-Alive. Si está habilitada, permite que una conexión se mantenga abierta para procesar varias solicitudes, lo que puede mejorar el rendimiento.
           
MaxKeepAliveRequests: Valor por defecto: 100 (número máximo de solicitudes por conexión Keep-Alive).
                      Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
                      Función: Especifica el número máximo de solicitudes que se pueden realizar a través de una conexión Keep-Alive antes de cerrarla.
                      
KeepAliveTimeout: Valor por defecto: 5 segundos.
                  Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
                  Función: Establece el tiempo máximo (en segundos) que el servidor espera para recibir la siguiente solicitud en una conexión Keep-Alive antes de cerrarla.

**Otras**
LogLevel: Valor por defecto: "warn" (advertencias y errores).
          Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
          Función: Controla el nivel de detalle de los mensajes de registro. Puede ser utilizado para ajustar la cantidad de información registrada en los archivos de registro del servidor.
          
LogFormat: Valor por defecto: No hay un valor por defecto.
           Ubicación: Archivo de configuración principal (httpd.conf) o en archivos de configuración de sitios virtuales.
           Función: Define el formato de registro para los archivos de registro de acceso. Permite personalizar qué información se registra y cómo se presenta en los registros de acceso del servidor.
           
