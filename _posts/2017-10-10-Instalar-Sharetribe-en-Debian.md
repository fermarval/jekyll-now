<p align="center">
  <img src="https://irp-cdn.multiscreensite.com/b3c540b6/dms3rep/multi/tablet/Sharetribe-1279x226.Logo.no-margin.png">
</p>

**Parte I. Instalando los requisitos**

* **Ruby**: La versión **2.3.4** es la que actualmente usa, no se garantiza que funcione correctamente con otras versiones. Si necesitas varias versiones de Ruby, se recomienda usar `rvm`. [Instalar Ruby en Debian](https://fermarval.github.io/Instalar-Ruby-en-Debian-Stretch/).

* **RubyGems**: Disponible con la descarga y compiplación de Ruby.

* **Bundler**: Lo instalamos de la siguiente manera: `gem install bundler`.

* **Node**: La versión **6.9** es la que actualmente usa, no se garantiza que funcione correctamente con otras versiones. Si necesitas usar diferentes versiones de Node, considera usar `n` or `nvm`. [Instalar Node.js en Debian](https://fermarval.github.io/Instalar-Node.JS-en-Debian-Stretch/).

* **Git**: Lo instalamos de la siguiente manera: `sudo apt-get install git-core`.

* **Una base de datos**. Solo ha sido testeada la versión **MySQL 5.7**, no esta garantizado que en otras versiones (p.ej. PostgreSQL) funcione. [Instalar MySQL 5.7 en Debian]().

* **Sphinx**: La versión 2.1.4 funciona correctamente, las nuevas versiones podrían funcionar igual de bien. Asegurate de activar el soporte MySQL. [Instalar Sphinx en Debian]().

* **Imagemagick**: Lo instalamos de la siguiente manera: `sudo apt-get install imagemagick`.

**Parte II. Configurando el entorno de de desarrollo**
