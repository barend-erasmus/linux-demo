# Linux: Demo

Prerequisites:
1. Ubuntu Server 17.04.
2. 'root' user.
3. 'demo' user (No root permissions).
4. Configure SSH keys
4. Login with 'demo' user.

In this document we'll cover:

1. Reading Linux Documentation
2. Connecting to a Linux Machine
    1. Using passwords
    2. Using SSH keys
3. Installing Redis on a Ubuntu Server
4. Installing NGINX on a Ubuntu Server
5. More on APT-GET


## Installing Redis on a Ubuntu Server

`sudo` stands for 'superuser do'

`sudo apt-get update` downloads the package lists from the repositories and "updates" them to get information on the newest versions of packages and their dependencies.

`sudo apt-get install build-essential` installs all the packages needed to compile a debian package. Inlcudes the gcc/g++ compilers.

`sudo apt-get install tcl8.5` installs TCL which is a very powerful dynamic programming language.

`wget http://download.redis.io/releases/redis-stable.tar.gz` downloads the Redis source to our **current/working** directory.

`tar xzf redis-stable.tar.gz` unzip/untar the downloaded file.

We can use `ls` to see the downloaded files.

`cd redis-stable` changes to 'redis-stable' directory.

`make` compiles the source code using the gcc/g++ compilers.

`sudo make install` installs the compiled source by running a TCL script.


## Installing NGINX on a Ubuntu Server

1. `sudo apt-get update`
2. `sudo apt-get install nginx`
3. `sudo ufw allow 'Nginx HTTP'`

## More on APT-GET

NODEJS 7 INSTALLATION