if BUILD_MPI
    MAYBE_MPI = epmpi
endif
SUBDIRS = $(MAYBE_MPI)

include $(top_builddir)/config/config.mk
include $(top_builddir)/config/targets.mk

# How to find source files
VPATH = $(srcdir):$(srcdir)/../../common:$(srcdir)/../../../common

AM_LDFLAGS = $(OCRUN_LDFLAGS)
AM_CPPFLAGS = $(CPPFLAGS)
AM_CPPFLAGS += $(OCRUN_CPPFLAGS) -I$(srcdir)/../../common
L1LIBS = $(OCRUN_LIBS) $(LIBS)

# what is the destination for programs built from this directory?
serialopencldir = $(bindir)/Serial/OpenCL

# what programs should be installed in the destination?
serialopencl_PROGRAMS = Spmv

# how to build those programs
Spmv_SOURCES = Spmv.cpp \
				spmv_cl.cpp \
                main.cpp
Spmv_LDADD   = $(L1LIBS)

