---
layout: post
title: keyword __attribute__ in C
author: intijk(intijk@gmail.com)
---

In GNU C, there exist the __attribute__ keyword. For example:

	int fun()  __attribute__((__warn_unused_result__));

The function return an int when finished, but it can be used like.

	fun();

instead of:

	retval=fun();

The first case, return value is ignored by caller, function writer hope any one call fun() respect the return value, thus any one who call fun() like the first case, the compiler would give an warning.

In OpenSHMEM, we have 

	# define _WUR __attribute__((__warn_unused_result__))

Where operations like **cswap** will utilize this feature to warn the caller respect the return value!

There are other parameters can be pass to __attribute__, see detail in thie link
http://gcc.gnu.org/onlinedocs/gcc/Function-Attributes.html

