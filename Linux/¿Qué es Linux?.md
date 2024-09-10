[Linux](https://en.wikipedia.org/wiki/Linux) es un **[[kernel]]**, es decir, la parte central de un sistema operativo que conecta el hardware con los programas. Las **[[distros]] de Linux** (abreviación de "distribuciones") son sistemas operativos completos que usan ese kernel. Es como si Linux fuera una marca de coches, y cada **distro** fuera un modelo diferente de coche.

Hay muchos tipos de distros, como hay diferentes tipos de coches: algunos son más sencillos, otros tienen más funciones, algunos están diseñados para trabajar rápido, otros para ahorrar recursos, y también hay distros personalizadas por los usuarios.

En cuanto a las diferencias entre las distros, aunque existen, no son muy importantes. Si sabes usar bien una distro de Linux, te será fácil adaptarte a las demás, ya que todas comparten la misma base.


## ¿Y que diferencias tiene Linux con Windows?

Pues primero déjame decirte que ambas hacen lo mismo, solo que el 99% de las aplicaciones están hechas para funcionar en windows. Entonces, ¿para qué molestarme en aprender a usar Linux? Muy simple, es mejor que windows en otros muchos aspectos. 
- Es gratis
- Es 100% personalizable
- No tiene nada de spyware o software de empresas
- Tiene alternativas a las aplicaciones de windows que suelen ser [[open source]] 
- ¿He dicho ya que es gratis?
- Fácil de usar
Para un usuario común que usa el ordenador en el día a día usando programas de ofimática y el navegador, no hay diferencia. Pero para nosotros que queremos programar, hay un mundo entre estos dos sistemas operativos. La mayor diferencia entre Linux y Windows es el archiconocido terminal, el cual le causa tanto temor a los novatos y tanto adoramos los que lo sabemos usar. Pero no te preocupes, la terminal es una herramienta como cualquier otra, Windows también tiene una, no es tan increíble como la de Windows.

## La terminal

![[terminal.jpg]]
La temible terminal, es al fin y al cabo una forma que tenemos de interactuar con el sistema, en este caso a través de [[Comandos básicos de Bash]]. Siempre van a tener la siguiente estructura:

```bash
user@localhost:~$ <command> <flags> <arguments>
usuario@maquina:~$ <comando> <banderas> <argumentos>
```

Por ejemplo, el comando [[Comandos básicos de Bash#^379a45|mkdir]], crea una carpeta, toma como argumento el nombre de la carpeta que queremos crear en el directorio que queramos.

```zsh
user@localhost:~$ mkdir miCarpeta
```

Crea una carpeta llamada miCarpeta en el directorio actual

```zsh
user@localhost:~$ mkdir miCarpeta/subCarpeta
```

Ahora hemos creado una carpeta nueva dentro de la anterior, pero, ¿no es un poco tedioso hacer esto en dos comandos?, veamos como podemos optimizar el proceso. Usaremos una bandera, pero, ¿cual?, pues podemos ver todas las banderas disponibles usando la bandera `--help`, que es común a casi todos los comandos. 

```zsh
user@localhost:~$ mkdir --help
Usage: mkdir [OPTION]... DIRECTORY...
Create the DIRECTORY(ies), if they do not already exist.

Mandatory arguments to long options are mandatory for short options too.
  -m, --mode=MODE   set file mode (as in chmod), not a=rwx - umask
  -p, --parents     no error if existing, make parent directories as needed,
                    with their file modes unaffected by any -m option.
  -v, --verbose     print a message for each created directory
  -Z                   set SELinux security context of each created directory
                         to the default type
      --context[=CTX]  like -Z, or if CTX is specified then set the SELinux
                         or SMACK security context to CTX
      --help        display this help and exit
      --version     output version information and exit

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report any translation bugs to <https://translationproject.org/team/>
Full documentation <https://www.gnu.org/software/coreutils/mkdir>
or available locally via: info '(coreutils) mkdir invocation'

```

Vemos que la bandera -p nos permite crear una carpeta dentro de otra , es decir, que podemos hacer todas las carpetas que queramos dentro de un solo comando, tanto separadas como dentro de otra.

```zsh
user@localhost:~$ mkdir -p carpeta1/carpeta2/carpeta3/carpeta4
user@localhost:~$ tree carpeta1
carpeta1
└── carpeta2
    └── carpeta3
        └── carpeta4
```

![[distros2.png]]
![[distros.png]]
