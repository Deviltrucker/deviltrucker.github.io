TestComandosLinux1
1.1 Usando el comando find.
Busca todos los ficheros del directorio / que no pertenezcan a ningún usuario
* find / -nouser 
1.2 NOTA: Para estos ejercicios tienes que crear un directorio en tu home llamado PRUEBAS y copiar la carpeta Textos en él.
Usando ls y grep.
Listar todos los archivos del directorio PRUEBAS/Textos que tengan extensión .txt.
* ls PRUEBAS/Textos | grep .txt 
1.3 Usando el comando find.
Buscar los ficheros del directorio /etc que no pertenezcan al usuario root
*  find /etc -type f -not -user root 
1.4 Utilizando expresiones regulares buscar todos los ficheros del directorio /usr que tengan extensión txt o lst 
* find /usr -regextype posix-egrep -regex '. (txt|lst)$' 
1.5 Usando el comando find.
Busca todos los subdirectorios del directorio /etc/security que estén vacíos
* find /etc/security -type d -empty 
1.6 Usando grep.
Mostrar las líneas, del archivo LosDosConejos.txt, que empiecen por L (mayúscula o minúscula)
* grep -i "^l" PRUEBAS/Textos/LosDosConejos.txt 
1.7 Usando grep y wc.
Contar las líneas, que han salido en el ejemplo anterior
* grep -i "^l" PRUEBAS/Textos/LosDosConejos.txt | wc -l 
1.8 Usando grep.
Visualiza las líneas del fichero PRUEBAS/Textos/ElPerroDeParra.txt que contiene la palabra “Parra” o “perro”
* grep -E ‘Parra|perro’ PRUEBAS/Textos/ElPerroDeParra.txt 
1.9 Utilizando el comando find.
Busca todos los ficheros del directorio /etc/ que estén vacíos
* find /etc/ -type f -empty 
1.10 Usando grep.
Visualice las líneas del archivo PRUEBAS/Textos/ElPerroDeParra.txt que no contengan la cadena de caracteres "Parra"
* grep -v Parra PRUEBAS/Textos/ElPerroDeParra.txt 

1.11 Usando el comando find.
Busca los ficheros del directorio /etc/apt con más de 30 días desde su última modificación.
* find /etc/apt -type f -mtime +30 
1.12 Usando cat y grep.
Visualice las líneas del archivo /etc/passwd que no contengan la cadena de caracteres "home"
* cat /etc/passwd | grep -v home 
TestComandosLinux2
2. 1 Usando el comando find, borra los ficheros del directorio PRUEBAS/ y subdirectorios cuyo nombre contenga la cadena “Borrar” 

* find PRUEBAS -name ' Borrar_ ' -exec rm '{}' \; 

2.2 Busca los ficheros del directorio /usr/share/icons/ que sean más grandes en tamaño de 1 Megabyte
* find /usr/share/icons/ -type f -mtime +30 -size +1M 

2.3 Usando grep.
Visualice las líneas del fichero PRUEBAS/Textos/ LosDosConejos.txt que empiecen con “P” o con “D”
* grep -E '^P|D' PRUEBAS/Textos/LosDosConejos.txt 

2.4 Usando grep
Visualice las líneas del archivo PRUEBAS/Textos/LosDosConejos.txt que contengan la
cadena de caracteres "”Sí”"
* grep “”Sí”” PRUEBAS/Textos/LosDosConejos.txt 

2.5 Busca los ficheros del directorio /etc/libreoffice que no hayan sido accedidos desde hace dos días 
* find /etc/libreoffice -atime +2 

2.6 Usando el comando find, copia los ficheros del directorio PRUEBAS/ y subdirectorios cuya extensión sea .txt en el directorio PRUEBAS/Textos/Borrar/ 

* find PRUEBAS -name ' .txt' -exec cp '{}' PRUEBAS/Textos/Borrar/ \; 

2.7 Usando grep.
Visualice las líneas del fichero PRUEBAS/Textos/ LosDosConejos.txt que contengan
la cadena de caracteres “perro” o “Perro”

* grep -i perro PRUEBAS/Textos/ LosDosConejos.txt 

2.8 Busca los ficheros del directorio /usr cuya última modificación haya sido entre 2 y 10 días 

* find /usr -mtime +2 -mtime -10 

2.9 Usando grep.
Visualice los nombres de los ficheros del directorio PRUEBAS/Textos que contengan la cadena de caracteres “perro” o “Perro”
* grep -li perro PRUEBAS/Textos/ 

2.10 Busca todos los ficheros del directorio /boot y subdirectorios sólo de nivel 1, con extensión .lst 

* find /boot -maxdepth 1 -name .lst 

2.11 Busca todos los subdirectorios de nivel 1 del directorio /etc que estén vacíos 

* find /etc maxdepth 1 -type d -empty 


2.12 Usando grep.
Visualice las líneas del fichero PRUEBAS/Textos/ElPerroDeParra.txt que empiecen con un guión (“-“)
* grep ^- PRUEBAS/Textos/ElPerroDeParra.txt 

TestComandosLinux3
3.1 Usando grep.
Número de veces que el fichero PRUEBAS/Textos/ElPerroDeParra.txt contiene la palabra “parra”
* grep -c parra PRUEBAS/Textos/ElPerroDeParra.txt 
3.2 Usando grep.
Número de veces que están las cadenas podencos y galgos en el fichero PRUEBAS/Textos/ LosDosConejos.txt
* grep -Ec 'podencos|galgos' PRUEBAS/Textos/LosDosConejos.txt 
3.3 Utilizando el comando find.
Buscar un fichero con el nombre y la extensión: gfxblacklist.txt
* find / -name gfxblacklist.txt 
3.4 Usando ls y grep
Listar todos los archivos del directorio actual y subdirectorios que sean del tipo .txt
* ls –lR | grep .txt 
3.5 Utilizando el comando find.
Buscar el fichero gfxblacklist.txt indicando que sólo busque en el directorio /boot y subdirectorios:
* find /boot -name gfxblacklist.txt 
3.6 Usando ls y grep.
Listar todos los archivos del directorio actual que sean del tipo .jpg o Jpg o JPG o jPG, etc. (que la búsqueda sea indiferente a MAY. o min.)
* ls | grep -i .jpg 
3.7 Utilizando el comando find.
Busca todos los ficheros del directorio /boot y subdirectorios, con extensión .lst:
* find /boot -name .lst 


3.8 Utilizando el comando find.
Buscar el fichero gfxblacklist.txt ignorando mayúsculas y minúsculas
* find / -iname gfxblacklist.txt 
3.9 Usando ls y grep.
Listar todos los archivos del directorio /dev que empiecen por tty y acaben en 1,2,3 ó 4.
* ls /dev/ | grep ^tty | grep [1-4]$ 
3.10 Utilizando el comando find.
Buscar todos los ficheros del directorio /usr que empiecen con por “a”, “b” o “c” y con extensión.txt
* find /usr -type f -name "[a-c] .txt" 
3.11 Visualice todas las líneas del archivo /etc/services que contengan la cadena de caracteres "http". 
* grep http/etc/services 
3.12 Utilizando el comando find.
Buscar directorios con el nombre python3
* find / type -d -name python3 

TestComandosLinux4

4.1 Utilizando el comando find.
Busca todos los ficheros ocultos del directorio /boot y subdirectorios
* find /boot -type f -name ". " 

4.2 Busca todos los ficheros del directorio /usr y de sus subdirectorios hasta los de nivel 2  que estén vacíos 
* find /usr maxdepth 2 -type f -empty

