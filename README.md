Curso de prework: Configuración de entorno de desarrollo en Windows

# ¿Que es WSL2 (Windows Subsystem for Linux)?

Es un ambiente de desarrollo GNU/Linux dentro de Windows para desarrollo.

Hay que seguir ciertos pasos para poder realizar la instalación de  WSL.

- Verifica la version de nuestro SO desde la terminal.
	teclas windows + r que abre ejecutar
	escibir cmd
	escirbir en la linea de comandos winver que nos abrira el Acerca de Windows

Nota.- Para utilizar WSL necesitamos Windows10 y versiones del 2004 19041 o posteriores.


# Instalando WSL

En este caso vamos a seguir los pasos de instalación normal de la liga de windows para su instalación.

link: https://docs.microsoft.com/en-us/windows/wsl/install-win10

Hay un paso importante cuando tratamos de cambiar la version a WSL 2 

wsl --set-default-version 2

Al paraecer lanza un herror de que no se encuentra correctamente instalado yo reinicie mi maquina y despes volvi a poner el comando de arriba y funciono.

Algo más que encontre es que hay que ejecutar el la actualización del kernel de linux que nos da la documentaicón de windows para poder cambiar a la version 2

Nota.- Toda la instalación y configuración se realizan desde Windows PowerShell con permisos de administrador.

# Configuración de ubunto en WSL

Cuando inicamos ubunto generalmente nos pedira crear un usuario y contraseñá para poder entrar al WSL ubunto. despues de esto es importante lo siguiente:

Que los proyectos para desarrollo esten creados dentro de la carpeta del usuario de ubunto.
No crear o mover archivos desde el explorador de archivos.

# Comandos básicos de la terminal e instalación de Node.js

¿Qué es node?

Es un run time enviroment, un ambiente de ejecución para escribir comandos de js, sirve para backend y ejecución de dependencias backend.

Linux y WSL son SO de softwer libre, los cuales usan algo llamado gestor de paquetes o manejador de depedencias; podrian ser conciderado como la tienda de herramientas para estos SO, lo cual son un repositorio de dependencias.

Con el comando dentro de ubunto por obviedad: sudo apt-get update (para actualizar las dependencias)
Ahora que esta actualizadas las dependncias hay que aplicarlas con el comando: sudo apt-get upgrade.
Siguiente paso es instalar node.js para esto usamos el comando de instalación: sudo apt install <dependencia>.
Checar la version instaladas: node -v

Instalaremos npm que es el manejador de paquetes de node
´sudo apt install npm´

¿Qué es npm?
Es una libreria de freamworks y dependencias que la comunidad de desarrolladores ha creado y sigue creando

Recordemos que con sudo antes de cualquier comando lo hacemos con permisos de administrador, con lo cual nos pedira la contraseñá del usuario creado en ubunto no la del sistema windows.

Haciendo algunos cambios para poder ver si funciona github.
