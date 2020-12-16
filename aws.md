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
Los tipos de registros más utilizados son (10):

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








