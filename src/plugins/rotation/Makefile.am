include $(top_srcdir)/src/plugins/Makefile.plugins

plugindir = $(PLUGINDIR)/rotation
plugin_LTLIBRARIES = librotation.la

plugin_in_files = rotation.plugin.in

# here we are explicitly specifying gtk+-3.0 and clutter-1.0 to use the vapi
# because vala still cannot parse the gir
VALAFLAGS = \
	--girdir=$(top_srcdir)/src	\
	--pkg Totem-1.0 --pkg libpeas-1.0 --pkg cogl-pango-1.0 --pkg GtkClutter-1.0 --pkg clutter-1.0 --pkg gtk+-3.0

librotation_la_SOURCES = totem-rotation-plugin.vala
librotation_la_LDFLAGS = $(plugin_ldflags)
librotation_la_CFLAGS = $(plugin_cflags) -include $(CONFIG_HEADER)
librotation_la_LIBADD = $(plugin_libadd)

GITIGNOREFILES = \
	$(librotation_la_SOURCES:.vala=.c) \
	librotation_la_vala.stamp \
	$(NULL)

-include $(top_srcdir)/git.mk
