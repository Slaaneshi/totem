include $(top_srcdir)/src/plugins/Makefile.plugins

plugindir = $(PLUGINDIR)/grilo
plugin_LTLIBRARIES = libgrilo.la

plugin_in_files = grilo.plugin.in

uidir = $(plugindir)
ui_DATA = grilo.ui
EXTRA_DIST += $(ui_DATA)

confdir = $(plugindir)
conf_DATA = totem-grilo.conf
EXTRA_DIST += $(conf_DATA)

libgrilo_la_SOURCES = totem-grilo.c
libgrilo_la_LDFLAGS = $(plugin_ldflags)
libgrilo_la_LIBADD =			\
        $(plugin_libadd)	\
        $(LIBGRILO_LIBS)
libgrilo_la_CFLAGS =			\
        $(plugin_cflags)	\
        $(LIBGRILO_CFLAGS)	\
		  -I $(top_srcdir)/src/backend

-include $(top_srcdir)/git.mk

