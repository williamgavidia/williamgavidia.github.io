---
layout: post
title:  "Instalación de Git"
date:   2016-04-02 19:46:52
comments: true
author: William Gavidia
categories: git
---
<br>
![Git](../../../images/Git-Logo.png)

<br>
<br>
[Git][git]  es un sistema de control de versiones distribuido y diseñado para manejar todo tipo de proyectos, desde pequeños hasta muy grandes con gran velocidad y eficiencia.
Y por si fuera poco es libre y de código abierto.<br><br>

A continuación veremos como instalar Git:<br><br>


# Instalando Git
<br>
 A continuación quiero guiarles paso a paso como instalarlo. Puedes obtenerlo de varias maneras; las dos principales son instalarlo desde <strong>código fuente</strong>, o instalar un <strong>paquete</strong> existente para tu plataforma.<br><br>

### Instalando desde código fuente
<br>
Para instalar Git, necesitas tener las siguientes librerías de las que Git depende: curl, zlib, openssl, expat y libiconv. Por ejemplo, si estás en un sistema que tiene yum (como <strong>Fedora</strong> ) o apt-get (como un sistema basado en <strong>Debian</strong>), puedes usar estos comandos para instalar todas las dependencias:<br>


```shell-session
$ yum install curl-devel expat-devel gettext-devel \
  openssl-devel zlib-devel
```

```shell-session
$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \
  libz-dev libssl-dev
```

<br>

### Instalando en Linux
<br>

Si quieres instalar Git en Linux a través de un instalador binario, en general puedes hacerlo a través del gestor de paquetes que trae tu distribución.<br><br>


#### Fedora
```shell-session
$ yum install git (Hasta Fedora 21)
```

o

```shell-session
$ dnf install git (Fedora 22 y posteriores)
```

<br>

#### Debian/Ubuntu
```shell-session
$ apt-get install git
```

<br>

#### Gentoo


```shell-session
$ emerge --ask --verbose dev-vcs/git
```


<br>

#### Arch Linux

```shell-session
$ pacman -S git
```

<br>

#### openSUSE
```shell-session
$ zypper install git
```

<br>

#### FreeBSD


```shell-session
$ cd /usr/ports/devel/git
```


```shell-session
$ make install
```

<br>

#### Solaris 11 Express

```shell-session
$ pkg install developer/versioning/git
```

<br>

#### OpenBSD
```shell-session
$ pkg_add git
```

<br>

[git]:      https://git-scm.co
[windows]:      http://www.microsoft.com/en-us/windows
[Download]:      https://git-scm.com/download/win