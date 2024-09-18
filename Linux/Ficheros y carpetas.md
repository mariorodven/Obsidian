---
dg-publish: "true"
---
Antes, explicando los comandos de [[¿Qué es Linux?#^La terminal]], he mencionado la palabra carpeta, pero esa palabra es muy de Windows, aquí se les llama directorios, en Linux el 99% de todo, es o un fichero o un directorio. 

```zsh
[mario@archVictus carpeta]$ ls -l
total 4
drwxr-xr-x 2 mario mario 4096 Sep 10 19:35 carpeta
-rw-r--r-- 1 mario mario    0 Sep 10 19:35 codigo.c
-rw-r--r-- 1 mario mario    0 Sep 10 19:35 codigo.py
-rw-r--r-- 1 mario mario    0 Sep 10 19:35 fichero.txt
```

Aquí usamos el comando `ls -l` que nos muestra el contenido del directorio actual y qué es cada cosa, ademas de mas información que actualmente no es relevante como el propietario del archivo, permisos o tamaño. Como veis, carpeta es, efectivamente, una carpeta, lo vemos en la primera letra de la primera columna, que nos pone una d de directory. En el resto de archivos vemos que no está la d, dado que no está, sabemos que son ficheros. Antes de pasar a algo mas interesante os recomiendo ver qué es una [[carpeta padre]]

Linux es una carpeta muy grande, el root (comúnmente escrito como `/`), todo esto lo explico mejor en[[Sistema de Archivos de Linux]].

