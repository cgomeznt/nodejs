Instalar una versión personalizada de NVM y Node.js
=======================================================

Instalar Node Version Manager (NVM)
+++++++++++++++++++++++++++++++++++++

Los siguientes pasos instalan Node Version Manager. Luego, puedes usar NVM para instalar Node.js.

Inicia sesión en tu servidor vía SSH.

Visita la siguiente página para determinar que versión de NVM instalar::

  https://github.com/nvm-sh/nvm#install-script

Confirma que estás en el directorio de tu usuario.::

  cd ~

Corre el siguiente comando para descargar NVM. Cambia la versión según sea necesario::

  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

o::

  wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

Este comando instala nvm en un nuevo directorio bajo tu usuario llamado /.nvm

Este comando también agrega lo siguiente a tu archivo .bashrc::

  export NVM_DIR="$HOME/.nvm"
  [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
  [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # This loads nvm bash_completion

Actualiza tu archivo .bashrc para usar estas nuevas configuraciones::

  source .bashrc

Confirma que tu directorio local .nvm está configurado::

  echo $NVM_DIR
  /home/username/.nvm

Edita tu .bash_profile y agrega la siguiente línea::

  source ~/.bashrc

Actualiza tu .bash_profile para que puedas usar esta nueva versión de nvm::

  . ~/.bash_profile

Corre el siguiente comando para probar si nvm está instalado::

  nvm --version
  0.39.7

Instalar Node.js
+++++++++++++++++++

Ahora que se ha instalado nvm, puedes usarlo para instalar Node.js

Revisa qué versiones de Node.js están disponibles::

  nvm ls-remote

Instala cualquier versión de Node.js que desees::

  nvm install v12.22.7

Establece tu versión actual de node a tu nueva versión::

  nvm use v12.22.7
  Now using node v12.22.7 (npm v)

Comprueba qué versión de Node.js se está ejecutando ingresando lo siguiente::

  node -v
  v12.18.3

Establecer la versión predeterminada de Node.js
++++++++++++++++++++++++++++++++++++++++++++++++++

Después de instalar una nueva versión de Node.js, tu sesión actual de Shell debería usarla automáticamente cuando vuelvas a iniciar sesión. Si notas que la versión no es correcta, es posible que debas revisar las instrucciones de .bash_profile de arriba. También puedes configurar la nueva versión como tu versión predeterminada corriendo el siguiente comando.

Asegúrate de cambiar el número de versión a la versión que has instalado. Este ejemplo usa v12.22.7::

  nvm alias default v12.22.7
  default -> v12.22.7

Probar Node.js
+++++++++++++++


