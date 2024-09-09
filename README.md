C++ project template
====================

Simple template for C++ projects using CMake as build system
generator.

Configuration
-------------

This step execute CMake to configure the build system (ex: Make).
You can add extra information such as the path where you want to install
your program/library, compilation options, generator...


``` bash
mkdir build && cd build
cmake .. [-DCMAKE_INSTALL_PREFIX=/install/path] [-G <generator>] [ ... ]
```

Check the [CMake generators page](https://cmake.org/cmake/help/v3.18/manual/cmake-generators.7.html)
to see available generators (Visual Studio, Kate, XCode, ...)

Compilation
-----------

Here we use Make as build system but you can use whatever build system CMake
can handle.

``` bash
make
```

Installation
------------

You can optionally install your program/library to the location pointed
by the variable CMAKE_INSTALL_PREFIX.

``` bash
make install
```
