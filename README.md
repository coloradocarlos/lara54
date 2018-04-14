# Laravel 5.4 test project (lara54)

# Quick Start

These instructions should work for Mac, WinOS, and Linux. If everything goes according to plan you will not need to install PHP7 or
Composer on your laptop.

By running the code in a pre-packaged VM, we reduce the depencies on the host operating system.

You can find out more about [Laravel Homestead](https://laravel.com/docs/5.4/homestead) on their web site.

## Download Dependencies for your platform

1. Download and install [VirtualBox 5.1](https://www.virtualbox.org/wiki/Downloads)

2. Download and install [Vagrant 1.9.3](https://www.vagrantup.com/downloads.html)

3. Download and install [Git](https://git-scm.com/downloads) or [SourceTree](https://www.sourcetreeapp.com/)

## Git clone the lara54 test repository

[https://github.com/coloradocarlos/lara54](https://github.com/coloradocarlos/lara54)

## Prepare the project directory with your laptop specific directory locations

The following steps are performed from a Cmd prompt in Windows or terminal window on a Mac. Change cp to xcopy in WinOS.

1. `> cd lara54`

2. `> cp .env.example .env`

3. `> cp Homestead.yaml.example Homestead.yaml`

4. Edit Homestead.yaml and change the directories in the file to point to your local file system

## Start Vagrant virtual machine and login to Vagrant VM

Steps below are performed from the host machine.

1. `> vagrant up`

2. `> vagrant ssh`

You will then be logged on to the Homestead instance. The screen should look something like this:

```console
Welcome to Ubuntu 16.04.2 LTS (GNU/Linux 4.4.0-51-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

3 packages can be updated.
0 updates are security updates.


Last login: Wed Apr  5 01:11:23 2017 from 10.0.2.2
vagrant@lara54:~
```

## Install PHP Composer Dependencies

This done from the Vagrant guest machine, not the host!

Change into the project directory, for example, lara54.

1. `$ cd lara54`

2. `$ composer install`

3. `$ php artisan key:generate`

## Start browser and point to Laravel test project

1. [http://localhost:8000](http://localhost:8000)

## Sharing

From Guest machine:

`$ ngrok http 192.168.10.10:80 -host-header=lara54.app`

## Clean-up

From Guest:

1. `$ exit`

From Host:

1. `> vagrant halt`
