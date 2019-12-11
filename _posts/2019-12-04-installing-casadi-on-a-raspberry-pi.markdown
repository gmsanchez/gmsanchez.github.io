---
layout: post
title:  "Installing CasADi on a Raspberry Pi"
date:   2019-12-04 19:46:00 -0300
categories: CasADi [Raspberry Pi]
---

This is a brief tutorial on how to install [CasADi 3.5.1](https://github.com/casadi/casadi/releases/tag/3.5.1) on a Raspberry Pi and it's heavily based on the CasADi [Linux Installation Guide](https://github.com/casadi/casadi/wiki/InstallationLinux).

Let's install some dependencies

``sudo apt-get install gcc g++ gfortran git cmake libclang-dev llvm-dev libblas3 libblas-dev liblapack3 liblapack-dev pkg-config --install-recommends``

To compile the Python interface you need SWIG and a decent Python installation

``sudo apt-get install swig ipython python-dev python-numpy python-scipy python-matplotlib --install-recommends``

Install IPOPT

``sudo apt install coinor-libipopt-dev``
