# What do i need to run PHP?

# Installing PHP on *nix
## Using apt-get

```
sudo apt-get update
```

### Apache Install

```
sudo apt-get install apache2
# Find Your IP Address eth0
ifconfig

# restart apache service
sudo /etc/init.d/apache2 restart
```

### Apache config file httpd.conf
```
$ ps -ef | grep apache
apache   12846 14590  0 Oct20 ?        00:00:00 /usr/sbin/apache2

$ /usr/sbin/apache2 -V | grep SERVER_CONFIG_FILE
-D SERVER_CONFIG_FILE="/etc/apache2/apache2.conf"
```

### Test your browser 
```
http://localhost/
```

### Lets Try how PHP Script works without installing php
```
<?php 
echo "Hello World"; 
?>
```


### MySQL Installation
```
sudo apt-get install mysql-server php5-mysql

# initializes the MySQL data directory and creates the system tables 
# that it contains
sudo mysql_install_db

# Last step
sudo /usr/bin/mysql_secure_installation

By default, a MySQL installation has an anonymous user, allowing anyone
to log into MySQL without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] y                                            
 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] y
... Success!

By default, MySQL comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] y
 - Dropping test database...
 ... Success!
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] y
 ... Success!

Cleaning up...
```

### PHP Installation
```
sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt
```

## Alternate way
Use LAMP in Linux and install it with tasksel easy to go

```
sudo apt-get install tasksel
sudo tasksel install lamp-server
```
## Using PHP Source (from the php src)

```
sudo -i
wget http://in1.php.net/get/php-5.6.13.tar.bz2/from/this/mirror
tar -xvf php-5.6.13.tar.bz2
cd php-5.6.13
./configure
make
make install
```

