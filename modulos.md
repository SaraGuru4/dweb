# <center>APACHE 2 </center> #
## Indica qué módulos estáticos hay activos en tu instancia de AWS y qué hace cada una de ellas:
### <center>**<span style="color:blue;background-color:yellow">apache2ctl -l</span>**</center>

# <center>![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/62.png)</center>

  - **core.c**: Esta directiva controla si las peticiones que contienen información de path añadida a continuación de un nombre de fichero existente serán aceptadas o rechazadas. La información de path añadida puede pasarse a los scripts en la variable de entorno PATH_INFO.Por ejemplo, suponga que la ubicación /test/ se refiere a un directorio que contiene un único fichero: here.html. Entonces, tanto las peticiones a /test/here.html/more como las peticiones a /test/nothere.html/more toman /more como PATH_INFO.

  - **mod_so.c**: Carga los demas modulos en el inicio y parada del servidor.

  - **mod_watchdog.c**: Proporciona infraestructura para que otros módulos ejecuten tareas periódicamente.

  - **http_core.c**: Carga el protocolo https.

  - **mod_log_config.c**: Con este módulo puede configurar el aspecto de los archivos de registro de Apache. Este módulo está habilitado por defecto.

  - **mod_logio.c**: Registro del número de bytes recibidos y enviados en cada respuesta.

  - **mod_version.c**: Configuración dependiente de la versión. Este módulo está diseñado para su uso en suites de prueba y grandes redes que tienen que lidiar con diferentes versiones de httpd y diferentes configuraciones. Proporciona un nuevo contenedor *IfVersion*, que permite una verificación de versión flexible que incluye comparaciones numéricas y expresiones regulares.

  - **mod_unixd.c**: Directorio para que apache ejecute chroot (8) después del inicio. Esta directiva le dice al servidor que haga chroot (8) al directorio especificado después del inicio, pero antes de aceptar solicitudes a través de 'net.

## Activar módulos:
### 1. Comprueba si los módulos info y status están activos en tu instancia.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/63.png)

    - El módulo status si está activo.

    - El módulo info no.
### 2. Activa el módulo que no esté activo y compruébalo
> Entramos en: /etc/apache2/mods-available
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/64.png) 
>Buscamos el módulo que queremos activar. En este caso  *mod_info*.
>El archivo tiene dentro la siguiente información:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/65.png) 
>Escribimos:
### <center>**<span style="color:blue;background-color:yellow">sudo a2enmod info</span>**</center> 

>Reinciamos apache2 y ya tenemos activo el mod info
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/66.png)
>Lo comprobamos:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/67.png)
>Ahora ya hemos activado el mod info.
