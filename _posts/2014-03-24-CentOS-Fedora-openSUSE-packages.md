---
layout: post
title: CentOS/Fedora/openSUSE packages for OpenSHMEM
author: intijk
---
GASNet and OpenSHMEM RPM packages now available under these distributions(including 32bits and 64bits, use default mpi conduit for GASNet)

 * CentOS 6
 * Fedora 18
 * Fedora 19
 * openSUSE 12.3
 * openSUSE 13.1

How to use:
---
Go repo list :  
[](https://build.opensuse.org/package/repositories/home:intijk:PGAS/OpenSHMEM)

Which shows:

<img src={{ site.url }}/assets/2014-03-24-CentOS-Fedora-openSUSE-packages/image1.png width=600></img>

Click on repository you want, foe example openSUSE 12.3.
Shows:

<img src={{ site.url }}/assets/2014-03-24-CentOS-Fedora-openSUSE-packages/image2.png width=600></img>

You could click rpm you want to install directly or click Go to download repository on the top.

Add link in the address bar as the repository source link.

<img src={{ site.url }}/assets/2014-03-24-CentOS-Fedora-openSUSE-packages/image3.png width=600></img>


For example, under openSUSE, 

	sudo zypper ar http://download.opensuse.org/repositories/home:/intijk:/PGAS/openSUSE_12.3/  PGAS

Sync the meta data:

	sudo zypper refresh

When ask if trust select t(Trust) or a(Always), then just install openshmem-devel.

	sudo zypper in openshmem-devel

Will automatically install GANet as dependency. 

Now you have oshcc, oshrun, etc. 


