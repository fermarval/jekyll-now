```
sudo nano /etc/apt/sources.list.d/mysql.list
```

Y escribir:
```
deb http://repo.mysql.com/apt/debian/ stretch mysql-5.7
deb-src http://repo.mysql.com/apt/debian/ stretch mysql-5.7
```

```
wget -O /tmp/RPM-GPG-KEY-mysql https://repo.mysql.com/RPM-GPG-KEY-mysql
sudo apt-key add /tmp/RPM-GPG-KEY-mysql
```

```
sudo apt-get update
sudo apt-get install mysql-server
```
