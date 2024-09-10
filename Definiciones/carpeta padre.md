En el sistema de archivos de Linux (y en muchos otros sistemas operativos), las carpetas o directorios se organizan de manera jerárquica, formando una estructura en forma de árbol. Dentro de esta estructura, los términos carpeta padre y carpeta hija se usan para describir las relaciones entre directorios.

- **Carpeta padre**: Es un directorio que contiene otros directorios o archivos en su interior. Por ejemplo, si tienes la carpeta `/home/usuario/documentos`, la carpeta `/home/usuario` es la carpeta padre de `documentos`. Cada carpeta padre puede tener varias carpetas hijas.
- **Carpeta hija**: Es un directorio que está contenido dentro de otro directorio, es decir, es "hija" de una carpeta superior (la carpeta padre). Siguiendo el ejemplo anterior, la carpeta `documentos` es la carpeta hija de `/home/usuario`.
## Ejemplo

Supongamos esta estructura de directorios:

```
/home 
	└── usuario 
		├── documentos 
		└── imágenes
```

En este caso:
- La carpeta `home` es la carpeta padre de `usuario`.
- La carpeta `usuario` es la carpeta hija de `home`, pero a su vez, es la carpeta padre de `documentos` e `imágenes`.
Esta estructura jerárquica es clave para navegar, organizar y acceder a archivos y carpetas en Linux.