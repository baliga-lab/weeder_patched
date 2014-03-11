#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([hello],[1.0.0],[weiju.wu@gmail.com])

AC_CONFIG_AUX_DIR([build-aux])
AM_INIT_AUTOMAKE([-Wall -Werror])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_SRCDIR([src/hello.c])

# we allow for cross-compilation on AROS and AmigaOS
AC_CANONICAL_HOST
case "$host" in
  m68k-*-amigaos) CC=vc CFLAGS="+aos68k -DWORDS_BIGENDIAN $CFLAGS" ;;
  i386-*-aros) CC=i386-linux-aros-gcc ;;
  x86_64-*-aros) CC=x68_64-aros-gcc ;;
esac

# Checks for programs.
AC_PROG_CC

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.
AC_C_BIGENDIAN

# Checks for library functions.

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
