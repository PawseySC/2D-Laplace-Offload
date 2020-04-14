# 2D-Laplace-Offload - Serial Implementation
This basic serial implementation of 2D Laplace equation solver is written in C programming language. It requires C compiler for compilation and linking. This page discusses:
* general build instructions for GCC compiler, 
* specific build instructions for [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz).

# Build Instructions

## General Build Instructions
This example can be built with any compiler supporting ANSI C. Here we demonstrate how to compile and link the example with GCC 8.3.0.

1. Compile the code by executing:
```
gcc -O3 -o laplace.o -c laplace.c
```
2. Link the executable by executing:
```
gcc -O3 -o laplace laplace.o
```

## Topaz Build Instructions
This example can be built on [Topaz cluster](https://support.pawsey.org.au/documentation/display/US/HPC+Systems#HPCSystems-Topaz) in following steps:

1. Load the gcc/8.3.0 module
```
module load gcc/8.3.0
```
2. Compile and link using make
```
make
```
