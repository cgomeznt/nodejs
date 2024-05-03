Instalar Node.js y NPM en CentOS 7.x
==================================

Instalación de Node.js y NPM en servidor con CentOS 7

Pre Requisitos
-------------------

Tener acceso sudo o root  al servidor y salida al Internet.

Instalación y Configuración
---------------------------

Actualizamos el Sistema Operativo con los repos oficiales y el EPEL::

	yum clean all
	yum -y update
 
Utilizar el sitio oficial de Node.js (para las versiones estables)::

	yum install -y gcc-c++ make
	curl -sL https://rpm.nodesource.com/setup_14.x | sudo -E bash -

Instalamos y tambien el NPM y algunos paquetes adicionales::

	yum install nodejs
	yum install npm
	
Confirmar la versión
---------------------

Para verificar node::

	node -v

Para verificar npm::

	npm -v