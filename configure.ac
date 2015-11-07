#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([arpspoof], [0.2], [https://github.com/cSploit/arpspoof/issues])
AC_CONFIG_SRCDIR([hashmap.h])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE([foreign])

LT_INIT

# Checks for programs.
AC_PROG_CC

# Checks for libraries.
AC_CHECK_LIB([pcap], [pcap_create], [], [AC_MSG_ERROR([libpcap not found])])
AC_CHECK_LIB([net], [libnet_init], [], [AC_MSG_ERROR([libpcap not found])])

# Checks for header files.
AC_CHECK_HEADERS([netinet/in.h \
                  stdlib.h \
                  string.h \
                  sys/param.h \
                  pcap.h \
                  libnet.h \
                  net/ethernet.h \
                  netinet/if_ether.h], [], [AC_MSG_ERROR([missing required headers])])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_CHECK_FUNCS([inet_ntoa memset socket])

AC_CONFIG_FILES([Makefile])

AC_OUTPUT
