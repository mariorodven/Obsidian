## Permisos

En Linux, los **permisos** determinan quién puede leer, modificar o ejecutar un archivo o directorio. Estos permisos se dividen en tres grupos principales:

1. **Usuario (owner)**: El dueño del archivo o directorio.
2. **Grupo**: Un conjunto de usuarios que comparten ciertos permisos.
3. **Otros**: Todos los demás usuarios del sistema.

Cada archivo o directorio tiene tres tipos de permisos:

1. **Lectura (r)**: Permite ver el contenido del archivo o listar los archivos dentro de un directorio.
2. **Escritura (w)**: Permite modificar el archivo o añadir/eliminar archivos dentro de un directorio.
3. **Ejecución (x)**: Permite ejecutar el archivo (si es un programa o script) o acceder a un directorio.

### Ejemplo de permisos:

Cuando ejecutas el comando `ls -l` para listar archivos, verás algo así:

```bash
-rwxr-xr--
```

Esto se descompone así:

- **rwx** (primer conjunto): Los permisos del **usuario** (puede leer, escribir y ejecutar).
- **r-x** (segundo conjunto): Los permisos del **grupo** (puede leer y ejecutar, pero no escribir).
- **r--** (tercer conjunto): Los permisos de **otros** (solo pueden leer).

### Modificar permisos:

Para cambiar los permisos, se usa el comando `chmod`. Por ejemplo, para dar permiso de ejecución a todos, se usaría:

```bash
chmod +x archivo
```

En resumen, los permisos de Linux permiten controlar qué usuarios pueden acceder y hacer qué cosas con cada archivo o directorio, manteniendo el sistema seguro y organizado.