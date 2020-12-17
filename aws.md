- - -
# <center>CREAR UNA INSTANCIA </center> #
### Entramos en https://www.awseducate.com/student/s/classrooms y entramos en nuestro classroom y clickamos en:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/1.png)
### Entramos en **Crear una solución** y le damos a **Ejecute una máquina virtual.**
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/2.png)
### El siguiente paso es buscar el servidor que queremos, ponemos solo los que son gratis y elegimos **Ubuntu 20.04**
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/3.png)
### Vamos a hacer una lista de los siguientes pasos para la instalación.
* <span style="color:purple">**Paso 2**:</span> Dejamos la opción que viene por defecto:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/4.png)
* <span style="color:purple">**Paso 3**:</span> En la siguiente opción no cambiamos nada, le damos a next step
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/5.png)
* <span style="color:purple">**Paso 4**:</span> En este paso tenemos que cambiar la memoria viene por defecto 8GB y le ponemos **30gb** que es el máximo gratuito
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/6.png)
* <span style="color:purple">**Paso 5**:</span> En esta opción no cambiamos nada.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/7.png)
* <span style="color:purple">**Paso 6**:</span> En el paso 6 lo unico que modificamos es la descripción y le ponemos ssh.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/8.png)
* Para terminar pulsamos el botón:  
# <center> <img src="https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/9.png"></center>
* <span style="color:purple">**Paso 7**:</span> Nos sale un resumen de las opciones que hemos elegido, comprobamos que todo este bien y le damosa launch.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/10.png)
* Antes de empezar se abre un dialogo para crear las claves necesarias para conectarnos sin contraseña, podemos elegir una existente pero en este caso vamos a crear una y descargarla:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/11.png)
* Cuando la descargamos se nos activa el botón **Launch instances** y pulsamosen él. Ya nos aparece en la siguiente pantalla que nuestra instancia está iniciada.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/12.png)
### Para usar la instancia, entramos en https://console.aws.amazon.com en la parte de instancias y desde ahi podemos ver las que tenemos y realizar los cambios iniciarlas o finalizarlas.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/13.png)
### Vamos a explicar como conectar las Keys para que no nos pida contraseña
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/14.png)
* <span style="color:purple">**Conectar**:</span> al clicar la opción conectar nos salen unos comandos que tenemos que realizar en donde tengamos nuestra clave, hacemos gitBash en descargas que es donde ahora esta:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/15.png)
* <span style="color:purple">**Comandos**:</span> Copiamos los comandos que nos aparecen en la web y los ejecutamos:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/16.png)
* <span style="color:purple">**Ya nos hemos conectado!!**:</span> Después de ejecutar los comandos ya nos entra automáticamente en el servidor que hemos creado, con esto no nos pedirá la contraseña.  
# <center><img src="https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/17.png"></center>
- - -
# <center>INSTALACIÓN:</center> #
### Antes de instalar cada programa realizaremos el comando:  <center>**<span style="color:blue;background-color:yellow">sudo apt update</span>**</center>
## <center> Apache </center>
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/18.png)
> Para comprobar que funciona correctamente primero tenemos que cambiar algunas cosas desde aws y permitir que puedan entrar a páginas HTTP.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/28.png)
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/30.png)
> Cuando cambiamos la configuración podemos copiar la ip de nuestra máquina y ponerla en el navegador para ver si funciona.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/31.png)
## <center>MySql-Server:</center>
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/19.png)
### Configuramos MySql
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/20.png)
> Ponemos una contraseña y también elegimos el tipo de contraseña que debe ser baja media o fuerte.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/21.png)  
> Comprobamos que todo está correcto y escribimos exit.  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/22.png)  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/23.png)
## <center>PHP</center>
> Instalamos php y comprobamos que se ha instalado correctamente.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/24.png)
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/25.png)
## <center>FTP<center>
> Una vez instalado vemos si está activo
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/26.png)
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/27.png)
- - -
# <center>IP ELÁSTICA </center> #
## <center>¿Qué es y para que sirve?</center>
### Las direcciones IP elásticas son direcciones IPv4 estáticas diseñadas para la informática en la nube dinámica. Con una dirección IP elástica, puede enmascarar los errores de una instancia o software volviendo a mapear rápidamente la dirección a otra instancia de su cuenta. 
### Viene a ser lo mismo que una IP estática, la asignamos por comodidad para que no cambie cada vez y tengamos que cambiar todos los comandos cada dia.
> Vamos a la opción **direcciones IP elásticas** y clicamos en asignar dirección IP elástica.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/32.png)
> En la ventana que nos aparece no cambiamos ninguna opción y le damos a asignar.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/33.png)
> Nos sale un mensaje en que se ha asignado correctamente y le damos a **Asociar esta dirección IP elástica**
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/34.png)
> En las opciones elegimos la instancia a la que le queremos poner la IP y la dirección IP privada, en este caso la única que nos sale. Hemos marcado el check para volver a asociar una ip si lo necesitamos.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/35.png)
> Si todo ha ido bien nos saldrá este mensaje:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/36.png)
> Vamos a las instancias y comprobamos que nuestra instancia ahora tiene una IP elástica asociada, en nuestro caso es **52.22.108.16**
# <center><img src="https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/37.png"></center>
- - -
# <center> DNS </center> #

- ¿Qué es y para qué sirve el DNS?
    - <p style='text-align: justify;'>El DNS o Sistema de Nombres de Dominio pertenece a la familia de protocolos de Internet y sirve para resolver los nombres de dominio, es decir, para determinar la dirección IP del servidor donde está alojado el dominio al que queremos acceder.</p>

    - <p style='text-align: justify;'>Cada nombre de dominio usa DNS para controlar cómo encuentran tu sitio web los visitantes y cómo recibes correo electrónico. Puedes considerar al nombre de dominio como una dirección física y el DNS actúa como tu GPS.</p>

- Indica cuales son y para qué se usan los diferentes tipos de registros DNS.
Los tipos de registros más utilizados son: (12)

    - **A** = Dirección (address). Este registro se usa para traducir nombres de servidores de alojamiento a direcciones IPv4.

    - **AAAA** = Dirección (address). Este registro se usa en IPv6 para traducir nombres de hosts a direcciones IPv6.

    - **<p style='text-align: justify;'>TXT** = Puedes rellenarlos con cualquier texto que desees. Los usos más habituales de los registros TXT son verificar la propiedad del dominio y evitar el uso indebido del correo electrónico.</p>

    - **<p style='text-align: justify;'>CNAME** = Nombre canónico (canonical Name). Se usa para crear nombres de servidores de alojamiento adicionales, o alias, para los servidores de alojamiento de un dominio. Es usado cuando se están corriendo múltiples servicios (como FTP y servidor web) en un servidor con una sola dirección IP. Cada servicio tiene su propia entrada de DNS (como ftp.ejemplo.com. y www.ejemplo.com.). Esto también es usado cuando corres múltiples servidores HTTP, con diferentes nombres, sobre el mismo host. Se escribe primero el alias y luego el nombre real. Ej. Ejemplo1 IN CNAME ejemplo2</p>

    - **<p style='text-align: justify;'>NS** = Servidor de nombres (name server). Define la asociación que existe entre un nombre de dominio y los servidores de nombres que almacenan la información de dicho dominio. Cada dominio se puede asociar a una cantidad cualquiera de servidores de nombres.</p>

    - **<p style='text-align: justify;'>MX** = Intercambio de correo (mail exchange). Asocia un nombre de dominio a una lista de servidores de intercambio de correo para ese dominio. Tiene un balanceo de carga y prioridad para el uso de uno o más servicios de correo.<p>

    - **<p style='text-align: justify;'>PTR** = Indicador (pointer). También conocido como 'registro inverso', funciona a la inversa del registro A, traduciendo IPs en nombres de dominio. Se usa en el archivo de configuración de la zona DNS inversa.</p>

    - **<p style='text-align: justify;'>SOA** = Autoridad de la zona (start of authority). Proporciona información sobre el servidor DNS primario de la zona.</p>

    - **SRV** = Service record (SRV record).

    - **<p style='text-align: justify;'>ANY** = Toda la información de todos los tipos que exista. (No es un tipo de registro, sino un tipo de consulta)</p>
    - **<p style='text-align: justify;'>SPF**: o Convenio de Remitentes, del inglés Sender Policy Framework. Es una protección contra la falsificación de direcciones en el envío de correo electrónico. Identifica, a través de los registros de nombres de dominio (DNS), a los servidores de correo SMTP autorizados para el transporte de los mensajes.
    - **<p style='text-align: justify;'>CAA**: es un mecanismo de autorización para entidades certificadoras. Funciona de forma que únicamente la entidad que indiques en el registro CAA podrá emitir certificados para tu dominio o subdominio. Su uso tiene fines restrictivos.

- Imagen los registros DNS de tu sitio en Guebs y explicación de los registros de tu dominio grupo1.zerbitzaria.net.
    >Entramos en nuestro cPanel: http://cpanel.grupo1.zerbitzaria.net/ En la parte de dominios, Zone Editor.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/40.png)
    >Una vez ahí dentro en nuestra web clicamos en administrar.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/39.png)
    >Ahí podemos ver las DNS de nuestra página web: 
    - El primero es la dirección ip de nuestra web.
    - El segundo el correo electrónico.
    - El tercero puede usarse para evitar el uso indevido del correo electrónico.
    ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/38.png)
- - -
# <center> DNS </center> #

## 1. ¿Cuántos servidores DNS existen?
> En la actualidad existen un total de 13 servidores raíz DNS, y están nombrados por letras de la “A” a la “M”. Estos servidores, tienen una dirección IPv4 y una dirección IPv6.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/41.png)


## 2. ¿Cuántas redirecciones DNS son posibles?
>Una redirección ->www es una regla en tu servidor web que transmite todo el tráfico de la versión web sin www de tu dominio a la versión con www, o viceversa.
Este tipo de redirecciones se pueden realizar manualmente añadiendo un código como el siguiente en el archivo .htaccess:
RewriteEngine On RewriteCond %{HTTP_HOST} ^viejodominio.com$ [OR] RewriteCond %{HTTP_HOST} ^www.viejodominio.com$ RewriteRule (.*)$ http://www.nuevodominio.com/$1 [R=301,L]  
> Hay dos tipos de redirecciones:
- Opción 1: Redirección 301 Permanente que notificará al navegador del visitante para actualizar sus registros.
- Opción 2: Redirección 302 Temporal que no actualizará marcadores del visitante.

## 3. ¿Qué son los servidores DNS Raíz?
>Lo primero que debemos saber es que cuando intentamos acceder a un servicio online de cualquier índole (correo electrónico, sitio web, etc.) los servidores DNS que controlan todo, más conocidos como **Root Name Servers** o **DNS Root Servers**, son los que gestionan las peticiones de traducción de un nombre de dominio a una dirección IP. Sin estos servidores, los usuarios deberán recordar la IP de todos los sitios web. Su funcionamiento de forma muy resumida es el siguiente:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/42.png)

>El usuario introduce una dirección web en el navegador, el navegador consulta primero con el host del equipo, si no hay información, consulta con el servidor DNS que tiene especificado el equipo, si este no tiene información, va subiendo de servidor DNS a servidor DNS hasta llegar a los servidores Root, que son los principales y están en lo alto de la cadena de «mando».

## 4. ¿Para qué montar un servidor si simplemente escribiendo en un fichero la relación IP/Nombre el sistema ya funcionaría?
> Por que hay millones de IP y nombres web en el mundo, sería un caos si cada uno lo hace de una forma diferente. De esta manera centralizas la información, creas un protocolo para que todas las personas tengan que seguirlo y así sea global. Todo el mundo pueda acceder y crear webs con ese formato.

> Es más rapido y más sencillo para el usuario.

## 5. Según lo expuesto, y si en tu configuración de red del sistema operativo solamente posees un servidor DNS, entonces: ¿cuál sería el proceso para encontrar la IP de la dirección web: http://www.debian.org/distrib/netinst?
>Cuando se introduce la dirección de una página web (URL) en el campo de búsqueda del navegador, este realiza una petición al llamado resolver, un componente especial del sistema operativo cuya función consiste en almacenar en caché direcciones IP ya solicitadas anteriormente, y proporcionarlas cuando la aplicación cliente (navegador, programa de correo) la solicita. Si la dirección IP solicitada no se encuentra en el caché del resolver, este redirige la petición al servidor DNS que corresponda, que, en general, se trata del servidor DNS del proveedor de Internet. Aquí se coteja la petición con la base de datos del DNS y, si está disponible, se envía la dirección IP correspondiente como respuesta (“forward lookup”). Esta permite al navegador del usuario dirigirse al servidor web deseado en Internet. Otra vía alternativa consiste en el camino inverso, es decir, en traducir la dirección IP en la dirección de dominio (“reverse lookup”).  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/45.png)  
>Si un servidor DNS no puede responder a una petición con la información de que dispone en su base de datos, puede solicitar la información a otro servidor o reenviar la petición al servidor DNS que corresponda. Esta resolución se puede realizar de dos formas:

- **Resolución recursiva**: es la que se produce cuando el servidor DNS no puede responder por sí mismo a una petición y toma la información de otro servidor. El resolver transfiere la petición completa a su servidor DNS, que proporciona a su vez la respuesta al resolver con el nombre de dominio, si se ha resuelto.
- **Resolución iterativa**: cuando el servidor DNS no puede resolver la petición, envía como respuesta la dirección del siguiente servidor DNS de la jerarquía. El resolver tiene que enviar él mismo una nueva petición y repetir la maniobra hasta que se resuelve el nombre de dominio.
La administración centralizada de la información de los dominios en el DNS se caracteriza por un índice elevado de fiabilidad y flexibilidad. Si la dirección IP de un servidor cambia, el usuario no suele percibir nada, ya que la dirección IP actual para el dominio correspondiente se guarda en la base de datos.

## 6. ¿Es posible si dispones de una conexión a Internet con IP dinámica ofrecer servicios en Internet? Es decir, si quieres ofrecer los servicios SND, no dispones de IP estática, esto es, cada vez que te conectas a Internet tu IP, aunque a veces sea la misma, no siempre es la misma.
>Por lo general, se requiere una dirección IP estática para que siempre se pueda acceder a un ordenador, una red doméstica o una red de una pequeña empresa a través de Internet con el mismo nombre de host. Esto también es necesario si desea conectarse a su red doméstica a través de VPN, por ejemplo. Sin embargo, si su red doméstica o la red de su negocio está conectada a Internet a través de una conexión DSL, se asigna regularmente una nueva dirección IP dinámica a la red. Como resultado, el ordenador, la red doméstica o la red de la empresa no pueden ser alcanzados permanentemente utilizando la dirección IP.  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/44.png)  
>En este caso, puede utilizar el Sistema DNS Dinámico (Dynamic Domain Name System) para cambiar automáticamente las direcciones IP que cambian constantemente en el registro DNS del dominio, de modo que su red doméstica esté permanentemente accesible bajo su dominio.

>Para utilizar el DNS dinámico, puede utilizar el cliente multiplataforma de IONOS. Este cliente multiplataforma fue escrito en Python. 

## 7. ¿Qué es ICANN?
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/43.jpg)
>Internet Corporation for Assigned Names and Numbers (ICANN) es una organización sin fines de lucro que opera a nivel internacional, responsable de asignar espacio de direcciones numéricas de protocolo de Internet (IP), identificadores de protocolo y de las funciones de gestión [o administración] del sistema de nombres.
>ICANN es una organización que opera a nivel multinacional/internacional y es la responsable de asignar las direcciones del protocolo IP, de los identificadores de protocolo, de las funciones de gestión del sistema de dominio y de la administración del sistema de servidores raíz.









