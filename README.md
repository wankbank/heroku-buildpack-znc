Heroku buildpack: ZNC
=====================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) specifically for ZNC.
It's yet another fork of someone elses attempt (that hasn't worked).

Usage
-----

Example usage:

    $ git clone https://github.com/znc/znc.git && cd znc

    $ heroku create --stack cedar --buildpack https://github.com/wankbank/heroku-buildpack-znc.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> C app detected
	-----> Running autogen.sh
    -----> Configuring
    -----> Compiling with Make
           Linking znc...
		   ZNC was successfully compiled.
		
Ultimately the ./configure command would also make install, however, with heroku it fails.
