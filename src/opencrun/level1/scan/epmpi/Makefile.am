include $(top_builddir)/config/config.mk
include $(top_builddir)/config/targets.mk

# How to find source files
VPATH = $(srcdir)/..:$(srcdir)/../../../common:$(srcdir)/../../../../common

# which compiler to use
CXX = ${MPICXX}
CXXLD = ${MPICXX}

AM_LDFLAGS = $(OCRUN_LDFLAGS)
AM_CPPFLAGS = $(CPPFLAGS)
AM_CPPFLAGS += $(MPI_CPPFLAGS) $(OCRUN_CPPFLAGS) -I${top_srcdir}/src/mpi/common
L1LIBS = $(OCRUN_LIBS) $(LIBS)

# what is the destination for programs built from this directory?
epopencldir = $(bindir)/EP/OpenCL

# what programs should be installed in the destination?
epopencl_PROGRAMS = Scan

# how to build those programs
Scan_SOURCES = Scan.cpp \
				scan_cl.cpp \
				main.cpp
Scan_LDADD   = $(L1LIBS)

