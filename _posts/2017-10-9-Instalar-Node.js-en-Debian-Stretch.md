<p align="center">
  <img src="http://d3gnp09177mxuh.cloudfront.net/tech-page-images/nodejs.png">
  <img src="http://www.omgubuntu.co.uk/wehelp/images/dah.png">
</p>

Al igual que el articulo de instalación de Ruby, esta entrada viene a raiz de la instalación de Sharetribe, por lo que realizaremos una instalación de la versión compatible para ese sistema. Mientras estoy escribiendo este articulo, la versión que aparece como válida es la  de *Node.js 6.9*, es recomendable echar un vistazo antes a la página de [requerimientos](https://github.com/sharetribe/sharetribe#installation) primero.

* Antes de nada, nos aseguramos de tener instalado cURL:
(Si vienes de instalar Ruby, este paso te lo puedes saltar)
```
sudo apt install curl
```

* Descargamos las dependencias necestarias e instalamos seguidamente Node.js:
```
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
sudo apt install -y nodejs
```

* Instalamos también herramientas de compilación:
```
sudo apt install -y build-essential
```
