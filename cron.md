- - -
# <center>CRON</center> #
# **6. CRONTAB**
## **¿Qué es CRON?**
### Cron es un administrador de tareas de Linux que permite ejecutar comandos en un momento determinado, por ejemplo, cada minuto, día, semana o mes. Si queremos trabajar con cron, podemos hacerlo a través del comando crontab.
## **¿Qué es CRONTAB?**
###  Es un archivo de texto donde se listan todas las tareas que deben ejecutarse y el momento en el que deben hacerlo.
## **¿Qué hace cada línea de cron?**
- <span style="color:YELLOW">30 * * * * /home/prueba.sh</span>
### Se ejecutara el script a todas las horas y 30 minutos: por ejemplo a la 1:30, 2:30 etc de cada hora, cada dia, cada mes, todos los dias de la semana. 
- <span style="color:YELLOW">30 20 * * * /home/prueba.sh</span>
### Se ejecutara el script a las 8 y 30 minutos, cada dia, cada mes, todos los dias de la semana.
- <span style="color:YELLOW">30 20 * * 1-5 /home/prueba.sh</span>
### Se ejecutara el script a las 8 y 30 minutos, cada dia, cada mes, de lunes a viernes. 
- <span style="color:YELLOW">30 20 * * 2,4 /home/prueba.sh</span>
### Se ejecutara el script a las 8 y 30 minutos, cada dia,cada mes, los martes y los jueves.
- <span style="color:YELLOW">30 20 10,20 * * /home/prueba.sh</span>
### Se ejecutara el script a las 8 y 30 minutos, el dia 10 y 20 de cada mes, cualquier dia de la semana.
- <span style="color:YELLOW">*/15 * * * * /home/prueba.sh</span>
### Se ejecutara el script cada 15 minutos todas las horas, todos los dias del mes, todos los meses y todos los dias de la semana.
- <span style="color:YELLOW">@daily /home/prueba.sh </span>
### Se ejecutara el script una vez al dia.
- <span style="color:YELLOW">@montly /etc/backup.sh </span>
### Se ejecutara el script una vez al mes.
- <span style="color:YELLOW">30 20 * * Mon-Fri /etc/test.sh</span>
### Se ejecutara el script a las 8 y 30 minutos, cada dia, cada mes, de lunes a viernes. 
- <span style="color:YELLOW">1 0 1-7 * * [ "$(date '+%a')" = "Fri" ] && /etc/backup.sh</span>
### Se ejecutara el script a las 12 y 01 minutos, del dia 1 al 7, cada mes, solo los viernes.
- - -
# **7.CREAR UN SCRIPT Y QUE SE EJECUTE**
### Primero  elegimos el editor para el crontab
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/50.png)
### Editamos el crontab con **crontab -e** y le introducimos la línea de hora y fecha deseadas y el archivo donde vamos a guardar el sript.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/51.png)
### Escribimos en sript.sh la linea que queremos que ejecute.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/52.png)
### Con el comando cat texto.txt veremos el resultado del script
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/53.png)
- - -
# **8.Crear un cron para que haga una copia (en un fichero comprimido) de la carpeta /home/ubuntu en la carpeta /copias cada 15 minutos los martes.**
### Escribimos el siguiente comando en crontab -e y nos realizará la copia que necesitamos comprimida:
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/54.png)
### Comprobamos que la ha realizado correctamente.
![Sin titulo](https://raw.githubusercontent.com/SaraGuru4/dweb/main/fotos/55.png)

