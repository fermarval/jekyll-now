Parte I. Instalando los requisitos

1. **Ruby**. La versión 2.3.4 es la que actualmente se usa, no se garantiza que funcione correctamente con otra versión inferior. Si necesitas varias versiones de Ruby, se recomienda usar **RVM**. [Instalar Ruby en Debian]()

RubyGems
Bundler: gem install bundler
Node. Version 6.9 is currently used and we don't guarantee everything works with other versions. If you need multiple versions of Node, consider using n or nvm.
Git
A database. Only MySQL 5.7 has been tested, so we give no guarantees that other databases (e.g. PostgreSQL) work. You can install MySQL Community Server two ways:
If you are on a Mac, use homebrew: brew install mysql (highly recommended). Also consider installing the MySQL Preference Pane to control MySQL startup and shutdown. It is packaged with the MySQL downloadable installer, but can be easily installed as a stand-alone.
Download a MySQL installer from here
Sphinx. Version 2.1.4 has been used successfully, but newer versions should work as well. Make sure to enable MySQL support. If you're using OS X and have Homebrew installed, install it with brew install sphinx --with-mysql
Imagemagick. If you're using OS X and have Homebrew installed, install it with brew install imagemagick
