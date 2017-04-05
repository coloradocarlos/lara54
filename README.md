# Laravel 5.4 test project (lara54)

# Quick Start

These instructions should work for Mac, WinOS, and Linux. If everything goes according to plan you will not need to install PHP7 or
Composer on your laptop.

## Download Dependencies for your platform

1. Download and install [VirtualBox 5.1](https://www.virtualbox.org/wiki/Downloads)

2. Download and install [Vagrant 1.9.3](https://www.vagrantup.com/downloads.html)

3. Download and install [Git](https://git-scm.com/downloads) or [SourceTree](https://www.sourcetreeapp.com/)

## Git clone the lara54 test repository

[https://github.com/coloradocarlos/lara54](https://github.com/coloradocarlos/lara54)

## Prepare the project directory with your laptop specific directory locations

This is done from a Cmd prompt in Windows or terminal window on a Mac. Change cp to xcopy in WinOS.

1. `> cd lara54`

2. `> cp .env.example .env`

3. `> cp Homestead.yaml.example Homestead.yaml`

4. Edit Homestead.yaml and change the directories in the file to point to your local file system

## Start Vagrant virtual machine and login

1. `vagrant up`

2. `vagrant ssh`

## Install PHP Composer Dependencies

This done from the Vagrant guest machine, not the host!

Change into the project directory, for example, lara54.

1. `$ cd lara54`

2. `$ composer install`

3. `$ php artisan key:generate`

## Start browser and point to Laravel test project

1. [http://localhost:8000](http://localhost:8000)


## Clean-up

From Guest:

1. `$ exit`

From Host:

1. `$ vagrant halt`