# Copyright (C) 1991-2014 Free Software Foundation, Inc.
# This file is part of the GNU C Library.

# The GNU C Library is free software; you can redistribute it and/or
# modify it under the terms of the GNU Lesser General Public
# License as published by the Free Software Foundation; either
# version 2.1 of the License, or (at your option) any later version.

# The GNU C Library is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# Lesser General Public License for more details.

# You should have received a copy of the GNU Lesser General Public
# License along with the GNU C Library; if not, see
# <http://www.gnu.org/licenses/>.

#
#	Makefile for setjmp/longjmp routines
#
subdir	:= setjmp

headers	:= setjmp.h bits/setjmp.h bits/setjmp2.h

routines	:= setjmp sigjmp bsd-setjmp bsd-_setjmp \
		   longjmp __longjmp jmp-unwind

tests		:= tst-setjmp jmpbug bug269-setjmp tst-setjmp-fp \
		   tst-sigsetjmp


include ../Rules

ifeq ($(build-shared),yes)
link-libm = $(common-objpfx)math/libm.so
else
link-libm = $(common-objpfx)math/libm.a
endif
$(objpfx)tst-setjmp-fp: $(link-libm)
