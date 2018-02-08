
The packaging scripts for CLBlast
================

This repository contains the packaging scripts for the [CLBlast OpenCL BLAS library](https://github.com/CNugteren/CLBlast). For more information see the CLBlast repository.


Debian
-------------

Debian/Ubuntu packaging is included. A package can be created by running `debuild -us -uc`, e.g. as follows:

    wget -O clblast_1.3.0.orig.tar.gz https://github.com/CNugteren/CLBlast/archive/1.3.0.tar.gz
    tar -xvf clblast_1.3.0.orig.tar.gz
    mv CLBlast-1.3.0/ clblast
    cd clblast
    cp -r ../debian/ .
    debuild -us -uc

The package is uploaded to an Ubuntu PPA: https://launchpad.net/~cnugteren/+archive/ubuntu/clblasts


Brew (OS X)
-------------

To be done.


NuGet (Windows)
-------------

To be done.
