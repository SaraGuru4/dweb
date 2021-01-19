# <center>APACHE 2 </center> #
### Ficheros de configuración y directivas en Linux
1. ¿Cuál es la ruta a los ficheros de configuración de apache?
    * /etc/apache2
2. ¿Cuál es el fichero de configuración principal?
    * httpd.conf: Archivo de configuración principal del servidor HTTP Apache.
3. ¿Que son las directivas "include" que aparecen en el fichero de configuración
principal?
    * Include permite que se incluyan otros archivos de configuración en el tiempo de ejecución. La ruta a estos archivos de configuración pueden ser absolutas o relativas con respecto al ServerRoot.
4. ¿Que contiene el fichero ports.conf?
    * El archivo de configuración /etc/apache2/ports.conf almacena las directivas que determinan los puertos TCP en los que está escuchando Apache. Aquí está el contenido predeterminado de este archivo en Ubuntu:
    ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/56.png)
    * La directiva Listen determina el puerto al que se enlazará Apache. Por defecto, este es el puerto 80 . Puede cambiar este valor al puerto de su elección. Solo asegúrese de reiniciar Apache (reinicio del servicio sudo apache2 ) para aplicar los cambios.
5. ¿Que contiene el fichero envvars?
    * Las variables de entorno de Apache2 se establecen en el archivo / etc / apache2 / envvars . Estas variables no son las mismas que las variables de entorno de su sistema Linux; se almacenan y manipulan en una estructura interna de Apache.
        ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/57.png)
    * El archivo / etc / apache2 / envvars contiene definiciones de variables como APACHE_LOG_DIR (la ubicación de los archivos de registro de Apache), APACHE_PID_FILE (el ID del proceso de Apache), APACHE_RUN_USERS (el usuario que ejecuta Apache, por defecto www-data ), etc.

    * Puede abrir y modificar este archivo en un editor de texto de su elección:
6. ¿Cuál es el uso de las carpetas "sites-avaliable" y "sites-enabled"'?
    * De forma predeterminada en los sistemas Ubuntu, los archivos de configuración de Apache Virtual Hosts se almacenan en / etc / apache2 / sites - directorio disponible y se pueden habilitar creando enlaces simbólicos al directorio / etc / apache2 / sites - habilitado . ServerName: el dominio que debe coincidir con esta configuración de host virtual.
    * Con avaliable tienes las paginas posibles y con enabled habilitas una pagina.
### Define para que se utilizan las siguientes :
* ServerRoot:
    * La directriz ServerRoot especifica el directorio de nivel superior que tiene el contenido web. Por defecto, ServerRoot está configurado a "/etc/httpd" para servidores seguros y no seguros.
* ServerAdmin:
    * Configure la directriz ServerAdmin a la dirección de correo electrónico del administrador del servidor Web. Esta dirección de correo aparecerá en los mensajes de error en las páginas generadas por el servidor Web, de tal manera que los usuarios pueden comunicar errores enviando correo al administrador. Por defecto, ServerAdmin es configurado a root@localhost. Una forma típica de configurar ServerAdmin es configurarlo en a webmaster@ejemplo.com. Una vez configurado, cree un alias del webmaster para la persona responsable del servidor Web en /etc/aliases y ejecute /usr/bin/newaliases.
* ServerName:
    * Use la directriz ServerName para configurar un nombre de servidor y un número de puerto (que coincida con la directriz Listen) para el servidor. El ServerName no necesita coincidir con el nombre real de la máquina. Por ejemplo, el servidor Web puede ser www.example.com pero el nombre del servidor es en realidad foo.example.com. El valor especificado en ServerName debe ser un nombre del Servicio de Nombres de Dominio (Domain Name Service, DNS)válido que pueda ser resuelto por el sistema — no invente algo. Lo siguiente es una directriz ServerName de ejemplo:
        * ServerName www.example.com:80

    * Cuando especifique un ServerName, asegúrese de que el par de la dirección IP y el nombre del servidor esten incluidos en el archivo /etc/hosts.
* ServerAlias:
    * Descripción:	Nombres alternativos para un host que se utilizan al hacer coincidir solicitudes con hosts virtuales de nombres
    * Sintaxis:	ServerAlias hostname [hostname] ...
    * Contexto:	anfitrión virtual
    * Estado:	Núcleo
    * Módulo:	núcleo
    * La ServerAlias directiva establece los nombres alternativos para un host, para su uso con hosts virtuales basados ​​en nombres . El ServerAliaspuede incluir comodines, si es apropiado.

       ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/58.png)
* User:
    * La directriz User establece el nombre de usuario para el proceso del servidor y determina qué archivos pueden acceder al servidor. Cualquier archivo que no esté accesible a este usuario tampoco estará disponible para los clientes conectándose al Servidor Apache HTTP. Por defecto User es configurado a apache. Esta directriz se ha desaprobado para la configuración de hosts virtuales.
* Include: 
    * Include permite que se incluyan otros archivos de configuración en el tiempo de ejecución. La ruta a estos archivos de configuración pueden ser absolutas o relativas con respecto al ServerRoot.
* Group:
    * Especifica el nombre del grupo de los procesos Servidor Apache HTTP. Esta directriz se ha desaprobado para la configuración de hosts virtuales. Por defecto, Group está configurado a apache.
* KeepAlive:
    * KeepAlive determina si el servidor permitirá más de una petición por conexión y se puede usar para prevenir a un cliente consumir demasiados recursos del servidor.
    Por defecto Keepalive está configurado a off. Si Keepalive está en on y el servidor se vuelve muy ocupado, este puede rápidamente generar el máximo número de procesos hijos. En esta situación, el servidor se volverá significativamente lento. Si se activa Keepalive, es una buena idea configurar el KeepAliveTimeout a un valor bajo (consulte la Sección 10.5.7 para más información sobre la directriz KeepAliveTimeout) y controle el archivo de registro /var/log/httpd/error_log en el servidor. Este registro informa cuando el servidor se esta quedando corto de procesos hijos.
* Files:
    * La directiva Files limita el ámbito de aplicación de las directivas que incluye según el nombre de los ficheros. Es comparable a Directory y Location. Debe cerrarse con Files. Las directivas usadas en esta sección se aplicarán a cualquier objeto con un nombre base (último componente del nombre de fichero) que coincida con el nombre de fichero especificado. Las secciones Files se procesan en el orden en que aparecen en el fichero de configuración, después de las secciones Directory y de leer los ficheros .htaccess, pero antes de las secciones Location. Tenga en cuenta que las directivas Files pueden anidarse dentro de las secciones Directory para restringir la parte del sistema de ficheros a la que se aplican.

    * El argumento filename puede incluir un nombre de fichero, o una cadena de carácteres comodín, donde ? equivale a cualquier carácter individual, y * equivale a cualquier secuencia de caracteres. También pueden usarse expresiones regulares extendidas, con la ventaja de que tambien se puede usar el carácter ~. Por ejemplo:

        * <Files ~ "\.(gif|jpe?g|png)$">

    * Equivaldría a la mayoría de los formatos gráficos de Internet. No obstante, es mejor usar <FilesMatch>.
* Location:
    * Las etiquetas <Location> y </Location> permiten crear un contenedor en el cual se puede especificar el control de acceso basado en URL. Por ejemplo, para permitir a personas conectarse desde dentro del dominio del servidor para ver informes de estado, utilice las directrices siguientes:
    ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/59.png)
    * Reemplace <.example.com> con el nombre de dominio de segundo nivel para el servidor Web.
* Errorlog:
    * ErrorLog especifica el archivo donde se guardan los errores del servidor . Por defecto, esta directriz es configurada a /var/log/httpd/error_log.
* Listen:
    * El comando Listen identifica los puertos en los que el servidor Web aceptará las peticiones entrantes. Por defecto, el Servidor Apache HTTP está configurado para escuchar en el puerto 80 para comunicaciones Web no seguras y (en el archivo /etc/httpd/conf.d/ssl.conf el cual define cualquier servidor seguro) en el puerto 443 para comunicaciones seguras.

    * Si el Servidor Apache HTTP está configurado para escuchar en un puerto por debajo del 1024, se necesita al usuario root para iniciarlo. Para los puertos 1024 y superiores, httpd puede ser arrancado por cualquier usuario.

    * La directriz Listen también se puede usar para especificar direcciones IP particulares sobre las cuales el servidor aceptará conexiones.
* Alias:
    * El valor Alias hace accesibles a los directorios fuera del directorio DocumentRoot. Cualquier URL que termine en el alias será automáticamente traducido a la ruta del alias. Por defecto, ya existe un alias configurado para un directorio icons. El servidor web puede acceder al directorio icons, pero el directorio no está en el DocumentRoot.
* Redirect:
    * Cuando se mueve una página web, se puede utilizar Redirect para crear asignaciones de la ubicación del archivo a un nuevo URL. El formato es como sigue:

        ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/60.png)
    * En este ejemplo, sustituya <old-path> con la vieja información de la ruta por <file-name> y <current-domain> y <current-path> con el dominio actual y la información de la ruta para <file-name>.

    * En este ejemplo, cualquier petición <file-name> en la vieja ubicación será redirigida automáticamente a la nueva ubicación.

    * Para técnicas más avanzadas de redireccionamiento, use el módulo mod_rewrite incluido con el Servidor Apache HTTP. Para más información sobre la configuración del módulo mod_rewrite, refiérase a la documentación de la Apache Software Foundation en http://httpd.apache.org/docs-2.0/mod/mod_rewrite.html.
* ErrorDocumetn 404:
    * La directriz ErrorDocument asocia un código de respuesta HTTP con un mensaje o un URL para que sea devuelto al cliente. Por defecto, el servidor Web produce una salida simple de mensaje de error cuando ocurre alguno. La directriz ErrorDocument obliga a que el servidor Web envie una salida de mensaje personalizado o página. 
    * En este caso el 404 es not found, osea no encontrada la página web.
* Options:
    * La directriz Options controla cuáles características del servidor están disponibles en un directorio en particular. Por ejemplo, en los parámetros restrictivos especificados para el directorio raíz, Options sólo permite FollowSymLinks. No hay características activadas, salvo que el servidor puede seguir enlaces simbólicos en el directorio raíz.

    * Por defecto, en el directorio DocumentRoot, Options se configura para incluir Indexes y FollowSymLinks. Indexes permite al servidor generar un listado de un directorio si no se especifica el DirectoryIndex (por ejemplo, index.html). FollowSymLinks permite al servidor seguir enlaces simbólicos en ese directorio.
* Etiqueta: "Virtualhost": 
    * Las etiquetas VirtualHost y /VirtualHost crean un contenedor mostrando las características de un host virtual. El contenedor VirtualHost acepta la mayoría de las directrices de configuración.

    * Se proporciona un contenedor VirtualHost en comentarios en httpd.conf, el cual ilustra el mínimo conjunto de directrices de configuración necesarias para cada host virtual. Refiérase a la Sección 10.8 para más información sobre los host virtuales.
* Etiqueta: "Directory":
    * Las etiquetas Directory /path/to/directory y /Directory. se usan para crear un contenedor que se utiliza para cercar un grupo de directrices de configuración que sólo se aplican a un directorio y sus subdirectorios específicos. Cualquier directriz aplicable a un directorio puede usarse en las etiquetas Directory.

    * Por defecto, se aplican parámetros muy restrictivos al directorio raíz (/), utilizando las directrices Options (consulte la Sección 10.5.23) y AllowOverride (vea la Sección 10.5.24). Con esta configuración, cualquier directorio del sistema que necesite valores más permisivos ha de ser configurado explícitamente con esos valores.

    * En la configuración por defecto, otro contenedor Directory es configurado para el DocumentRoot el cual asigna parámetros menos rígidos al árbol del directorio para que el Servidor Apache HTTP pueda acceder a los archivos que residan allí.

    * El contenedor Directory también se puede usar para configurar directorios adicionales cgi-bin para las aplicaciones del servidor fuera del directorio especificado en la directriz ScriptAlias (consulte a la Sección 10.5.41 para más información).

    * Para lograr esto, el contenedor Directory debe configurar la opción ExecCGI para ese directorio.

    * Por ejemplo, si los scripts CGI están localizados en /home/my_cgi_directory, añada el contenedor siguiente Directory al archivo httpd.conf:

        ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/61.png)

    * Luego, necesitará anular el comentario de la directriz AddHandler para identificar archivos con la extensión .cgi como scripts CGI. Consulte la Sección 10.5.56 para saber cómo configurar el AddHandler.

    * Para que esto funcione, los permisos para los scripts CGI y la ruta completa a los scripts, se deben colocar a 0755.
* DocumentRoot:
    * DocumentRoot es el directorio que contiene la mayoría de los archivos HTML que se entregarán en respuesta a peticiones. El directorio predeterminado DocumentRoot para servidores web seguros y no seguros es /var/www/html. Por ejemplo, el servidor puede recibir una petición para el siguiente documento:

        * http://example.com/foo.html

    * El servidor busca por el archivo siguiente en el directorio por defecto:

        * /var/www/html/foo.html
    * Si se quiere cambiar DocumentRoot para que no lo compartan los servidores web seguros y no seguros, vea la Sección 10.8.
* DirectoryIndex:
    * DirectoryIndex es la página por defecto que entrega el servidor cuando hay una petición de índice de un directorio especificado con una barra (/) al final del nombre del directorio. Cuando un usuario pide la página http://ejemplo/este_directorio/, recibe la página del índice del directorio, DirectoryIndex, si existe, o un listado de directorios generado por el servidor. El valor por defecto para DirectoryIndex es index.html y el tipo de mapa index.html.var. El servidor intentará encontrar cualquiera de estos archivos y entregará el primero que encuentre. Si no encuentra ninguno de estos archivos y Options Indexes esta configurado para ese directorio, el servidor genera y devuelve una lista, en formato HTML, de los subdirectorios y archivos dentro del directorio, a menos que la característica de listar directorios esté desactivada.