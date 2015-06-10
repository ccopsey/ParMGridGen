# ParMGridGen [![Build Status](https://travis-ci.org/ccopsey/ParMGridGen.svg?branch=master)](https://travis-ci.org/ccopsey/ParMGridGen)

This is a fork of [ParMGridGen](http://www-users.cs.umn.edu/~moulitsa/software.html) with CMake build system.

To build ParMGridGen:

  1. Download or clone the sources from `http://github.com/ccopsey/ParMGridGen`
  2. `cd` into `ParMGridGen`
  3. `cmake .`
  4. `make install`

To build individual components of the library, for example only `mgridgen`, use:

  `make mgridgen install`

To build the parallel libraries an MPI library must be installed and either discoverable by CMake, or defined explicitly.

Advanced options are available via CMake.

## Original README

This is PARMGRIDGEN version 1.0. You can find the manual describing the
various routines in the directory Doc. Also, the file called INSTALL
contains instructions on how to build and test PARMGRIDGEN.

Any bug fixes and upgrades of the PARMGRIDGEN package is available on WWW
at URL: http://www.cs.umn.edu/~moulitsa/software.html


Irene Moulitsas
moulitsa@cs.umn.edu

Tue Dec  4 18:24:47 CST 2001