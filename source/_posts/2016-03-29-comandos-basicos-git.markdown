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

{% highlight ruby %}
git commit --amend
{% endhighlight %} <br>


Luego podremos editar el último commit y si deseamos corregir algún error que hayamos cometido.<br><br>

# 2. GIT MERGE –ABORT
<br>
Sirve para <strong>abortar un merge</strong> en curso, se usa para deshacer un merge fallido, lo que quiere decir es que solo puedes abortar un merge y regresar todo a la normalidad cuando el merge ha fallado y tiene conflictos.<br><br>


{% highlight ruby %}
git merge --abort 
{% endhighlight %} <br>



# 3. GIT BRANCH
<br>
Sirve para crear, listar, eliminar ramas y algunas opciones más.<br><br>

Creando una rama local:


{% highlight ruby %}
git branch nombre_rama
{% endhighlight %} <br>



Listando ramas locales:

{% highlight ruby %}
git branch
{% endhighlight %} <br>



Listando ramas remotas:

{% highlight ruby %}
git branch -r
{% endhighlight %} <br>



Eliminando una rama local:

{% highlight ruby %}
git branch -d nombre_rama
{% endhighlight %} <br>



Forzar la eliminación de una rama local:

{% highlight ruby %}
git branch -D nombre_rama
{% endhighlight %} <br>



Cambiar de nombre a una rama local, estando en la misma rama:

{% highlight ruby %}
git branch -m nombre_nuevo
{% endhighlight %} <br>



Cambiar de nombre a una rama local, estando en otra rama:

{% highlight ruby %}
git branch -m nombre_anterior nombre_nuevo
{% endhighlight %} <br>



# 4. GIT STASH
<br>
Sirve para <strong>guardar</strong>  el estado actual de tus cambios sin tener que realizar un commit en tu proyecto, al usarlo regresas el puntero hacia el ultimo commit realizado como si nada hubiera pasado.
Asi los cambios que realizaste se han guardado en una rama temporal de `Git` y los puedes recuperar cuando desees con los comandos: <strong>“git stash apply”</strong>  o <strong>“git stash pop”</strong> .<br><br>

Guardando o escondiendo mis cambios:

{% highlight ruby %}
git stash
{% endhighlight %} <br>


Recuperando mis cambios guardados o escondidos anteriormente:

{% highlight ruby %}
git stash apply
{% endhighlight %} <br>


# 5. GIT TAGS
<br>
Git tiene la habilidad de etiquetar (<strong>tag</strong>) puntos específicos o importantes en la historia.
Generalmente la gente usa esta funcionalidad para marcar puntos donde se ha lanzado alguna versión (<strong>v1.0, y así sucesivamente</strong>).<br><br>

Listando tus etiquetas (<strong>lo hace alfabéticamente por defecto</strong> ):

{% highlight ruby %}
git tag
{% endhighlight %} <br>


Buscando una etiqueta de acuerdo a un patrón en particular:

{% highlight ruby %}
git tag -l 'v7.3.*'
{% endhighlight %} <br>


Creando una nueva etiqueta:

{% highlight ruby %}
git tag -a v1.0.0 -m "CU: Agregando la Tipografia"
{% endhighlight %} <br>


Enviando una etiqueta al servidor:

{% highlight ruby %}
git push origin tag v1.0.0
{% endhighlight %} <br>


# 6. GIT SHOW
<br>
Muestra información de varios tipos de objetos Git.

Mostrando la información del tag `v1.0.0` en forma corta (<strong>-s de short</strong>):

{% highlight ruby %}
git show v1.0.0 -s
{% endhighlight %} <br>


# 7. GIT CONFIG
<br>
A través de este comando podemos leer y escribir las configuraciones de Git para el sistema, por usuario y/o por repositorio.<br><br>

Definiendo el nombre con que será identificado la persona que realiza los commits:

{% highlight ruby %}
git config --global user.name "Wuilliam Gavidia"
{% endhighlight %} <br>


Definiendo el email del commiter:

{% highlight ruby %}
git config --global user.email "zerpaw@gmail.com"
{% endhighlight %} <br>


Definiendo el `editor de texto` con el que trabajará Git (en este caso elijo [Vim][vim]):

{% highlight ruby %}
git config --global core.editor vim
{% endhighlight %} <br>


Definiendo [Meld][meld] como herramienta para la solución de conflictos en un merge:

{% highlight ruby %}
git config --global merge.tool meld
{% endhighlight %} <br>


Definiendo el alias `“st”` para Git:

{% highlight ruby %}
git config --global alias.st status
{% endhighlight %} <br>


Con esto he definido el alias `“st”`, para que en vez de escribir:

{% highlight ruby %}
git status
{% endhighlight %} <br>


Tan solo escriba:

{% highlight ruby %}
git st
{% endhighlight %} <br>


Espero que de verdad les sirva de algo estos comando [Git][git], son pocos pero realmente valiosos, estoy seguro de que te servirán mas de uná vez. Suerte!!!

[git]:      https://git-scm.com/
[vim]:      http://www.vim.org/
[meld]:     http://meldmerge.org/om/
