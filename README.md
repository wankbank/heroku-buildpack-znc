Heroku buildpack: ZNC
=====================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) specifically for ZNC.
I forked someone elses and it didn't work. I got this nearly working with dokku, but ultimately abandoned it.

It probably won't work, but PRs are welcome.

Usage
-----

Example usage:

    $ git clone git@github.com:znc/znc.git && cd znc

    $ heroku create --stack cedar --buildpack http://github.com/lonnen/heroku-buildpack-znc.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> C app detected
    -----> Configuring
           Looking for somelibrary… ok
    -----> Compiling with Make
           gcc -o myapp myapp.c

The buildpack will detect most apps with a Makefile, but issues commands specific to ZNC. It may work if your app has the same `configure` `make` `make install` set of commands.
