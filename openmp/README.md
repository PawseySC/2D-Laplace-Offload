# 2D-Laplace-Offload - OpenMP Implementation
This implementation of 2D Laplace equation solver is written in C programming language with OpenMP compiler directives. It requires GCC or Clang compiler for compilation and linking. This
page discusses:
* general build instructions for GCC and Clang compilers,
* specific build instructions for [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz).

# Build Instructions

## General Build Instructions
### GCC compiler
Here we demonstrate how to compile and link the example with GCC 9.2.0.

1. Compile the code by executing:
```
gcc -O3 -fopenmp -o laplace_mp.o -c laplace_mp.c
```
2. Link the executable by executing:
```
gcc -O3 -fopenmp -o laplace_mp laplace_mp.o
```
### Clang compiler
Here we demonstrate how to compile and link the example with Clang 9.0.0 (for NVidia target).

1. Compile the code by executing:
```
clang -O3 -fopenmp-targets=nvptx64-nvidia-cuda -fopenmp -o laplace_mp.o -c laplace_mp.c
```
2. Link the executable by executing:
```
clang -O3 -fopenmp-targets=nvptx64-nvidia-cuda -fopenmp -lm -o laplace_mp laplace_mp.o
```

## Topaz Build Instructions
### GCC compiler
This example can be built on [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz) with GCC compiler in following steps:

1. Load the gcc/9.2.0 module
```
module load gcc/9.2.0
```
2. Compile and link using make
```
make -f makefile.gcc
```
### Clang compiler
This example can be built on [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz) with Clang compiler in following steps:

1. Load the clang/9.0.0 module (compiled with GCC/7.2.0)
```
module load gcc/7.2.0
module load clang/9.0.0
```
2. Compile and link using make
```
make -f makefile.clang
```
