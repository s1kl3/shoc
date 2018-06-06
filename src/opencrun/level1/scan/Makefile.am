if BUILD_MPI
    MAYBE_MPI = epmpi tpmpi
endif
SUBDIRS = $(MAYBE_MPI)

include $(top_builddir)/config/config.mk
include $(top_builddir)/config/targets.mk

# How to find source files
VPATH = $(srcdir):$(srcdir)/../../common:$(srcdir)/../../../common

AM_LDFLAGS = $(OCRUN_LDFLAGS)
AM_CPPFLAGS = $(CPPFLAGS)
AM_CPPFLAGS += $(OCRUN_CPPFLAGS)
L1LIBS = $(OCRUN_LIBS) $(LIBS)

# what is the destination for programs built from this directory?
serialopencldir = $(bindir)/Serial/OpenCL

# what programs should be installed in the destination?
serialopencl_PROGRAMS = Scan

# how to build those programs
Scan_SOURCES = Scan.cpp \
				scan_cl.cpp \
                main.cpp
Scan_LDADD   = $(L1LIBS)

