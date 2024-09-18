---
dg-publish: "true"
---
Un **entorno virtual** en Python permite aislar las dependencias de un proyecto, evitando conflictos con otros proyectos y con el sistema global. Aquí te explico cómo crear un entorno virtual y utilizar `pip` para instalar paquetes en distribuciones basadas en **Arch** y **Debian**.

#### 1. **Instalar Python y pip**

Primero, asegúrate de tener Python y `pip` (el administrador de paquetes de Python) instalados.

- En **[[Debian|Debian/Ubuntu]]** usando [[gestores de paquetes|apt]]:
```zsh
sudo apt update
sudo apt install python3 python3-pip python3-venv
```
- En **[[Arch|Arch Linux]]** usando [[gestores de paquetes|pacman]]:
```bash
sudo pacman -S python python-pip
```

#### 2. **Crear el entorno virtual**

El comando `venv` de Python permite crear un entorno virtual.

- Ve al directorio donde quieres crear tu entorno virtual.
- Crea el entorno virtual usando el siguiente comando:
```bash
python3 -m venv nombre_del_entorno
```

Esto creará un directorio llamado `nombre_del_entorno`, donde se almacenarán los archivos del entorno virtual.

#### 3. **Activar el entorno virtual**

Para **activar** el entorno virtual, usa el siguiente comando:

```bash
source nombre_del_entorno/bin/activate
```

Después de la activación, tu terminal mostrará el nombre del entorno virtual al inicio de cada línea, lo que indica que está activo. Todos los paquetes instalados a partir de ahora serán locales al entorno y no afectarán al sistema global.

#### 4. **Instalar paquetes usando pip**

Con el entorno virtual activado, puedes instalar paquetes utilizando `pip`:

```bash
pip install nombre_del_paquete
pip install requests
pip install -r requirements.txt
```

#### 5. **Usar los paquetes instalados en el código**

Una vez instalado el paquete, puedes usarlo en tu código Python importándolo como lo harías normalmente:

```python
import requests

response = requests.get("https://www.example.com")
print(response.status_code)
```

#### 6. **Desactivar el entorno virtual**

Cuando termines de trabajar, puedes desactivar el entorno virtual con el comando:

```bash
deactivate
```

Esto te devuelve al entorno del sistema global.

#### Resumen de pasos:

1. Instala Python y `pip`.
2. Crea el entorno virtual: `python3 -m venv nombre_del_entorno`.
3. Activa el entorno: `source nombre_del_entorno/bin/activate`.
4. Instala paquetes con `pip`.
5. Usa los paquetes importándolos en tu código Python.
6. Desactiva el entorno con `deactivate`.

Este flujo de trabajo te permite gestionar proyectos Python de manera organizada y sin interferir con otras instalaciones o proyectos.