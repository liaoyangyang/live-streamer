## Process this file with automake to produce Makefile.in

AM_CPPFLAGS = \
	-DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
	-DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
	-DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
	-I$(top_srcdir)/src -I$(top_srcdir)/src/common -I$(srcdir) \
	$(LIVE555_CPPFLAGS) \
	$(DBUSXX_CFLAGS)

AM_CFLAGS = -Wall
AM_CXXFLAGS = -Wall

noinst_LTLIBRARIES =  \
	librtsp-server.la

librtsp_server_la_SOURCES =  \
	EvUsageEnvironment.cpp \
	EvUsageEnvironment.h \
	DynamicRTSPServer.cpp \
	DynamicRTSPServer.hh \
	LiveStreamInput.cpp \
	LiveStreamInput.hh \
	LiveStreamOutput.cpp \
	LiveStreamOutput.hh

if ENABLE_VO_AACENC
librtsp_server_la_SOURCES += \
	AACAudioEncoder.cpp \
	AACAudioEncoder.hh
endif
