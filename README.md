# Linux: Demo

Prerequisites:
1. Ubuntu Server 17.04.
2. 'root' User.
3. 'demo' User (No root Permissions).
4. Configure SSH keys.
5. Login with 'demo' user.

In this document we'll cover:

1. Reading Linux Documentation
2. Connecting to a Linux Machine
    1. Using passwords
    2. Using SSH keys
3. Installing Redis on a Ubuntu Server
4. Configure Redis as a Service
5. Installing NGINX on a Ubuntu Server
6. More on APT-GET
7. Create a New Linux User
8. Create SSH Key Pair
9. Switching User in Linux


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

`make install` installs the compiled source by running a TCL script.

Redis is now installed. We can test this by running `redis-cli` which should give us an error as their is no instance of Redis running.

To run a Redis instance we need a configuration file which we can create by using 'nano' editor.

`sudo mkdir /etc/redis` create the directory.

`sudo nano /etc/redis/6379.conf` opens/creates the file at '/etc/redis/6379.conf' in 'nano'

If we just wanted to create a file without opening it we could have used `touch /etc/redis/6379.conf`

`redis-server /etc/redis/6379.conf` run Redis Server with the config as a parameter.

## Configure Redis as a Service

## Installing NGINX on a Ubuntu Server

1. `sudo apt-get update`
2. `sudo apt-get install nginx`
3. `sudo ufw allow 'Nginx HTTP'`

## More on APT-GET

NODEJS 7 INSTALLATION

## Create a New Linux User

`sudo useradd -m <username>`

`sudo passwd <username>`

## Create SSH Key Pair

https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2

## Switching User in Linux

`su - <username>`