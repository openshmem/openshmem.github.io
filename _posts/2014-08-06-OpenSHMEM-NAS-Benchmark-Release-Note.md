---
layout: post
title: OpenSHMEM NAS Benchmark Release Notification
author: naveen-rn
---

The OpenSHMEM version of the NAS Parallel benchmark has been released
by the OpenSHMEM project. The official release notification can be
found in this link - [ReleaseNote](http://bongo.cs.uh.edu/site/Downloads/Examples).


In brief, the release details are:

```bash
version ID : version 1.0a
download   : wget http://bongo.cs.uh.edu/site/sites/default/site_files/openshmem-npbs-release-1.0a.tar.bz2 
```

This OpenSHMEM version is based on the MPI implementation of the NPB
3.2. Block Tridiagonal(BT), Embarrassingly Parallel(EP), MultiGrid(MG)
and Scalar Pentadiagonal(SP) Fortran versions are available along with
the C version of the Integer Sort(IS).

Configuration for the various SHMEM implementations including UH, SGI
and CRAY can be done through the make.def.{uhosh, SGI, cray} template
files available in 

```bash
cd C/config/NAS.samplesconfig/NAS.samples/make.def.{uhosh,sgi,cray}
cd Fortran/config/NAS.samplesconfig/NAS.samples/make.def.{uhosh,sgi,cray}
```
We can lookout for the future releases in this [location](http://bongo.cs.uh.edu/site/Downloads) and
updates on the various release notifications [here](http://openshmem.github.io/).
