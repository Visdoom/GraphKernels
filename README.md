# GraphKernels

This package was originally developed by Elisabetta Ghsiu (https://github.com/eghisu).
This version is adjusted to work under Python3.

A large collection of source codes for computing kernels on graph.

- GraphKernelsCollection contains a variety of scripts for computing kernels with MATLAB and Python
- graphkernels is a Python package for graph kernels. The Python interface is created from a C++ source code that is wrapped with SWIG
- GKextCPy is the package created to build the extension module for the wrapper from C++ to Python


# Installation under Linux

The installation has only been tested under Ubuntu 16.04 LTS. 
For the installation to work one needs to install the following packages before!
- compiled C headers of `igraph` 
- C headers of `eigen3`

## Installation of `igraph`
-  Downloaded the .tar from http://igraph.org/c/#downloads
- unpack into /usr/local/include using `sudo tar xvzf [igraph-packagename].tar.gz`
- go into folder
- run ` ./configure`, `make check`, `make` and `make install` in that order

## Installation of `eigen3`
The C header files of `eigen3` can either be downloaded and saved under `/usr/local/include` directly or one builds them the same as `igraph` cloning the source code from https://github.com/eigenteam/eigen-git-mirror

I followed the instructions from https://github.com/eigenteam/eigen-git-mirror/blob/master/INSTALL
If `cmake` is not installed on your system you can get it through `apt install cmake`.

## Installation of `graphkernels`
After the setup of the C header dependencies one can install the `graphkernels` package by simply cloning the repository and executing `python3 setup.py install` in the graphkernels folder.
The setup script will subsequently install the C-Python-Wrapper `GKextCPy` and set up the `graphkernels` package.
