Hawaii Base Applications
========================

[![GitHub release](https://img.shields.io/github/release/hawaii-desktop/hawaii-baseapps.svg)](https://github.com/hawaii-desktop/hawaii-baseapps)
[![GitHub issues](https://img.shields.io/github/issues/hawaii-desktop/hawaii-baseapps.svg)](https://github.com/hawaii-desktop/hawaii-baseapps/issues)

Base applications for the Hawaii desktop environment.

## Dependencies

Make sure you have Qt 5.4 or better with the following modules:

* qtbase
* qtdeclarative
* qtquickcontrols

And the following modules from KDE:

* polkit-qt5

## Build

Building this software is a piece of cake.

Assuming you are in the source directory, just create a build directory
and run cmake:

```sh
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=/opt/hawaii ..
```

To do a debug build the last command can be:

```sh
cmake -DCMAKE_INSTALL_PREFIX=/opt/hawaii -DCMAKE_BUILD_TYPE=Debug ..
```

To do a release build instead it can be:

```sh
cmake -DCMAKE_INSTALL_PREFIX=/opt/hawaii -DCMAKE_BUILD_TYPE=Release ..
```

If not passed, the `CMAKE_INSTALL_PREFIX` parameter defaults to /usr/local.
You have to specify a path that fits your needs, /opt/hawaii is just an example.

Package maintainers would pass `-DCMAKE_INSTALL_PREFIX=/usr`.

The `CMAKE_BUILD_TYPE` parameter allows the following values:

* **Debug:** debug build
* **Release:** release build
* **RelWithDebInfo:** release build with debugging information

## Installation

It's really easy, it's just a matter of typing:

```sh
make install
```

from the build directory.
