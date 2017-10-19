<p align="center">
  <img src="https://github.com/fermarval/fermarval.github.io/blob/master/images/sharetribetittle.png">
</p>

Sharetribe es una plataforma sotware de código abierto para crear tu propio marketplace online con el espitirú de Airbnb, Uber o eBay.

El software de Sharetribe facilita que cualquiera pueda crear su propia plataforma de marketplace en línea en un día, incluso sin habilidades técnicas. Puede ser utilizado por coopeartivas, asociaciones, individuos propios, startups, ciudades y municipios, entre otros. El software es actualmente el más adecuado para crear marketplaces entre iguales (P2P), como Airbnb o eBay, donde las personas intercambian bienes o servicios, pero también pueden usarse para crear mercados B2C, donde pequeños proveedores profesionales ofrecen sus servicios a sus clientes.

El software de Sharetribe es mantenido y desarrollado principalmente por Sharetribe Ltd. El modelo comercial de la compañia es similar al que ofrece Automattic, la empresa que desarrolla WordPress. La compañia ofrece alojamiento del software para aquellos que no desean tocar el código en absoluto, cobrando una tarifa mensual por el servicio de alojamiento. Por otro lado, está la versión código libre, sin coste y disponible para que cualquiera se la descargue e instale en su propio host, como haremos a continuación.

**1. Clonamos el repósito desde Github**
Para ello necesitaremos tener Git instalado antes:
```
sudo apt-get install git-core
```
Nos situamos en la carpeta del usuario (/home/TU-USUARIO) y clonamos el repósito:
```
git clone git://github.com/sharetribe/sharetribe.git
cd sharetribe
```
Dentro de la carpeta de Sharetribe realizaremos los siguientes pasos.

**2. Instalamos requisitos previos necesiarios**
```
sudo apt-get install curl dirmngr imagemagick npm
```

**3. Instalamos NodeJS**
La versión que he necesitado de NodeJS es la 7.8, otras versiones inferiores dan problemas a la hora de instalar.

Vamos a utilizar NVM para instalar/cambiar de versión de NodeJS:
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.5/install.sh | bash
```
Y luego:
```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"
```
Comprobamos que tenemos NVM correctamente instalado:
```
command -v nvm
```
Si aparece por consola la versión de NVM, está correcto.

Ahora, instalamos la versión 7.8 de NodeJS:
```
nvm install 7.8
```
Esperamos a que se instale correctamente.

**4. Instalamos Sphinx**
Realizamos la instalación con los siguientes comandos.
```
sudo apt-get install libmysqlclient20 libodbc1 libpq5
wget http://sphinxsearch.com/files/sphinxsearch_2.2.11-release-1~xenial_amd64.deb
sudo dpkg -i sphinxsearch_2.2.11-release-1~xenial_amd64.deb
```

**5. Instalamos Ruby**
Para facilitar el trabajo, instalaremos RVM (Ruby Version Manager), una herramienta que nos permitirá instalar y cambiar diferentes versiones de Ruby.

Importamos las claves GPG:
```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```
Instalamos la versión Ruby 2.3.4:
```
source ~/.rvm/scripts/rvm
rvm install 2.3.4
```
Esperamos mientra se descarga y compila, puede tardar un poco.

Nos aseguramos de que usamos la versión 2.3.4:
```
rvm use 2.3.1

```

**6. Instalamos las Gems requeridas**
Primero, necesitas instalar un par de dependencias:
```
sudo apt-get install libxslt-dev libxml2-dev
sudo apt-get install libmysqlclient-dev -y
```
Instalamos la Gem bundle:
```
gem install bundler
```
Iniciamos la instalación:
```
bundle install
```

**7. Instalamos los modulos de NodeJS**
Simplemente ejecuta:
```
npm install
```

**8. Instalamos y configuramos MySQL**
Procedemos a instalar la versión 5.7, en el caso de que no la tengas aún:

Creamos el archivo `database.yml` copiando el archivo de configuración de la base de datos de ejemplo:
```
cp config/database.example.yml config/database.yml
```
Añadimos los detalles de la configuración de la base de datos en el archivo: `nano config/database.yml`.

**9. Preparemos Sharetribe para la versión de producción**
Genera tu key secreta:
```
rake secret
```
Creamos el archivo `config.yml` copiando el archivo de configuración de ejemplo:
```
cp config/config.example.yml config/config.yml
```




En desarrollo...
