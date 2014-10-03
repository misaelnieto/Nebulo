## Process this file with automake to produce Makefile.in

## Created by Anjuta


uidir = $(pkgdatadir)/ui
ui_DATA = nebulo.ui


AM_CPPFLAGS = \
	-DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
	-DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
	-DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
	$(NEBULO_CFLAGS)

AM_CFLAGS =\
	 -Wall\
	 -g

bin_PROGRAMS = nebulo

nebulo_SOURCES = \
	nebulo.vala config.vapi

nebulo_VALAFLAGS =  --pkg gobject-introspection-1.0 --pkg gtk+-3.0  \
	--pkg gtk+-3.0


nebulo_LDFLAGS = \
	-Wl,--export-dynamic

nebulo_LDADD = $(NEBULO_LIBS)




EXTRA_DIST = $(ui_DATA)

# Remove ui directory on uninstall
uninstall-local:
	-rm -r $(uidir)
	-rm -r $(pkgdatadir)

