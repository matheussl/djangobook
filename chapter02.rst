======================
Cap�tulo 2: Come�ando
======================

Instalar o Django � um processo de v�rios passos, em fun��o das m�ltiplas partes que
envolve os cen�rios de desenvolvimento web hoje em dia. Neste cap�tulo, vamos leva-los atrav�s de 
como se instalar o framework e as suas dependencias.

Como o Django � "apenas" c�digo Python, ele � executado em qualquer lugar que rode Python -- incluindo
alguns telefones celulares! Mas este cap�tulo abrange apenas os cen�rios comums para se 
instalar o Django. Vamos assumir que voc� esteje instalando em uma m�quina desktop/laptop ou um servidor.

Depois, no Cap�tulo 12, n�s iremos cobrir como fazer o deploy do Django para um site em produ��o.

Instalando o Django
====================

Django � puramente escrito em Python, ent�o o primeiro passo para instalar o 
framework � ter certeza de que voc� tem o Python instalado.

Vers�es do Python
------------------

O n�cleo do framework Django (vers�o 1.4) trabalha com qualquer vers�o do Python da 2.5
at� a 2.7. O GIS(Geographic Information Systems) do Django exige o Python 2.5 at� o 2.7.

Se voc� n�o tem certeza da vers�o do Python que que tem instalada e voc� tem
completa liberdade para tomar essa decis�o, escolha a �ltima vers�o da s�rie 2.x: vers�o 2.7.
Embora Django funcione igualmente bem com qualquer vers�o 2.5 at� 2.7, a ultima 
vers�o do Python tem boa performace de desempenho e idiomas adicionais
caracter�sticas que talvez voc� deseje ultilizar em suas aplica��es. Al�m disso, 
add-ons de terceiros que voc� possa querer ultilizar talvez nescessite da mais recente que 
o Python 2.5, ent�o ultilize a ultima versnao do Python mantendo o leque de op��es em aberto.

.. admonition:: Django and Python 3.0

    No momento em que este livro estava sendo escrito, o Python 3.0 estava sendo lan�ado, mas Django
    foi testado apenas de experimentalmente. Python 3.0 intruduziu a 
    um n�mero substancial de incompatibilidades com as vers�es anteriores, mundando 
    a si mesmo, e, como resultado, muita das principais bibliotecas Python e
    frameworks, incluindo Django, ainda n�o tinha pego.

    Django 1.5 dar� suporte para o Python 2.6, 2.7, e 3.2. Entretando,
    suporte para o Python 3.2 � considerado um "preview", o que significa que
    os desenvolvedores Django n�o est�o confiantes o suficiente para prometer
    estabilidade da produ��o. Para isso sugiro que voc� espere at� a vers�o do Django 1.6 

Instala��o
-----------

Se voc� estiver no Linux ou no Mac OS X, voc� provavelmente tem o Python instalado.
Escreva ``python`` no prompt de comando (ou em Applications/Utilities/Terminal, no Mac OS X).
Se voc� v� algo como isso, � porque o Python est� instalado::

    Python 2.7.3rc2 (default, Apr 22 2012, 22:30:17)
    [GCC 4.6.3] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

Caso contr�rio, voc� prescisa fazer o download e instalar o Python. Isso � f�cil e r�pido
instru��es detalhadas poder�o ser encontradas em http://www.python.org/download/

Instalando Django
=================

Em um determinado momento, duas dinstintas vers�es dinstintas do Django est�o dispon�veis para voc�:
a �ltima vers�o oficial e a vers�o de desenvolvimento. A vers�o que voc� decidir instalar 
depende das suas prioridades. Se voc� quer uma vers�o testada e est�vel, ou se voc� quer uma
vers�o contendo os recursos mais recentes. Talvez voc� possa contribuir para o Django, � custa de
estabilidade?

N�s recomendamos trabalhar com um lan�amento oficial, mas � importante saber que a vers�o 
de desenvolvimento existe, porque voc� ir� encontrar men��es na documenta��o e pelos 
membros da comunidade.

Instalando um lan�amento oficial
------------------------------

Um lan�amento oficial tem um n�mero de vers�o, como 1.4.2, 1.4.1 ou 1.4, 
um lan�amento n�o oficial tem um n�mero de vers�o, como 1.4.2, 1.4.1 ou 1.4, e a �ltima 
estar� sempre dispon�vel em http://www.djangoproject.com/download/.

Se voc� est� em uma distribui��o Linux que inclui um pacote do Django, � uma boa ideia
usar a vers�o do distribuidor. Dessa forma voc� ter� atualiza��es de seguran�a juntamente com
o resto dos pacotes do seu sistema.

Se voc� n�o tem acesso a uma vers�o pr�-empacotada, voc� pode fazer o download e instalar
o framework manualmente. Para isso, primeiramente fa�a o do tarball, que ser� chamado
de algo como ``Django-1.4.2.tar.gz``. (N�o importa em qual diret�rio local voc� tenha baixado
este arquivo inicial; O processo de instala��o colocar� os arquivos do Django no lugar correto.) 
Ent�o, descompacte-o e e execute ``setup.py install``, como voc� faz com a maioria das bibliotecas
do Python.

Veja como esse processo se parece em sistemas Unix:

#. ``tar xzvf Django-1.4.2.tar.gz``
#. ``cd Django-*``
#. ``sudo python setup.py install``

No Windows, n�s recomendamos o uso do 7-Zip (http://www.djangoproject.com/r/7zip/)
para descomprimir os arquivos ``.tar.gz``. Uma vez com os arquivos descompactados, inicie o DOS
shell (o "Prompt de Comando") com os privil�gios de administrador e execute o comando seguinte 
dentro do diret�rio cujo nome come�a com ``Django-``::

    python setup.py install

No caso de voc� estiver curioso: os arquivos do Django ser�o instalados no local da
instala��o do seu Python no ``site-packages`` diret�rio -- um diret�rio aonde o o Python
procura por biblioteca de terceiros. Normalmente � um lugar como ``/usr/lib/python2.7/site-packages``.

Instalando a vers�o de "Desenvolvimento"
----------------------------------------

Django ultiliza o Git (http://git-scm.com) para o controle de vers�o. A mais
recente e maior vers�o de desenvolvimento do Django se encontra no seu oficial 
reposit�rio do Git (https://github.com/django/django). Voc� deve considerar a 
instala��o dessa vers�o se voc� quer trabalhar on the bleeding edge, ou se voc� quiser 
contribuir com o c�digo do Django.

Git � gratu�to, um uma distribui��o de c�digo live de revis�o de controle de sistema, e o
time do Django usa ele para controlar as mudan�as no c�digo fonte do Django. Voc� pode fazer
o download e instalar o Git no http://git-scm.com/download, mas � mas f�cil instalar com
o controlador de pacots do seu sistema operacional. Voc� pode usar o Git para pegar a mais 
recente vers�o dos c�digos do Django e, a qualquer momento, voc� pode atualizar os c�digos 
da sua vers�o local do Django para obter as �ltimas altera��es feitas pelos os desenvolvedores
Django.

Ao usar a vers�o de desenvolvimento, tenha em mente que n�o h� coisas como garantias de que
n�o ser� quebrada a qualquer momento. Como dito, alguns membros do time do Django executa sites
de produ��o em vers�es de desenvolvimento, para que eles tenham um incentivo de mant�-los est�veis.

Para pegar a �ltima vers�o do Django, siga esses passos:

#. Tenha certeza que voc� tenha o Git instalado. Voc� pode peg�-lo gratuitamente em http://git-scm.com/,
e voc� pode achar a excelente documenta��o em http://git-scm.com/documentation.

#. Clone o reposit�rio usando o seguinte comando ``git clone https://github.com/django/django djmaster``

#. Localize na instala��o do Python o diret�rio ``site-packages``. Normalmente
   fica localizada em um lugar como ``/usr/lib/python2.7/site-packages``. Se voc� n�o faz id�ia,
   escreva isso no prompt de comando::

       python -c 'import sys, pprint; pprint.pprint(sys.path)'

    A sa�da resultante dever� incluir o diret�rio do seu ``site-packages``.

#. Dentro do diret�rio ``site-packages``, crie um arquivo chamado ``djmaster.pth``
  e edite ele para conter o caminho completo para o seu diret�rio ``djmaster``.
  Por exemplo, o arquivo poderia conter essa linha::

       /path/to/djmaster

#. Coloque ``djmaster/django/bin`` em seu PATH do sistema. Este diret�rio inclui
   inclui utilit�rios de administra��o, tais como o ``django-admin.py``.

.. admonition:: Dica:

    Se arquivos ``.pth`` s�o novos para voc�, voc� pode aprender mais sobre eles em
    http://www.djangoproject.com/r/python/site-module/.

Depois de baixar pelo Git e seguir os passos anteriores, n�o h� nescessidade de 
executar ``python setup.py install``-- voc� acabou de fazer o trabalho manualmente!

Como o c�digo do Django muda frequentemente com corre��o de bugs e ad��o de recurso,
voc� provavelmente queira atualiza-lo de vez em quando. Para atualizar o c�digo, 
apenas execute o comando ``git pull origin master`` dentro do diret�rio ``djmaster``.
Quando voc� executar o comando, o Git entrar� em contato com https://github.com/django/django,
determinando se algo c�digo fonte foi mudado, e atualizando a sua vers�o local com as altera��es
que tem sido feitas desde o �ltimo update. It's quite slick.

Finalmente, se voc� usa a vers�o de desenvolvimento do Django, voc� deve saber como 
qual a vers�o do Django est� sendo executada. Conhecer o n�mero da sua vers�o ser� importante
se voc� nescessitar correr at� a comunidade para ajuda, ou se voc� apresentar melhorias 
para o framework. Nestes casos, voc� dever� dizer as pessoas que revisionam, tamb�m conhecido como "commit", 
o que voc� est� usando. Para saber o seu atual "commit", digite "git log -1" de dentro de um diret�rio ``django``, e 
olhe para os identificadores depois de "commit". Este n�mero muda toda vez que o Django � alterado,
seja por meio de uma corre��o de bug, adi��o de funcionalidade, documenta��o ou melhoria de qualquer coisa.

Testando a instala��o do Django
================================

Para um feedback positivo de p�s instala��o, pare um instante para ver se a instala��o
est� funcionando. Em um shell de comando, mude para outro diret�rio (ex., *n�o* o diret�rio que que
cont�m o diret�rio ``django``) e inicie o interpretador interativo Python digitando ``python``. Se a 
instala��o obteve exito, voc� podera importar o m�dulo ``django``:

    >>> import django
    >>> django.VERSION
    (1, 4, 2, 'final', 0)

.. admonition:: Exemplos do Interpretador Interativo

    O interpretador interativo do Python � um programa de linha de comando que permite que voc� escreva
    um programa Python interativamente. Para inicializa-lo, execute o comando ``python`` na linha de comando.

    Ao longo desse livro, apresentamos exemplos em sess�es no interpretador interativo do Python. Voc� poder�
    reconhecer esses exemplos pelos tr�s sinais de maior qu� (``>>>``), que designam o interpretador no prompt. Se
    voc� est� copiando exemplos deste livro, n�o copie estes sinais de maio-qu�.

    Declara��es de v�rias linhas nesse interpretador interativo s�o preenchidos com tr�s pontos (``...``). Por exemplo::

        >>> print """This is a
        ... string that spans
        ... three lines."""
        This is a
        string that spans
        three lines.
        >>> def my_function(value):
        ...     print value
        >>> my_function('hello')
        hello

    Esses tr�s pontos no inicio de linhas adicionais s�o inseridas pelo shell do Python -- eles n�o s�o parte
    daquilo que est� sendo inserido. N�s incluimos aqui para ser fiel a sa�da real do interpretador. Se voc� copiar
    estes exemplos para acompanhar, n�o copie estes pontos.

Configurando um Banco de Dados
===============================

Neste ponto, voc� pode muito bem come�ar a escrever uma aplica��o web com o Django, 
porque os pr�-requisitos r�pidos do Django � apenas estar trabalhando com uma instala��o do Python.
No entanto, as probabilidades de que voc� ir� desenvolver um Web site com um *banco de dados dirigido*, 
neste caso, voc� nescessitar� de configurar um servidor de banco de dados.

Se voc� apenas quer come�ar a jogar com o Django, pule para a se��o "Come�ando um Projeto" --
mas tenha em mente que todos os exemplos desse livro asumme que voc� tenha trabalhado configurado
um banco de dados.

Django suporta quatro tipo de banco de dados

* PostgreSQL (http://www.postgresql.org/)
* SQLite 3 (http://www.sqlite.org/)
* MySQL (http://www.mysql.com/)
* Oracle (http://www.oracle.com/)

Para a maior parte, todos esses bancos de dados trabalham igualmente bem com o n�cleo do Django framework.
(Uma not�vel excess�o � o opcional GIS suporte ao Django, que � muito mais poderoso que o PostgreSQL do que 
com outros bancos de dados.) Se voc� n�o estiver amarrado a nenhum sistema legado e tem a liberdade para 
escolher o banco de dados, n�s recomendamos PostgreSQL, que alcan�a um bom equilibrio entre custo, recurso, 
velocidade e estabilidade.

Configurar o banco de dados � um processo de duas etapas:

* Primeiro, voc� prescisa instalar e configurar servidor de banco de dados em si.
  Este processo est� al�m do escopo desse livro, mas cada um dos quatro banco de dados
  tem uma rica documenta��o em seus pr�prios websites. (Se, voc� est� em um servidor
  de hospedagem compartilhado, provavelmente eles ir�o definiram isso para voc�.)

* Segundo, voc� prescisa instalar a biblioteca Python para o seu banco de dados em particular. 
  Isso � um pouco de c�digo de terceiros que permite ao Python se comunicar com o banco de dados.
  N�s delineamos especificamente, por requerimentos de banco de dados nas se��es seguintes.

Se voc� est� apenas brincando um pouco com o Django e n�o quer instalar um servidor de 
banco de dados, considere ent�o usar o SQLite. SQLite � o unico na lista de banco de dados suportados
� o �nico que n�o requere nenhum dos passos citados acima. Ele se limita em ler e escrever informa��es
em um �nico arquivo em seu sistema, e a vers�o 2.5 do Python ou superior inclui um suporte nativo para ele.

No Windows, a obten��o de drives bin�rios do banco de dados pode ser algo frustante. Se voc� est� ansioso para
saltar, n�s recomendamos o uso do Python 2.7 e seu suporte nativo para o SQLite.

Usando Django com o PostgresSQL
--------------------------------

Se voc� esta usando o PostgreSQL, voc� nescessita instalar o pacote ``psycopg`` ou o ``psycopg2`` 
pelo endere�o http://www.djangoproject.com/r/python-pgsql/. N�s recomendamos ``psycopg2``, como � mais novo, 
mais ativamente desenvolvido e pode ser f�cilmente instalado. De qualquer forma, tome nota da vers�o que 
voc� est� ultilizando, a vers�o 1 ou a 2; voc� ir� nescessitar dessa informa��o posteriormente.

Se voc� est� usando o PostgreSQL no Windows, se pode achar um precompilador de bin�rios do ``psycopg``
no http://www.djangoproject.com/r/python-pgsql/windows/.

Se voc� estiver no Linux, verifique se a sua distribui��o de gerenciamento de pacotes sistemas ofere�e
um pacote chamado "python-psycopg2", "psycopg2-python", "python-postgresql" ou alguma coisa similar.

Usando Django com o SQLite 3
--------------------------

You're in luck: no database-specific installation is required, because Python
ships with SQLite support. Skip ahead to the next section.

Using Django with MySQL
-----------------------

Django requires MySQL 4.0 or above. The 3.x versions don't support nested
subqueries and some other fairly standard SQL statements.

You'll also need to install the ``MySQLdb`` package from
http://www.djangoproject.com/r/python-mysql/.

If you're on Linux, check whether your distribution's package-management system
offers a package called "python-mysql", "python-mysqldb", "mysql-python" or
something similar.

Using Django with Oracle
------------------------

Django works with Oracle Database Server versions 9i and higher.

If you're using Oracle, you'll need to install the ``cx_Oracle`` library,
available at http://cx-oracle.sourceforge.net/. Use version 4.3.1 or higher, but
avoid version 5.0 due to a bug in that version of the driver.  Version 5.0.1
resolved the bug, however, so you can choose a higher version as well.

Using Django Without a Database
-------------------------------

As mentioned earlier, Django doesn't actually require a database. If you just
want to use it to serve dynamic pages that don't hit a database, that's
perfectly fine.

With that said, bear in mind that some of the extra tools bundled with Django
*do* require a database, so if you choose not to use a database, you'll miss
out on those features. (We highlight these features throughout this book.)

Starting a Project
==================

Once you've installed Python, Django and (optionally) your database
server/library, you can take the first step in developing a Django application
by creating a *project*.

A project is a collection of settings for an instance of Django, including
database configuration, Django-specific options and application-specific
settings.

If this is your first time using Django, you'll have to take care of some
initial setup. Create a new directory to start working in, perhaps something
like ``/home/username/djcode/``.

.. admonition:: Where Should This Directory Live?

    If your background is in PHP, you're probably used to putting code under the
    Web server's document root (in a place such as ``/var/www``). With Django,
    you don't do that. It's not a good idea to put any of this Python code
    within your Web server's document root, because in doing so you risk the
    possibility that people will be able to view your raw source code over the
    Web. That's not good.

    Put your code in some directory **outside** of the document root.

Change into the directory you created, and run the command
``django-admin.py startproject mysite``. This will create a ``mysite``
directory in your current directory.

.. note::

    ``django-admin.py`` should be on your system path if you installed Django
    via its ``setup.py`` utility.

    If you're using the development version, you'll find ``django-admin.py`` in
    ``djmaster/django/bin``. Because you'll be using ``django-admin.py``
    often, consider adding it to your system path. On Unix, you can do so by
    symlinking from ``/usr/local/bin``, using a command such as ``sudo ln -s
    /path/to/django/bin/django-admin.py /usr/local/bin/django-admin.py``. On
    Windows, you'll need to update your ``PATH`` environment variable.

    If you installed Django from a packaged version for your Linux
    distribution, ``django-admin.py`` might be called ``django-admin`` instead.

If you see a "permission denied" message when running
``django-admin.py startproject``, you'll need to change the file's permissions.
To do this, navigate to the directory where ``django-admin.py`` is installed
(e.g., ``cd /usr/local/bin``) and run the command ``chmod +x django-admin.py``.

The ``startproject`` command creates a directory containing five files::

    mysite/
        manage.py
        mysite/
            __init__.py
            settings.py
            urls.py
            wsgi.py

.. note:: Doesn't match what you see?

    The default project layout recently changed. If you're seeing a
    "flat" layout (with no inner ``mysite/`` directory), you're probably using
    a version of Django that doesn't match this tutorial version. This book covers
    Django 1.4 and above, so if you're using an older version you probably want to
    consult Django's official documentation.

    The documentation for Django 1.X version is available at https://docs.djangoproject.com/en/1.X/.

These files are as follows:

* ``mysite/``: The outer ``mysite/`` directory is just a container for your project.
  Its name doesn't matter to Django; you can rename it to anything you like.

* ``manage.py``: A command-line utility that lets you interact with this
  Django project in various ways. Type ``python manage.py help`` to get a
  feel for what it can do. You should never have to edit this file; it's
  created in this directory purely for convenience.

* ``mysite/mysite/``: The inner ``mysite/`` directory is the actual Python package
  for your project. Its name is the Python package name you'll need to use to
  import anything inside it (e.g. ``import mysite.settings``).

* ``__init__.py``: A file required for Python to treat the ``mysite``
  directory as a package (i.e., a group of Python modules). It's an empty
  file, and generally you won't add anything to it.

* ``settings.py``: Settings/configuration for this Django project. Take a
  look at it to get an idea of the types of settings available, along with
  their default values.

* ``urls.py``: The URLs for this Django project. Think of this as the
  "table of contents" of your Django-powered site.

* ``wsgi.py``: An entry-point for WSGI-compatible webservers to serve your project.
  See How to deploy with WSGI (https://docs.djangoproject.com/en/1.4/howto/deployment/wsgi/) for more details.

Despite their small size, these files already constitute a working Django
application.

Running the Development Server
------------------------------

For some more post-installation positive feedback, let's run the Django
development server to see our barebones application in action.

The Django development server (also called the "runserver" after the command
that launches it) is a built-in, lightweight Web server you can use while
developing your site. It's included with Django so you can develop your site
rapidly, without having to deal with configuring your production server (e.g.,
Apache) until you're ready for production. The development server watches your
code and automatically reloads it, making it easy for you to change your code
without needing to restart anything.

To start the server, change into your project container directory (``cd mysite``),
if you haven't already, and run this command::

    python manage.py runserver

You'll see something like this::

    Validating models...
    0 errors found.

    Django version 1.4.2, using settings 'mysite.settings'
    Development server is running at http://127.0.0.1:8000/
    Quit the server with CONTROL-C.

This launches the server locally, on port 8000, accessible only to connections
from your own computer. Now that it's running, visit http://127.0.0.1:8000/
with your Web browser. You might see a different Django version depending on
which version of Django you have installed. You'll see a "Welcome to Django" page shaded in a
pleasant pastel blue. It worked!

One final, important note about the development server is worth mentioning
before proceeding. Although this server is convenient for development, resist
the temptation to use it in anything resembling a production environment. The
development server can handle only a single request at a time reliably, and it
has not gone through a security audit of any sort. When the time comes to
launch your site, see Chapter 12 for information on how to deploy Django.

.. admonition:: Changing the Development Server's Host or Port

    By default, the ``runserver`` command starts the development server on port
    8000, listening only for local connections. If you want to change the
    server's port, pass it as a command-line argument::

        python manage.py runserver 8080

    By specifying an IP address, you can tell the server to allow non-local
    connections. This is especially helpful if you'd like to share a
    development site with other members of your team. The IP address
    ``0.0.0.0`` tells the server to listen on any network interface::

        python manage.py runserver 0.0.0.0:8000

    When you've done this, other computers on your local network will be able
    to view your Django site by visiting your IP address in their Web browsers,
    e.g., http://192.168.1.103:8000/ . (Note that you'll have to consult your
    network settings to determine your IP address on the local network. Unix
    users, try running "ifconfig" in a command prompt to get this information.
    Windows users, try "ipconfig".)

What's Next?
============

Now that you have everything installed and the development server running,
you're ready to :doc:`learn the basics <chapter03>` of serving Web pages with Django.
