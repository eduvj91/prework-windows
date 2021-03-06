          ██████╗ ██████╗ ███████╗██╗    ██╗ ██████╗ ██████╗ ██╗  ██╗
          ██╔══██╗██╔══██╗██╔════╝██║    ██║██╔═══██╗██╔══██╗██║ ██╔╝
          ██████╔╝██████╔╝█████╗  ██║ █╗ ██║██║   ██║██████╔╝█████╔╝ 
          ██╔═══╝ ██╔══██╗██╔══╝  ██║███╗██║██║   ██║██╔══██╗██╔═██╗ 
          ██║     ██║  ██║███████╗╚███╔███╔╝╚██████╔╝██║  ██║██║  ██╗
          ╚═╝     ╚═╝  ╚═╝╚══════╝ ╚══╝╚══╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝
                                                                     
           ██╗    ██╗██╗███╗   ██╗██████╗  ██████╗ ██╗    ██╗███████╗
           ██║    ██║██║████╗  ██║██╔══██╗██╔═══██╗██║    ██║██╔════╝
           ██║ █╗ ██║██║██╔██╗ ██║██║  ██║██║   ██║██║ █╗ ██║███████╗
           ██║███╗██║██║██║╚██╗██║██║  ██║██║   ██║██║███╗██║╚════██║
           ╚███╔███╔╝██║██║ ╚████║██████╔╝╚██████╔╝╚███╔███╔╝███████║
            ╚══╝╚══╝ ╚═╝╚═╝  ╚═══╝╚═════╝  ╚═════╝  ╚══╝╚══╝ ╚══════╝

# ¿Que es WSL2 (Windows Subsystem for Linux)?

Es un ambiente de desarrollo GNU/Linux dentro de *Windows* para desarrollo.

Hay que seguir ciertos pasos para poder realizar la instalación de  WSL.

- Verifica la version de nuestro SO desde la terminal.
- Teclas `windows + r` que abre ejecutar
- Escribir `cmd`
- Escribir en la linea de comandos `winver` que nos abrirá el Acerca de Windows

> Nota.- Para utilizar WSL necesitamos Windows-10 y versiones del 2004 19041 o posteriores.

# Instalando WSL

En este caso vamos a seguir los pasos de instalación normal de la liga de windows para su instalación.

[WSL2 enlace](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

> Nota.- Toda la instalación y configuración se realizan desde Windows Power Shell con permisos de administrador.
> Nota.- Reiniciar la computadora después de instalar WSL para que funcione correctamente todo. 

# Configuración de Ubuntu en WSL

Cuando iniciamos Ubuntu generalmente nos pedirá crear un usuario y contraseña para poder entrar al WSL Ubuntu. Después de esto es importante lo siguiente:

Importante:
- Que los proyectos para desarrollo estén creados dentro de la carpeta del usuario de Ubuntu.
- No crear o mover archivos desde el explorador de archivos.

# Comandos básicos de la terminal e instalación de Node.js

¿Qué es node?

Es un run time environment, un ambiente de ejecución para escribir comandos de js, sirve para backend y ejecución de dependencias backend.

Linux y WSL son SO de software libre, los cuales usan algo llamado gestor de paquetes o handler de dependencias; podrían ser considerado como la tienda de herramientas para estos SO, lo cual son un repositorio de dependencias.

- Con el comando dentro de Ubuntu: `sudo apt-get update (para actualizar las dependencias)`
- Ahora que esta actualizadas las dependencias hay que aplicarlas con el comando: `sudo apt-get upgrade`
- Siguiente paso es instalar node.js para esto usamos el comando de instalación: `sudo apt install <dependencia>`
- Confirmar la version instaladas: `node -v`

> Como instalar la ultima version estable de node

Enlace: <https://midu.dev/como-instalar-node-en-mac-y-windows/>

Instalaremos npm que es el handler de paquetes de node
´sudo apt install npm´

¿Qué es npm?
Es una librería de frameworks y dependencias que la comunidad de desarrolladores ha creado y sigue creando

Recordemos que con sudo antes de cualquier comando lo hacemos con permisos de administrador, con lo cual nos pedirá la contraseña del usuario creado en Ubuntu no la del sistema windows.

Haciendo algunos cambios para poder ver si funciona github.

Instala git a su ultima version: <https://www.bytesized.xyz/how-to-update-git-in-ubuntu-windows-subsystem-for-linux/>
