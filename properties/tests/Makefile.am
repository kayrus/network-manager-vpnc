SUBDIRS=pcf

INCLUDES = -I${top_srcdir}

noinst_PROGRAMS = test-import-export

test_import_export_SOURCES = \
	test-import-export.c

test_import_export_CPPFLAGS = \
	$(GLIB_CFLAGS) \
	$(GLADE_CFLAGS) \
	$(GTK_CFLAGS) \
	$(GCONF_CFLAGS) \
	$(GNOMEKEYRING_CFLAGS) \
	$(NM_UTILS_CFLAGS) \
	$(DBUS_CFLAGS)

test_import_export_LDADD = \
	$(GTHREAD_LIBS) \
	$(GLADE_LIBS) \
	$(GTK_LIBS) \
	$(GCONF_LIBS) \
	$(GNOMEKEYRING_LIBS) \
	$(DBUS_LIBS) \
	$(NM_UTILS_LIBS) \
	$(top_builddir)/properties/.libs/libnm-vpnc-properties.a

if WITH_TESTS

check-local: test-import-export
	$(abs_builddir)/test-import-export $(abs_srcdir)/pcf

endif
