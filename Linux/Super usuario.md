En Linux, el **superusuario** (también conocido como **root**) es una cuenta con el nivel más alto de [[Permisos]] en el sistema.
### **Qué es el Superusuario (root)**

- **Definición**: El superusuario es el usuario principal del sistema con acceso total a todos los [[Sistema de Archivos de Linux|archivos]] y configuraciones del sistema. Es la cuenta con todos los privilegios, sin restricciones.
- **Nombre de usuario**: En la mayoría de las [[distros|distribuciones]] de Linux, el superusuario se llama `root`.

### **Funciones y Privilegios del Superusuario**

1. **Acceso Completo**: Puede leer, modificar y eliminar cualquier archivo o directorio en el sistema.
2. **Configuración del Sistema**: Puede cambiar configuraciones del sistema, como ajustar la red, instalar y desinstalar software, y configurar servicios del sistema.
3. **Gestión de Usuarios**: Puede crear, modificar y eliminar cuentas de usuario y grupos.
4. **Mantenimiento del Sistema**: Puede realizar tareas de mantenimiento crítico, como actualizar el sistema operativo y gestionar el hardware.

### **Uso del Superusuario**

1. **Acceso Directo**:
    
    - Puedes iniciar sesión directamente como `root` usando el [[Comandos básicos de Bash|comando]] `su` (substitute user) y proporcionando la contraseña de `root`.
    - Ejemplo: `su` te pedirá la contraseña de `root` y te cambiará al usuario `root`.
2. **Uso de Sudo**:    
    - Es una práctica más segura usar `sudo` (superuser do) para ejecutar comandos específicos con permisos de superusuario sin iniciar sesión como `root`.
    - Ejemplo: `sudo comando` ejecuta el comando con privilegios de superusuario. Por ejemplo, `sudo apt update` actualiza la lista de paquetes con permisos elevados.

- **Ejemplos como**:

```bash
[user@localhost:~$](<[mario@archVictus carpeta]$ sudo mkdir superCarpeta
[sudo] password for mario: 
[mario@archVictus carpeta]$ ls superCarpeta/
[mario@archVictus carpeta]$ sudo touch superCarpeta/superFichero.txt
[mario@archVictus carpeta]$ nano superCarpeta/superFichero.txt 
[mario@archVictus carpeta]$ echo "Hola" %3E> superCarpeta/superFichero.txt 
bash: superCarpeta/superFichero.txt: Permission denied
[mario@archVictus carpeta]$ rm -rf superCarpeta/
rm: cannot remove 'superCarpeta/superFichero.txt': Permission denied>)
```

### **Precauciones y Seguridad**

1. **Evitar el Uso Innecesario**:
    
    - No se recomienda iniciar sesión como `root` de manera regular, ya que cualquier error o comando mal ejecutado puede afectar seriamente el sistema. En su lugar, usa `sudo` para realizar tareas específicas que requieran permisos elevados.
2. **Contraseña Segura**:
    
    - Asegúrate de que la contraseña de `root` sea segura y difícil de adivinar para proteger el sistema contra accesos no autorizados.
3. **Minimizar Riesgos**:
    
    - Realiza operaciones como `root` solo cuando sea absolutamente necesario y asegúrate de entender las consecuencias de los comandos que ejecutas.

### **Resumen**

- **Superusuario (root)**: Tiene acceso total y sin restricciones a todos los aspectos del sistema.
- **Acceso**: Se puede obtener mediante `su` para iniciar sesión directamente o `sudo` para ejecutar comandos específicos con permisos elevados.
- **Seguridad**: Se recomienda usar `sudo` para minimizar riesgos y evitar errores que puedan afectar al sistema.

El superusuario es crucial para la administración del sistema, pero debe usarse con cuidado para mantener la estabilidad y seguridad del sistema operativo.

### **Carpeta [[Sistema de Archivos de Linux|/root]] **

1. **Qué es**:
    
    - **Directorio Personal**: `/root` es el directorio de inicio del usuario `root`. Similar a cómo cada usuario tiene su propio directorio personal (por ejemplo, `/home/juan` para el usuario `juan`), el superusuario tiene su propio espacio en `/root`.
    - **Ubicación**: Está ubicado en la raíz del sistema de archivos, es decir, directamente bajo `/`.
2. **Propósito**:
    
    - **Configuraciones y Archivos del Superusuario**: Contiene archivos de configuración y documentos específicos para el usuario `root`. Estos archivos pueden incluir scripts, configuraciones del sistema y otros datos importantes que el superusuario puede necesitar.
    - **Espacio de Trabajo**: Proporciona un lugar específico donde `root` puede almacenar archivos y configuraciones que no deben mezclarse con los archivos de otros usuarios.
3. **Acceso**:
    
    - **Permisos**: Solo el usuario `root` tiene acceso completo a este directorio. Los demás usuarios no tienen permisos para leer, escribir o ejecutar archivos en `/root`.
    - **Seguridad**: El acceso restringido a `/root` ayuda a proteger las configuraciones críticas y los archivos del sistema que solo deben ser modificados por el superusuario.

### **Relación con el Superusuario**

1. **Inicio de Sesión como Root**:
    
    - Cuando el superusuario inicia sesión, su directorio de inicio es `/root`. Esto significa que, al iniciar sesión como `root`, te encuentras automáticamente en el directorio `/root`.
2. **Uso de `sudo`**:
    
    - Aunque `sudo` permite ejecutar comandos como `root` sin iniciar sesión como `root`, no cambia el directorio de inicio. Los comandos ejecutados con `sudo` no necesariamente afectan el directorio `/root` a menos que se especifique explícitamente.

### **Ejemplos de Uso**

- **Archivos de Configuración**: Un archivo de configuración del sistema que el superusuario necesita modificar podría estar guardado en `/root`.
- **Scripts**: El superusuario puede almacenar y ejecutar scripts desde `/root`.

### **Resumen**

- **`/root`**: Es el directorio personal del superusuario `root`, ubicado directamente bajo la raíz del sistema de archivos (`/`).
- **Acceso**: Solo `root` tiene permisos completos sobre este directorio.
- **Propósito**: Sirve para almacenar archivos y configuraciones importantes y específicos del superusuario.

La carpeta `/root` es fundamental para el manejo y configuración del sistema desde la cuenta de superusuario, proporcionando un espacio seguro y específico para las tareas administrativas.