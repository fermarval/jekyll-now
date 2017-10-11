<p align="center">
  <img src="https://irp-cdn.multiscreensite.com/b3c540b6/dms3rep/multi/tablet/Sharetribe-1279x226.Logo.no-margin.png">
</p>

En desarrollo...

**Parte I. Instalando los requisitos**

* **Ruby**: La versión **2.3.4** es la que actualmente usa, no se garantiza que funcione correctamente con otras versiones. Si necesitas varias versiones de Ruby, se recomienda usar `rvm`. [Instalar Ruby en Debian](https://fermarval.github.io/Instalar-Ruby-en-Debian-Stretch/).

* **RubyGems**: Disponible con la descarga y compilación de Ruby.

* **Bundler**: Lo instalamos de la siguiente manera: `gem install bundler`.

* **Node**: La versión **6.9** es la que actualmente usa, no se garantiza que funcione correctamente con otras versiones. Si necesitas usar diferentes versiones de Node, considera usar `n` or `nvm`. [Instalar Node.js en Debian](https://fermarval.github.io/Instalar-Node.js-en-Debian-Stretch/).

* **Git**: Lo instalamos de la siguiente manera: `sudo apt-get install git-core`.

* **Una base de datos**. Solo ha sido testeada la versión **MySQL 5.7**, no esta garantizado que en otras versiones (p.ej. PostgreSQL) funcione. [Instalar MySQL 5.7 en Debian]().

* **Sphinx**: La versión 2.1.4 funciona correctamente, las nuevas versiones podrían funcionar igual de bien:

```
sudo apt-get install libmysqlclient20 libodbc1 libpq5
wget http://sphinxsearch.com/files/sphinxsearch_2.2.11-release-1~xenial_amd64.deb
sudo dpkg -i sphinxsearch_2.2.11-release-1~xenial_amd64.deb
```

* **Imagemagick**: Lo instalamos de la siguiente manera: `sudo apt-get install imagemagick`.

**Parte II. Configurando el entorno de de desarrollo**

* Vamos a cualquier carpeta donde clonar el repósito, por ejemplo la carpeta de tu usuario:
```
git clone git://github.com/sharetribe/sharetribe.git
cd sharetribe
git checkout latest
```
Con esto último comprobamos que hemos clonado correctamente la ultima versión del repositorio.

* Instalamos el bundle:
```
bundle install
```

* Instalamos los módulos de node:
```
npm install
```
Este proceso suele tardar unos minutos.

* Creamos el archivo `database.yml` copiando el archivo de configuración de la base de datos de ejemplo:
```
cp config/database.example.yml config/database.yml
```

* Añadimos los detalles de la configuración de la base de datos en el archivo `config/database.yml`.

* Creamos el archivo `config.yml` copiando el archivo de configuración de ejemplo:
```
cp config/config.example.yml config/config.yml
```

En desarrollo...
