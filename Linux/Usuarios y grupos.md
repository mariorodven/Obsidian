1. **Usuarios**:
    
    - **Qué son**: Son las cuentas individuales en un sistema [[¿Qué es Linux?|Linux]]. Cada usuario tiene su propio espacio y configuración en el sistema.
    - **Propósito**: Permiten que múltiples personas usen el mismo sistema de manera segura, manteniendo sus datos y configuraciones separados.
    - **Ejemplo**: Un usuario llamado `juan` puede tener su propio directorio personal (`/home/juan`), configuraciones y archivos.
2. **Grupos**:
    
    - **Qué son**: Son colecciones de usuarios. Los grupos permiten asignar permisos a varios usuarios a la vez.
    - **Propósito**: Facilitan la gestión de permisos y recursos para conjuntos de usuarios.
    - **Ejemplo**: Un grupo llamado `desarrolladores` puede incluir a varios usuarios, permitiéndoles acceso a ciertos archivos o directorios compartidos.

### **Permisos de Archivos y Directorios**

Cada [[Ficheros y carpetas|Archivos y Directorios]] en Linux tiene [[permisos]] específicos que determinan qué acciones pueden realizar los usuarios:

1. **Permisos básicos**:
    
    - **Lectura (r)**: Permite ver el contenido del archivo o listar el contenido de un directorio.
    - **Escritura (w)**: Permite modificar el archivo o añadir/eliminar archivos en un directorio.
    - **Ejecución (x)**: Permite ejecutar el archivo (si es un programa o script) o acceder al directorio.
2. **Asignación de permisos**:
    
    - **Propietario (Usuario)**: El dueño del archivo o directorio. Puede tener permisos independientes.
    - **Grupo**: Los usuarios que pertenecen al grupo asignado al archivo o directorio. Tienen permisos específicos.
    - **Otros**: Todos los demás usuarios en el sistema. Tienen permisos generales para todos los archivos.
    
    **Ejemplo**: Si un archivo tiene permisos `-rwxr-xr--`, significa:
    
    - **`rwx`** (usuario): El propietario puede leer, escribir y ejecutar.
    - **`r-x`** (grupo): Los miembros del grupo pueden leer y ejecutar, pero no escribir.
    - **`r--`** (otros): Todos los demás usuarios pueden solo leer.

### **Super Usuario y Sudo**

1. **Super Usuario (root)**:
    
    - **Qué es**: Es el usuario con el mayor nivel de permisos en el sistema. Tiene acceso completo a todos los archivos y puede realizar cualquier operación.
    - **Uso**: Usado para tareas administrativas como instalar software, cambiar configuraciones del sistema, y gestionar usuarios.
2. **Sudo**:
    
    - **Qué es**: Es una herramienta que permite a los usuarios ejecutar comandos con permisos de superusuario sin necesidad de iniciar sesión como `root`.
    - **Cómo funciona**: Un usuario normal puede ejecutar comandos específicos con permisos elevados usando `sudo`. Se le pedirá la contraseña del usuario para autorizar la acción.
    - **Ejemplo**:
        - `sudo apt update`: Ejecuta el comando `apt update` con permisos de superusuario para actualizar la lista de paquetes.
    - **Beneficio**: Permite a los usuarios realizar tareas administrativas de manera controlada y segura sin darles acceso completo al usuario `root`.

### Resumen

- **Usuarios**: Cuentas individuales en el sistema.
- **Grupos**: Colecciones de usuarios que comparten permisos.
- **Permisos**: Controlan el acceso a archivos y directorios.
- **Super Usuario**: `root`, tiene todos los permisos.
- **Sudo**: Herramienta que permite ejecutar comandos con permisos de superusuario.

Esta estructura ayuda a gestionar la seguridad y el acceso en el sistema, permitiendo un control granular sobre qué usuarios pueden hacer qué.