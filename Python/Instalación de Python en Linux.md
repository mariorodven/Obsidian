---
dg-publish: "true"
---
### Instalar y actualizar Python en Linux para distribuciones basadas en **Arch** y **Debian**

Python suele estar preinstalado en la mayoría de las distribuciones Linux, pero a veces puede ser necesario instalarlo manualmente o actualizarlo a la última versión. A continuación, te explico cómo instalar Python, verificar la versión actual y cómo actualizarlo en sistemas **Arch** y **Debian/Ubuntu**.

---

### 1. **Instalar Python en distribuciones basadas en Debian (Ubuntu, Debian, etc.)**

#### a. Verificar si Python está instalado

Primero, verifica si ya tienes Python instalado y qué versión tienes:
```bash
python3 --version
```

Si Python está instalado, verás algo como: `Python 3.x.x`.

#### b. Instalar Python

Si no tienes Python instalado o necesitas instalarlo, sigue estos pasos:

1. **Actualizar los repositorios del sistema:**
```bash
sudo apt update
```
2. **Instalar Python y pip:**
```bash
sudo apt install python3 python3-pip
```
3. **Instalar herramientas adicionales** (opcional, para crear entornos virtuales):
```bash
sudo apt install python3-venv python3-dev
```

#### c. Actualizar Python en Debian/Ubuntu

Para actualizar Python a la última versión disponible en los repositorios, ejecuta:
```bash
sudo apt update
sudo apt upgrade python3
```

Si deseas una versión más reciente que la que se encuentra en los repositorios predeterminados, puedes agregar un PPA (Personal Package Archive):

1. **Agregar el PPA de Python:**
```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
```
2. **Instalar una versión específica de Python (por ejemplo, Python 3.10):**
```bash
sudo apt install python3.10
```
#### d. Comprobar la versión instalada

Una vez que Python esté instalado o actualizado, verifica la versión actual:
```bash
python3 --version
```

### 2. **Instalar Python en distribuciones basadas en Arch (Arch Linux, Manjaro, etc.)**

#### a. Verificar si Python está instalado

Primero, verifica si tienes Python instalado y su versión:

```bash
python3 --version
```

#### b. Instalar Python en Arch

Si Python no está instalado, puedes instalarlo con **pacman**, el gestor de paquetes de Arch:

1. **Actualizar la base de datos de paquetes:**
```bash
sudo pacman -Syu
```

2. **Instalar Python:**
```bash
sudo pacman -S python
```

3. **Instalar pip (el gestor de paquetes de Python):**
```bash
sudo pacman -S python-pip
```

#### c. Actualizar Python en Arch

Para actualizar Python a la última versión en Arch Linux, utiliza:
```bash
sudo pacman -Syu python
```

Esto actualizará Python a la versión más reciente disponible en los repositorios de Arch.

#### d. Comprobar la versión instalada

Una vez que Python esté instalado o actualizado, verifica la versión actual:
```bash
python --version
```

### Resumen de comandos clave:

- **Verificar la versión actual de Python**: `python3 --version` o `python --version` en Arch.
- **Instalar Python en Debian/Ubuntu**: `sudo apt install python3 python3-pip`.
- **Instalar Python en Arch**: `sudo pacman -S python python-pip`.
- **Actualizar Python en Debian/Ubuntu**: `sudo apt upgrade python3`.
- **Actualizar Python en Arch**: `sudo pacman -Syu python`.