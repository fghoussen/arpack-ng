LDADD = $(top_builddir)/SRC/libarpack$(LIBSUFFIX).la
AM_CPPFLAGS = -I$(top_builddir) -I$(top_srcdir)/ICB $(EIGEN3_CFLAGS)

EXTRA_DIST = README

lib_LTLIBRARIES = libpyarpack@LIBSUFFIX@.la
libpyarpack@LIBSUFFIX@_la_SOURCES = pyarpack.cpp
libpyarpack@LIBSUFFIX@_la_CPPFLAGS = $(BOOST_CPPFLAGS) $(PYTHON_CPPFLAGS) -I$(top_builddir)/EXAMPLES/MATRIX_MARKET -I$(top_builddir)/ICB -I$(top_builddir) $(EIGEN3_CFLAGS)
libpyarpack@LIBSUFFIX@_la_LDFLAGS = $(BOOST_LDFLAGS) $(PYTHON_LDFLAGS)
libpyarpack@LIBSUFFIX@_la_LIBADD = $(BOOST_NUMPY_LIB) $(BOOST_PYTHON_LIB) $(PYTHON_LIBS) $(PYTHON_EXTRA_LIBS)

PY_LOG_COMPILER = $(PYTHON)
TEST_EXTENSIONS = .py
TESTS_ENVIRONMENT = PYTHONPATH="@abs_top_builddir@/EXAMPLES/PYARPACK/.libs:$$PYTHONPATH"; export PYTHONPATH;
check_SCRIPTS  = pyarpackDenseLDLT.py
check_SCRIPTS += pyarpackDenseLLT.py
check_SCRIPTS += pyarpackDenseLUPP.py
check_SCRIPTS += pyarpackDenseLURR.py
check_SCRIPTS += pyarpackDenseQRPP.py
check_SCRIPTS += pyarpackDenseQRRR.py
check_SCRIPTS += pyarpackSparseBiCGDiag.py
check_SCRIPTS += pyarpackSparseBiCGILU.py
check_SCRIPTS += pyarpackSparseCGDiag.py
check_SCRIPTS += pyarpackSparseCGILU.py
check_SCRIPTS += pyarpackSparseLDLT.py
check_SCRIPTS += pyarpackSparseLLT.py
check_SCRIPTS += pyarpackSparseLU.py
check_SCRIPTS += pyarpackSparseQR.py
TESTS = $(check_SCRIPTS)
