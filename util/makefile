#-------------------------------------------------------------------------------
#   Assembly Language Implementation of a B-Tree
#   Copyright (C) 2025  J. McIntosh
#
#   This program is free software; you can redistribute it and/or modify
#   it under the terms of the GNU General Public License as published by
#   the Free Software Foundation; either version 2 of the License, or
#   (at your option) any later version.
#
#   This program is distributed in the hope that it will be useful,
#   but WITHOUT ANY WARRANTY; without even the implied warranty of
#   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#   GNU General Public License for more details.
#
#   You should have received a copy of the GNU General Public License along
#   with this program; if not, write to the Free Software Foundation, Inc.,
#   51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
#-------------------------------------------------------------------------------
# file:		makefile
# author:	J. McIntosh
# brief:	makefile for libutil.so
#-------------------------------------------------------------------------------
libutil.so: memmove64.o util.o
	gcc -z noexecstack -g -shared memmove64.o util.o -o libutil.so
util.o: util.c
	gcc -g -fPIC -c util.c -o util.o
memmove64.o: memmove64.asm
	nasm -g -f elf64 memmove64.asm
clean:
	rm -f libutil.so util.o memmove64.o
