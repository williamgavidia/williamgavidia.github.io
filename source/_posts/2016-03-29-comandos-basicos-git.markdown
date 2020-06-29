---
layout: post
title:  "Git Comandos Basicos"
date:   2016-03-29 15:46:52
comments: true
author: William Gavidia
categories: git
---
<br>
<img src="../../../images/Git-Logo.png" class="center" />
<br>
<br>
[Git][git] es un sistema de `control de versiones` distribuido y es muy usado en el mundo informatico, en este post mencionaremos algunos <strong>comandos Git</strong>  muy útiles al momento de utilizar este controlador de versiones.


A continuación vamos a ver algunos de los comandos Git que no debes dejar de usar:
<br><br>


# 1. GIT COMMIT –AMEND 
<br>
Sirve para modificar el log de un commit, por ejemplo imagínate que escribiste mal un commit, y con este comando tienes la oportunidad de corregirlo.

Modificando el log del último commit que hayamos realizado:<br><br>

```shell-session
git commit --amend
```


Luego podremos editar el último commit y si deseamos corregir algún error que hayamos cometido.<br><br>

# 2. GIT MERGE –ABORT
<br>
Sirve para <strong>abortar un merge</strong> en curso, se usa para deshacer un merge fallido, lo que quiere decir es que solo puedes abortar un merge y regresar todo a la normalidad cuando el merge ha fallado y tiene conflictos.<br><br>


```shell-session
git merge --abort 
```



# 3. GIT BRANCH
<br>
Sirve para crear, listar, eliminar ramas y algunas opciones más.<br><br>

Creando una rama local:


```shell-session
git branch nombre_rama
```



Listando ramas locales:

```shell-session
git branch
```



Listando ramas remotas:

```shell-session
git branch -r
```



Eliminando una rama local:

```shell-session
git branch -d nombre_rama
```



Forzar la eliminación de una rama local:

```shell-session
git branch -D nombre_rama
```



Cambiar de nombre a una rama local, estando en la misma rama:

```shell-session
git branch -m nombre_nuevo
```



Cambiar de nombre a una rama local, estando en otra rama:

```shell-session
git branch -m nombre_anterior nombre_nuevo
```



# 4. GIT STASH
<br>
Sirve para <strong>guardar</strong>  el estado actual de tus cambios sin tener que realizar un commit en tu proyecto, al usarlo regresas el puntero hacia el ultimo commit realizado como si nada hubiera pasado.
Asi los cambios que realizaste se han guardado en una rama temporal de `Git` y los puedes recuperar cuando desees con los comandos: <strong>“git stash apply”</strong>  o <strong>“git stash pop”</strong> .<br><br>

Guardando o escondiendo mis cambios:

```shell-session
git stash
```


Recuperando mis cambios guardados o escondidos anteriormente:

```shell-session
git stash apply
```


# 5. GIT TAGS
<br>
Git tiene la habilidad de etiquetar (<strong>tag</strong>) puntos específicos o importantes en la historia.
Generalmente la gente usa esta funcionalidad para marcar puntos donde se ha lanzado alguna versión (<strong>v1.0, y así sucesivamente</strong>).<br><br>

Listando tus etiquetas (<strong>lo hace alfabéticamente por defecto</strong> ):

```shell-session
git tag
```


Buscando una etiqueta de acuerdo a un patrón en particular:

```shell-session
git tag -l 'v7.3.*'
```


Creando una nueva etiqueta:

```shell-session
git tag -a v1.0.0 -m "CU: Agregando la Tipografia"
```


Enviando una etiqueta al servidor:

```shell-session
git push origin tag v1.0.0
```


# 6. GIT SHOW
<br>
Muestra información de varios tipos de objetos Git.

Mostrando la información del tag `v1.0.0` en forma corta (<strong>-s de short</strong>):

```shell-session
git show v1.0.0 -s
```


# 7. GIT CONFIG
<br>
A través de este comando podemos leer y escribir las configuraciones de Git para el sistema, por usuario y/o por repositorio.<br><br>

Definiendo el nombre con que será identificado la persona que realiza los commits:

```shell-session
git config --global user.name "Wuilliam Gavidia"
```


Definiendo el email del commiter:

```shell-session
git config --global user.email "zerpaw@gmail.com"
```


Definiendo el `editor de texto` con el que trabajará Git (en este caso elijo [Vim][vim]):

```shell-session
git config --global core.editor vim
```


Definiendo [Meld][meld] como herramienta para la solución de conflictos en un merge:

```shell-session
git config --global merge.tool meld
```


Definiendo el alias `“st”` para Git:

```shell-session
git config --global alias.st status
```


Con esto he definido el alias `“st”`, para que en vez de escribir:

```shell-session
git status
```


Tan solo escriba:

```shell-session
git st
```


Espero que de verdad les sirva de algo estos comando [Git][git], son pocos pero realmente valiosos, estoy seguro de que te servirán mas de uná vez. Suerte!!!

[git]:      https://git-scm.com/
[vim]:      http://www.vim.org/
[meld]:     http://meldmerge.org/om/
