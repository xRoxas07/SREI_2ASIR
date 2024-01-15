**1. ¿Qué es TLD? ¿Cómo se clasifican los dominios de nivel superior?, Pon algunos ejemplos**

TLD significa "Top-Level Domain" o "Dominio de Nivel Superior" en español. Los TLD son la última parte de un nombre de dominio en Internet, que se encuentra después del último punto.

Los TLD se clasifican en varias categorías, y cada categoría tiene un propósito específico. Aquí hay algunas de las principales clasificaciones de TLD:

**TLD genéricos (gTLD):**

.com: Comúnmente utilizado para sitios web comerciales y de negocios.
.org: Originalmente destinado a organizaciones sin fines de lucro.
.net: Inicialmente pensado para redes y proveedores de servicios relacionados con Internet.

**TLD de infraestructura (arpa):**

Usado para propósitos técnicos y de infraestructura.

**TLD patrocinados (sTLD):**

Diseñados para comunidades específicas o para propósitos especiales. Ejemplos incluyen .gov (gobierno), .edu (educación), y .mil (militar).

**TLD de código de país (ccTLD):**

Asociados con países o territorios específicos. Por ejemplo, .us (Estados Unidos), .uk (Reino Unido), .es (España).

**TLD de nueva generación (ngTLD):**

Introducidos más recientemente para ampliar las opciones de dominios. Ejemplos incluyen .app, .blog, .guru.

**2. ¿Qué es FQDN?, Pon algún ejemplo de FQDN**

FQDN significa "Fully Qualified Domain Name" en inglés, y se refiere a un nombre de dominio completo y específico en el sistema de nombres de dominio (DNS) de Internet.
Un FQDN incluye el nombre de host y el dominio de nivel superior (TLD) para formar una ruta completa y única hacia un recurso en Internet.

Un FQDN sigue la estructura: **nombre-de-host.dominio.tld**

- nombre-de-host es el nombre asignado al host o servidor.
- dominio es el nombre de dominio al que pertenece el host.
- tld es el dominio de nivel superior, como .com, .org, .net, etc.

Ejemplo de FQDN: **www.ejemplo.com**

**3. ¿Qué son los root servers? , ¿Cuántos root servers hay?, ¿Cuántos servidores raíz físicos existen y dónde se encuentran?, ¿Qué es anycast?**

Los "root servers" son un conjunto de servidores de nombres de
dominio que constituyen la infraestructura principal del sistema de nombres de 
dominio en Internet. Estos servidores raíz contienen información sobre la ubicación
de los servidores de nombres de dominio de nivel superior (TLD) y ayudan a 
dirigir las solicitudes de DNS a los servidores adecuados.

A enero de 2022, hay 13 servidores raíz designados con letras de la A a la M. 
Sin embargo, es importante destacar que estos 13 servidores raíz no son máquinas
individuales, sino que son instancias replicadas en todo el mundo para mejorar la redundancia
y la disponibilidad del sistema. Estas instancias replicadas utilizan la técnica conocida como **anycast**.

Anycast es una técnica de red en la que múltiples nodos (en este caso, servidores) comparten la misma dirección IP
y los paquetes de datos se envían al nodo más cercano geográficamente. En el contexto de los servidores raíz,
esto significa que los 13 servidores raíz comparten la misma dirección IP, pero están distribuidos en
diferentes ubicaciones geográficas alrededor del mundo. Cuando un usuario realiza una solicitud DNS,
la red dirigirá la solicitud al servidor raíz más cercano según la topología de la red.

**4. ¿Qué es un archivo de zona (zone file)? Indica para qué sirven los registros de un archivo de zona. Pon un ejemplo de un archivo de zona e interpreta la información almacenada**

 Un archivo de zona (zone file) es un archivo de texto utilizado en el sistema de nombres de dominio
 para almacenar información sobre la asignación de nombres de dominio a direcciones IP y 
 otros recursos de red. Estos archivos son utilizados por servidores DNS para resolver 
 consultas y dirigir el tráfico de Internet a los destinos correctos.

Algunos de los registros de recursos más comunes incluyen:

**A (Address) Record:** Asocia un nombre de dominio con una dirección IPv4.
ejemplo.com.     IN    A      192.168.1.1

**AAAA (IPv6 Address) Record:** Similar al A Record, pero para direcciones IPv6.
ejemplo.com.     IN    AAAA   2001:0db8:85a3:0000:0000:8a2e:0370:7334

**CNAME (Canonical Name) Record:** Asocia un nombre de dominio con otro nombre de dominio (alias).
www.ejemplo.com. IN    CNAME  ejemplo.com.

**MX (Mail Exchange) Record:** Especifica los servidores de correo electrónico para el dominio.
ejemplo.com.     IN    MX     10 mail.ejemplo.com.

**NS (Name Server) Record:** Indica los servidores de nombres autoritativos para el dominio.
ejemplo.com.     IN    NS     ns1.ejemplo.com.

**SOA (Start of Authority) Record:** Proporciona información sobre el dominio y el servidor autoritativo.
ejemplo.com.     IN    SOA    ns1.ejemplo.com. admin.ejemplo.com. (
                                2024011501 ; Serial
                                3600       ; Refresh (1 hora)
                                1800       ; Retry (30 minutos)
                                604800     ; Expire (1 semana)
                                86400 )    ; Minimum TTL (1 día)

