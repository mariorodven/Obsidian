### **Distribuciones Basadas en Debian**

- **Qué son**: Son sistemas operativos que utilizan Debian como su base. Estas distribuciones heredan la estabilidad y la estructura de Debian pero a menudo añaden sus propias características, herramientas o cambios de diseño.
- **Ejemplos populares**:
    - **Ubuntu**: Muy conocida por su facilidad de uso y enfoque en la accesibilidad para nuevos usuarios. Tiene versiones de escritorio y servidor y una amplia base de usuarios y soporte.
    - **Linux Mint**: Derivada de Ubuntu, conocida por su enfoque en la simplicidad y facilidad de uso, especialmente para usuarios que vienen de Windows.
    - **Debian**: La distribución original en la que se basan otras distros, conocida por su estabilidad y robustez.
- Fiabilidad: esa es la palabra que definiría a las [[distros]] basadas en debian, dado que tienen un [[kernel]] a prueba de balas, el cual no tiene la última versión pero si tiene muchas pruebas para que no haya bugs ni problemas.
### **APT (Advanced Package Tool)**

- **Qué es**: Es el sistema de gestión de paquetes utilizado por Debian y las distribuciones basadas en Debian.
- **Funciones**: Permite instalar, actualizar y eliminar paquetes de software.
- **Comandos comunes**:
    - `apt update`: Actualiza la lista de paquetes disponibles.
    - `apt install nombre_paquete`: Instala un paquete.
    - `apt upgrade`: Actualiza todos los paquetes instalados a sus versiones más recientes.
    - `apt remove nombre_paquete`: Elimina un paquete.

### **Backports**

- **Qué son**: Son versiones más nuevas de paquetes que han sido adaptadas para ser usadas en versiones estables de Debian.
- **Uso**: Permiten que las versiones de software más recientes se puedan instalar en una versión estable de Debian sin cambiar toda la distribución.
- **Ejemplo**: Si una nueva versión de un programa tiene características importantes pero tu versión de Debian es estable, puedes habilitar los backports para instalar esta versión más reciente.

En resumen, las distribuciones basadas en Debian como **Ubuntu** y **Linux Mint** utilizan **APT** para gestionar paquetes y a menudo hacen uso de **backports** para proporcionar versiones más recientes de software en sistemas estables.