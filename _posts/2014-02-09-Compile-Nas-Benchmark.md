---
layout: post
title: Compile NAS Benchmark
author: intijk
---

Curent Newest Version of NAS Benchmark is NPB3.3.1, 3 implement types are:

	NPB3.3-SER Serial 	
	NPB3.3-OMP OpenMP
	NPB3.3-MPI MPI 

9 Benchmarks in it, 7 written in Fortran, 2 in C.

To compile it, the only you need to do is edit file *config/make.def.template*, then copy or rename it to *config/make.def*.

The options in the file is mainly assign compiler for it.
After remove annotation, option left are:

	MPIF77 = mpif77
	FLINK   = $(MPIF77)
	FMPI_LIB  = -L/usr/local/lib -lmpi
	FMPI_INC = -I/usr/local/include
	FFLAGS  = -O
	FLINKFLAGS = -O
	
	MPICC = mpicc
	CLINK   = $(MPICC)
	CMPI_LIB  = -L/usr/local/lib -lmpi
	CMPI_INC = -I/usr/local/include
	CFLAGS  = -O
	CLINKFLAGS = -O
	CC      = cc -g
	BINDIR  = ../bin

Start from the default template, the only 2 options you may need change are **MPIF77** and **MPICC**. For any further configuration, just change the  corresponding parameters.

Now you could 
	
	make CLASS=S

under eache benchmark folder to test it.



