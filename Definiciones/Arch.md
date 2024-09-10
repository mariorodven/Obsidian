### **Arch Linux**

- **Qué es**: Arch Linux es una [[distros|distribución]] de Linux conocida por su simplicidad, flexibilidad y enfoque en la personalización. Está diseñada para usuarios avanzados que quieren construir su sistema desde cero y tener control total sobre su configuración.
- **Características**: Minimalista y ligera, permite al usuario instalar solo lo necesario y personalizar cada aspecto del sistema.

### **Rolling Release**

- **Qué es**: Un modelo de actualización de software en el que el sistema recibe actualizaciones continuas en lugar de lanzar nuevas versiones mayores en intervalos regulares.
- **Ventaja**: Siempre tienes el software más reciente sin necesidad de realizar grandes actualizaciones de versión. Arch Linux sigue este modelo, lo que significa que se actualiza constantemente con las últimas versiones de paquetes. Por otro lado, si el [[kernel]] nuevo tuviese algún defecto no se detectaría porque no se ha sometido a prueba. Al igual que en todas las demas distros puedes acceder a los diferentes [[Tipos de Kernel]] en la instalación del sistema operativo.
### **Pacman**

- **Qué es**: Es el gestor de paquetes de Arch Linux.
- **Funciones**: Permite instalar, actualizar y eliminar paquetes de software en el sistema.
- **Comandos comunes**:
    - `pacman -S nombre_paquete`: Instala un paquete.
    - `pacman -Syu`: Actualiza todos los paquetes del sistema.
    - `pacman -R nombre_paquete`: Elimina un paquete.

### **AUR (Arch User Repository)**

- **Qué es**: Es un repositorio mantenido por la comunidad para Arch Linux que contiene paquetes no oficiales que no están en los repositorios oficiales.
- **Uso**: Permite a los usuarios acceder a una gran variedad de software adicional y personalizado. Los paquetes en el AUR deben ser construidos a partir de scripts de construcción proporcionados por la comunidad.

En resumen, Arch Linux es una distribución flexible y minimalista que utiliza un modelo de actualización rolling release. `pacman` es su gestor de paquetes, y el **AUR** es un repositorio comunitario que expande la oferta de software disponible.