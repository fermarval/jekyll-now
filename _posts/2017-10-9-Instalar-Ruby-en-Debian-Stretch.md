Esta entrada viene como parte de la instalación de **Sharetribe**, por tanto instalaremos la versión de Ruby que actualmente esta soportada por este sistema de Marketplace. Según la documentación oficial, Sharetribe soporta la vesión 2.3.4, esto puede variar con el tiempo, es recomentable revisar la [página de requerimientos](https://github.com/sharetribe/sharetribe#installation) primero. 

Para facilitar el trabajo, instalaremos [RVM](https://rvm.io/rvm/install) (Ruby Version Manager), una herramienta que nos permitirá instalar y cambiar diferentes versiones de Ruby.

1. Instalamos **curl**  y **dirmngr** (si no lo tenemos ya instalado):

```
sudo apt install curl
```
```
sudo apt install dirmngr
```

2. Importamos las claves GPG:

```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

3. Instalamos la versión Ruby 2.3.4:

```
source ~/.rvm/scripts/rvm
rvm install 2.3.4
```
Esperamos mientra se descarga y compila los paquetes requeridos para la instalación de Ruby 2.3.4, este proceso puede tardar un tiempo que depende de la velocidad del equipo. Una vez que concluya ya estaría la instalación realizada al completo.

4. Comprobamos que **rubygems** esta disponible con la instalación que hemos realizado de Ruby:

```
rvm rubygems current
```

5. Finalmente nos aseguramos de que estamos usando la versión 2.3.4 (si se nos da el caso de que tenemos varias versiones instaladas en el sistema):

```
rvm use 2.3.1
```
