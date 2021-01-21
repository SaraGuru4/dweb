- - -
# <center>VIRTUAL HOST </center> #
## Para cambiar la configuración del Host de Apache2 tenemos que entrar en la siguiente ruta y modificar el archivo apache2.conf
### <center>**<span style="color:blue;background-color:yellow">/etc/apache2/apache2.conf</span>**</center>

# <center>![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/68.png)</center>
# www.apuntes.daw.net:80

- Configuración mediante fichero .htaccess.
>Antes:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/69.png)  
>Despues:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/70.png)
- Alojado en: /var/www/apuntes/.
>Escribimos:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/71.png)
- Sin Fichero index.
>Escribimos:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/72.png)
- Permitir mostrar índice de ficheros.
>Antes:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/73.png)  
>Despues:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/74.png)
- Pagina de error 404: /var/www/404.html.
>Escribimos:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/75.png)
- Redirigir www.apuntes.daw.net/buscador/ a www.google.es.
>Primero tenemos que habilitarlo:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/76.png)  
>Después escribir la redirección:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/77.png)
- Ficheros log: apuntes.error.log y apuntes.access.log  
>![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/78.png)


- - -
# www.daw.net:443
- Alojado en: /var/www/daw/seguro/
>Escribimos:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/80.png)
- Crear y utilizar el certificado daw.crt y la firma daw.key
> ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/85.png)
- Fichero index: inicio.html.
>Escribimos:  
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/81.png)
- No permitir mostrar índice de ficheros.
>![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/82.png)
- Pagina de error 404: /var/www/404.html
> ![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/83.png)
- Ficheros log: daw.ssl.error.log y daw.ssl.access.log
>![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/79.png)
- Autenticación de usuarios "Basic” con fichero de usuarios permitidos en
/var/www/acceso.basic.daw
>![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/84.png)