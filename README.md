
The packaging scripts for CLBlast
================

This repository contains the packaging scripts for the [CLBlast OpenCL BLAS library](https://github.com/CNugteren/CLBlast). For more information see the CLBlast repository. This repository contains packaging scripts maintained by the author of CLBlast. There are also other packages maintained by others:

* Conda: https://github.com/conda-forge/clblast-feedstock
* Archlinux: https://aur.archlinux.org/packages/clblast-git/


Debian
-------------

Debian/Ubuntu packaging is included in the `debian` subfolder. A package can be created by running `debuild -us -uc`, e.g. as follows:

    wget -O clblast_1.5.0.orig.tar.gz https://github.com/CNugteren/CLBlast/archive/1.5.0.tar.gz
    tar -xvf clblast_1.5.0.orig.tar.gz
    mv CLBlast-1.5.0/ clblast
    cd clblast
    cp -r ../debian/ .
    debuild -us -uc

For releasing to the Ubuntu PPA, follow the above steps, and then continue with:

    debuild -k<gpg-key-id> -S  # as found on the Launchpad PPA under "OpenPGP keys"
    dput clblast ../clblast_1.5.0-1ubuntu1_source.changes

The package is uploaded to an Ubuntu PPA: https://launchpad.net/~cnugteren/+archive/ubuntu/clblast


Homebrew (macOS)
-------------

Homebrew packaging for OSX/macOS is included in the `homebrew` folder. This is a copy of the formula included in the [Homebrew core repository](https://github.com/Homebrew/homebrew-core/blob/master/Formula/clblast.rb). CLBlast can be installed using `brew install clblast`.


NuGet (Windows)
-------------

To be done.
