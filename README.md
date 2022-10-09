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

Es un ambiente de desarrollo GNU/Linux dentro de *Windows* para desarrollo que funciona en la terminal.

Hay que seguir ciertos pasos para poder realizar la instalación de  WSL.

- Verifica la version de nuestro SO desde la terminal.
- Teclas `windows + r` que abre ejecutar
- Escribir `cmd`
- Escribir en la linea de comandos `winver` que nos abrirá el **"Acerca de Windows"**

> *Nota.- Para utilizar WSL necesitamos Windows-10 y versiones del 2004 19041 o posteriores*

# Instalando WSL

En este caso vamos a seguir los pasos de instalación normal de la liga de windows para su instalación.

[WSL2 instalación](https://learn.microsoft.com/es-mx/windows/wsl/install)

> Notas:
> - Toda la instalación y configuración se realizan desde Windows Power Shell con permisos de administrador.
> - Reiniciar la computadora después de instalar WSL para que funcione correctamente todo, en la ventana nos dice este mensaje.
> - Al reiniciar, automaticamente se abre ubunto y nos da las opciones de colocar nuestro usuario y contraseña.

# Configuración de Ubuntu en WSL

Cuando iniciamos Ubuntu generalmente nos pedirá crear un usuario y contraseña para poder entrar al WSL Ubuntu. Después de esto es importante lo siguiente:

> Importante:
> - Actualizar y aplicar las dependiencias con los comandos `sudo apt-get update & upgrade`.
> - Que los proyectos para desarrollo estén creados dentro de la carpeta del usuario de Ubuntu.
> - No crear o mover archivos desde el explorador de archivos.

Antes de seguir instalando personalizaremos nuestra terminal y cambiaremos la shell por defecto que en este caso es bash.

## Personalizando terminal para el trabajo con NVIM

1. Seguimos la instrucciones para instalar oh-myzsh [aquí](https://github.com/ohmyzsh/ohmyzsh/wiki)
2. Instalamos tema para oh-mayzsh *powerlevel10k* [aquí](https://github.com/romkatv/powerlevel10k#installation)
3. Instalanmos plugins para oh-myzsh [plugins recomendados](https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df)
4. Configuramos vim para trabajar y neovim después de instalar ahora si los siguientes puntos, node y git.

# Comandos básicos de la terminal e instalación de Node.js

¿Qué es node?

Es un run time environment, un ambiente de ejecución para escribir comandos de js, sirve para backend y ejecución de dependencias backend.

Linux y WSL son SO de software libre, los cuales usan algo llamado gestor de paquetes o handler de dependencias; podrían ser considerado como la tienda de herramientas para estos SO, lo cual son un repositorio de dependencias.

- Con el comando dentro de Ubuntu: `sudo apt-get update (para actualizar las dependencias)`
- Ahora que esta actualizadas las dependencias hay que aplicarlas con el comando: `sudo apt-get upgrade`
- Siguiente paso es instalar node.js para esto usamos el comando de instalación: `sudo apt install <dependencia>`
- Confirmar la version instaladas: `node -v`

> Como instalar la ultima version estable de node

[Node desde nvm](https://midu.dev/como-instalar-node-en-mac-y-windows/)

Instalaremos npm que es el manejador o handler de paquetes de node
´sudo apt install npm´

¿Qué es npm?
Es una librería de frameworks y dependencias que la comunidad de desarrolladores ha creado y sigue creando.

Recordemos que con *sudo* antes de cualquier comando lo hacemos con permisos de administrador, con lo cual nos pedirá la contraseña del usuario creado en Ubuntu no la del sistema windows.

# Instala Git

Instalando Git mediante un manejador de paquetes APP.

[Instala git a su ultima version](https://www.bytesized.xyz/how-to-update-git-in-ubuntu-windows-subsystem-for-linux/)

- Crear nuestra llave ssh para poder descargar los repos de GitHub mediante este medio.[Git & GitHub](https://github.com/eduvj91/git-github#configura-tus-llaves-ssh-en-local)

# Instalando y configurando NEOVIM

Para esto hemos creado un repo en GitHub con todas las configuraciones necesarias, el nombre es .config que es donde van todas las configuraciones necesarias para nvim y demas plugins.

1. Clonar repositorio .config
2. Crear el link simbolico `ln -s [target file] [Symbolic filename]` para .zshrc que esta dentro de .config para mantener historial git, revisar los cambios en estos archivos.
3. Instalar paquete de idiomas windows terminal en español en dado caso de necesitar. [cambia idioma terminal](https://terminaldelinux.com/terminal/introduccion/idioma-terminal-espanol/)
4. Descargamos Vim-Plug para los complementos de vim.
5. Creamos enlace simbolico para nuestro .vimrc que esta dentro de .config
6. Instala la ultima version de Vim y NeoVim [Vim PPA](https://www.ochobitshacenunbyte.com/2021/02/15/instalar-la-ultima-version-de-vim-en-linux/) y [Nvim PPA](https://es.linuxcapable.com/how-to-install-neovim-editor-on-ubuntu-22-04-lts/)
7. En vim si aparece error de idomas solo poner en la linea de comandos set spell y nos ayudara a descargar los ficheros en .vim/local/spell y para neovim en .local/share/spell.
