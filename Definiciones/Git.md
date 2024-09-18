---
dg-publish: "true"
---
**Git** es un **sistema de control de versiones distribuido**, creado por **Linus Torvalds** en 2005 para gestionar el desarrollo del **[[kernel|kernel de Linux]]**. Su propósito es permitir a los programadores colaborar en proyectos de software, manteniendo un registro detallado de los cambios en el código a lo largo del tiempo, sin depender de un servidor central.

### Características clave de Git:

1. **Control de versiones distribuido**: A diferencia de los sistemas centralizados, en Git cada desarrollador tiene una copia completa del historial del proyecto, lo que permite trabajar de manera independiente sin estar siempre conectado a un servidor central.
    
2. **Rendimiento eficiente**: Git está diseñado para ser rápido, especialmente en operaciones comunes como fusiones (merge) o diferencias (diff). Es muy eficiente en cuanto a cómo gestiona los cambios y el historial del proyecto.
    
3. **Branching y merging**: Git facilita la creación de ramas (**branches**) para trabajar en diferentes características o correcciones de errores de manera aislada. Luego, estas ramas se pueden fusionar (**merge**) de manera eficiente con el código principal. Esto fomenta una metodología de trabajo flexible.
    
4. **Integridad y seguridad**: Cada cambio en Git se identifica mediante un hash único (SHA-1), lo que garantiza la integridad de los datos y la capacidad de verificar el historial sin modificaciones no autorizadas.
    
5. **Soporte para trabajo colaborativo**: Git permite que múltiples desarrolladores trabajen en el mismo proyecto simultáneamente. Las herramientas de control de versiones y las estrategias de fusión permiten resolver conflictos cuando varias personas modifican las mismas partes del código.
    

### Flujo de trabajo en Git

1. **Clonación (clone)**: Los desarrolladores copian un repositorio existente en sus sistemas locales.
2. **Ramas (branches)**: Se crean ramas para trabajar en nuevas características o correcciones.
3. **Commits**: Los desarrolladores hacen _commits_ para registrar cambios en el código.
4. **Push y pull**: Se "empujan" (_push_) los cambios al repositorio remoto, y otros pueden "extraer" (_pull_) esos cambios para sincronizar sus copias locales.

### GitHub, GitLab y otros

**Git** no depende de ninguna plataforma específica, pero **GitHub**, **GitLab** y **Bitbucket** son servicios populares que alojan repositorios Git y añaden herramientas adicionales para la colaboración, como revisiones de código, seguimiento de problemas y despliegues automáticos.

### ¿Por qué es tan popular?

Git es ampliamente utilizado porque:

- Es flexible y se adapta a diferentes flujos de trabajo.
- Es rápido, eficiente y escalable.
- Ha sido adoptado por la mayoría de los desarrolladores y equipos, convirtiéndose en un estándar en la industria del software.