---
layout: post
title:  "Installing CasADi on a Raspberry Pi"
date:   2019-12-04 19:46:00 -0300
categories: CasADi [Raspberry Pi]
---

This is a brief tutorial on how to install [CasADi 3.5.1](https://github.com/casadi/casadi/releases/tag/3.5.1) on a Raspberry Pi and it's heavily based on the CasADi [Linux Installation Guide](https://github.com/casadi/casadi/wiki/InstallationLinux).

Let's install some dependencies

``sudo apt-get install gcc g++ gfortran git cmake libclang-dev llvm-dev libblas3 libblas-dev liblapack3 liblapack-dev ocl-icd-opencl-dev pkg-config --install-recommends``

To compile the Python interface you need SWIG and a decent Python installation

``sudo apt-get install swig ipython python-dev python-numpy python-scipy python-matplotlib --install-recommends``

Install IPOPT

``sudo apt install coinor-libipopt-dev``


``cmake -DPYTHON_EXECUTABLE=/usr/bin/python2 -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 -DPYTHON_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython2.7.so -DNUMPY_PATH=/usr/include/python2.7/numpy -DWITH_PYTHON=ON -DWITH_QPOASES=ON -DWITH_LAPACK=ON -DWITH_IPOPT=ON -DWITH_HSL=ON -DWITH_CLANG=ON -DWITH_OPENCL=ON -DWITH_DL=ON -DWITH_BLASFEO=ON -DWITH_BUILD_BLASFEO=ON -DWITH_MUMPS=ON ..``
