# ParMGridGen [![Build Status](https://travis-ci.org/ccopsey/ParMGridGen.svg?branch=master)](https://travis-ci.org/ccopsey/ParMGridGen)

This is a fork of ParMGridGen(http://www-users.cs.umn.edu/~moulitsa/software.html) with CMake build system.

To build ParMGridGen:

  1. Download or clone the sources from `http://github.com/ccopsey/ParMGridGen`
  2. `cd` into `ParMGridGen`
  3. `cmake .`
  4. `make install`

To build individual components of the library, for example only `mgridgen`, use:

  `make mgridgen install`

Advanced options are available via CMake.
