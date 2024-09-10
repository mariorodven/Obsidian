Aquí os dejo una lista con los comandos que creo esenciales para moverse por la terminal de Linux, están organizados de forma que muestra el uso, las banderas de uso común y un ejemplo.

Los **comandos de Linux** permiten a los usuarios interactuar con el sistema operativo, pero estos comandos no operan directamente sobre el **hardware**. En su lugar, los comandos **se comunican con el [[kernel]]**, que es el núcleo del sistema operativo.

El **kernel** es responsable de gestionar los recursos del sistema (como la memoria, la CPU y los dispositivos de hardware). Cuando un usuario ejecuta un comando, por ejemplo `ls` para listar archivos, ese comando **envía una solicitud al kernel** a través del **shell** (la interfaz de comandos). El kernel interpreta esa solicitud y accede al hardware o sistema de archivos, devolviendo los resultados al usuario.

En resumen, los comandos de Linux son como instrucciones que, a través del kernel, permiten controlar y usar el hardware y recursos del sistema.
### 1. **cd** (Cambiar directorio)

- **Uso**: Navega entre directorios.
- **Ejemplo**:
    - `cd /home/usuario`: Cambia al directorio `/home/usuario`.
    - `cd ..`: Sube un nivel en la jerarquía de carpetas.

### 2. **cp** (Copiar archivos)

- **Uso**: Copia archivos o directorios.
- **Banderas comunes**:
    - `-r`: Copia recursivamente un directorio.
    - `-v`: Modo verboso, muestra qué se está copiando.
- **Ejemplo**:
    - `cp archivo.txt /ruta/destino`: Copia un archivo.
    - `cp -r carpeta/ /ruta/destino/`: Copia una carpeta.

### 3. **mkdir** (Crear directorio)

^379a45

- **Uso**: Crea uno o varios directorios.
- **Banderas comunes**:
    - `-p`: Crea directorios de manera recursiva.
- **Ejemplo**:
    - `mkdir nueva_carpeta`: Crea una carpeta. ^5c53e8
    - `mkdir -p /ruta/subcarpeta`: Crea una subcarpeta dentro de una ruta.

### 4. **touch** (Crear archivo vacío o actualizar timestamp)

- **Uso**: Crea un archivo vacío o actualiza la fecha de modificación de uno existente.
- **Ejemplo**:
    - `touch archivo.txt`: Crea un archivo vacío llamado `archivo.txt`.

### 5. **rmdir** (Eliminar directorios vacíos)

- **Uso**: Elimina solo directorios vacíos.
- **Ejemplo**:
    - `rmdir carpeta_vacía`: Elimina una carpeta vacía.

### 6. **rm** (Eliminar archivos o directorios)

- **Uso**: Elimina archivos o directorios.
- **Banderas comunes**:
    - `-r`: Elimina recursivamente (para directorios).
    - `-f`: Fuerza la eliminación sin confirmación.
- **Ejemplo**:
    - `rm archivo.txt`: Elimina un archivo.
    - `rm -rf carpeta/`: Elimina una carpeta y su contenido.

### 7. **chmod** (Cambiar permisos de archivos o directorios)

- **Uso**: Cambia los permisos de un archivo o directorio.
- **Banderas comunes**:
    - `+x`: Añade permiso de ejecución.
    - `u`, `g`, `o`: Modifica permisos para usuario (u), grupo (g) o otros (o).
- **Ejemplo**:
    - `chmod +x script.sh`: Da permisos de ejecución al archivo.
    - `chmod 755 archivo.txt`: Permisos de lectura, escritura y ejecución para el usuario, lectura y ejecución para grupo y otros.

### 8. **chown** (Cambiar propietario de archivos o directorios)

- **Uso**: Cambia el propietario de un archivo o directorio.
- **Ejemplo**:
    - `chown usuario:grupo archivo.txt`: Cambia el propietario y grupo de un archivo.

### 9. **tree** (Mostrar estructura de directorios en forma de árbol)

- **Uso**: Muestra los directorios y archivos en formato de árbol.
- **Banderas comunes**:
    - `-L N`: Limita el nivel de profundidad del árbol.
- **Ejemplo**:
    - `tree`: Muestra la estructura completa del directorio actual.
    - `tree -L 2`: Muestra dos niveles de profundidad.

### 10. **ls** (Listar archivos y directorios)

- **Uso**: Muestra el contenido de un directorio.
- **Banderas comunes**:
    - `-l`: Muestra detalles adicionales como permisos, tamaño, fechas.
    - `-a`: Muestra archivos ocultos.
    - `-h`: Muestra tamaños en formato legible (KB, MB).
- **Ejemplo**:
    - `ls -la`: Lista todo, incluyendo archivos ocultos, con detalles.

### 11. **less** (Ver archivos grandes página por página)

- **Uso**: Permite visualizar el contenido de un archivo de manera interactiva.
- **Ejemplo**:
    - `less archivo.txt`: Abre el archivo para leerlo con paginación.

### 12. **tail** (Mostrar las últimas líneas de un archivo)

- **Uso**: Muestra las últimas líneas de un archivo.
- **Banderas comunes**:
    - `-n N`: Muestra las últimas N líneas.
    - `-f`: Muestra nuevas líneas a medida que se agregan (útil para logs).
- **Ejemplo**:
    - `tail -n 20 archivo.txt`: Muestra las últimas 20 líneas de un archivo.

### 13. **cat** (Concatenar y mostrar archivos)

- **Uso**: Muestra el contenido de un archivo en la terminal.
- **Ejemplo**:
    - `cat archivo.txt`: Muestra el contenido del archivo.

### 14. **man** (Manual de comandos)

- **Uso**: Muestra el manual de un comando, explicando cómo usarlo y sus opciones.
- **Ejemplo**:
    - `man ls`: Muestra la documentación del comando `ls`.

Los **comandos de Linux** son en su mayoría consistentes entre las distintas **[[distros|distribuciones]] (distros)** de Linux, ya que todas las distros comparten el mismo **kernel de Linux** y muchos de los mismos programas y herramientas fundamentales. Sin embargo, puede haber **algunas variaciones** entre distros en cuanto a los comandos y herramientas disponibles, debido a:

1. **[[gestores de paquetes]]**: Cada distro usa un **gestor de paquetes** diferente para instalar y actualizar software:
    
    - En **Debian/Ubuntu** se usa `apt`.
    - En **Red Hat/Fedora** se usa `dnf` o `yum`.
    - En **Arch Linux** se usa `pacman`.
    
    Así, aunque el propósito es el mismo (gestionar paquetes), el comando específico varía entre distros.
    
2. **Versiones de software**: Algunas distros, como **Arch Linux**, siempre tienen las versiones más recientes de los comandos, mientras que otras como **Debian** priorizan la estabilidad y pueden ofrecer versiones más antiguas. Esto puede afectar qué opciones o banderas están disponibles para ciertos comandos.
    
3. **Preconfiguraciones y herramientas adicionales**: Algunas distros agregan herramientas o scripts propios para realizar tareas específicas. Por ejemplo, **Ubuntu** incluye comandos específicos como `ubuntu-drivers` para gestionar controladores.
    

### Resumen:

Los comandos básicos de Linux son casi los mismos en todas las distros, pero pueden variar en algunos detalles como el gestor de paquetes o las versiones de los programas. El conocimiento de los comandos generales te permite manejarte bien en cualquier distro, aunque puedas encontrar diferencias menores según la configuración y el propósito de cada una.