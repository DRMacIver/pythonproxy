===========
pythonproxy
===========

pythonproxy runs a given python command against whatever version of python you like.

If that version is not installed, it uses `pyenv <https://github.com/yyuu/pyenv>`_'s installer plugin to first install it and *then* run against
that python version.

Usage is:

.. code:: bash

  pythonproxy <exact version> <any sequence of arguments that python version can take>

e.g.:

.. code:: bash

  david@laser-shark:~/projects/pythonproxy$ ./pythonproxy 3.5.0
  Python 3.5.0 (default, Oct 26 2015, 09:27:25) 
  [GCC 4.9.2] on linux
  Type "help", "copyright", "credits" or "license" for more information.
  >>> 


FAQ
---

Why?
~~~~

Because I got bored of the dance of managing many different python versions. pyenv is great for certain
workflows, but I've found that for my common workflows involving managing lots of different pythons it's
mostly annoying.

In particular "which python am I running at the moment?" is a tedious game and I'd much rather just explicitly
specify the python version each time.

Its installer infrastructure though is *great*. So I've been using it in a lot of places. This basically wraps
that usage pattern up into a single script.

Should I use it?
~~~~~~~~~~~~~~~~

¯\\_(ツ)_/¯

It works for me, but it's not very well tested (some manual testing, no automated tests) and is probably
about as inappropriate for your workflow as pyenv ended up being for mine.

Also it's written in bash, and running other people's bash scripts is always a fraught endeavour. No promises
that it won't delete your hard drive.

How do I use it?
~~~~~~~~~~~~~~~~

Ideally: Very carefully.

In practice: Just stick pythonproxy on your path somewhere. You'll need to make sure bash and git are both
installed, but it should otherwise work.

What platforms are supported?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

My laptop. Maybe my Travis CI infrastructure.

But it will probably work on any vaguely unixish system.
