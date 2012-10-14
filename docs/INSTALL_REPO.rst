=============================================
Installing python-openzwave from repositories
=============================================

Install the needed tools
========================
You must install mercurial and subversion to get sources of python-openzwave
and openzwave. Look at the documentation of your Linux distribution to do that.

On a debian like distribution :

    sudo apt-get install mercurial subversion

You need cython (0.14 or 0.15) to compile the python library (libopenzwave.pyx).
Some users have reported errors when using 0.16. You also need some python depencies

On a debian like distribution :

    sudo apt-get install cython python-dev python-setuptools python-louie

You need sphinx and make to generate the documentation.

On a debian like distribution :

    sudo apt-get install python-sphinx make

To compile the openzwave library, you need the common builds tools
and the libudev developments headers.

On a debian like distribution :

    sudo apt-get install build-essential libudev-dev g++

Get sources of python-openzwave
===============================

You are now ready to download sources of python-openzwave :

    hg clone https://code.google.com/p/python-openzwave/

The previous command will create a copy of the official repository on your
computer in a directory called python-openzwave.

Update and build process
========================

Go to the previously created directory

	cd python-openzwave

The following command will update your local repository to the last release
of python-openzwave and openzwave.

    ./update.sh

When update process is done you can compile sources

    ./compile.sh

If you have already build python-openzwave in a previous installation, you can
use the clean option to remove old builds.

    ./compile.sh clean

Installation
============

You can now install the packages using the following command will.

    sudo ./install.sh

The installation script create a list of installed files. So you can remove
python-openzwave using the following command :

    sudo ./uninstall.sh