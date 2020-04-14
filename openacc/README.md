# 2D-Laplace-Offload - OpenACC Implementation
This implementation of 2D Laplace equation solver is written in C programming language with OpenACC compiler directives. It requires PGI compiler for compilation and linking. This
page discusses:
* general build instructions for PGI compiler,
* specific build instructions for [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz).

# Build Instructions

## General Build Instructions
Here we demonstrate how to compile and link the example with PGI 19.7.

1. Compile the code by executing:
```
pgcc -O3 -acc -o laplace_acc.o -c laplace_acc.c
```
2. Link the executable by executing:
```
pgcc -O3 -acc -o laplace_acc laplace_acc.o
```

## Topaz Build Instructions
This example can be built on [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz) in following steps:

1. Load the pgi/19.7 module
```
module load pgi/19.7
```
2. Compile and link using make
```
make
```
