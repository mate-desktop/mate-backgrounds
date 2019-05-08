backgrounddir = $(datadir)/backgrounds/mate/desktop

background_DATA = \
	Float-into-MATE.png \
	GreenTraditional.jpg \
	Stripes.png \
	MATE-Stripes-Dark.png \
	MATE-Stripes-Light.png \
	Ubuntu-Mate-Cold-no-logo.png \
	Ubuntu-Mate-Dark-no-logo.png \
	Ubuntu-Mate-Radioactive-no-logo.png \
	Ubuntu-Mate-Warm-no-logo.png

metadata_in_files = mate-desktop.xml.in
metadatadir = $(datadir)/mate-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)

$(metadata_DATA): $(metadata_in_files)
	$(AM_V_GEN) GETTEXTDATADIR=$(top_srcdir) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

noinst_DATA = mate-desktop.xml.in
CLEANFILES = mate-desktop.xml mate-desktop.xml.in

EXTRA_DIST = $(background_DATA) mate-desktop.xml.in.in

mate-desktop.xml.in: mate-desktop.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/mate-desktop.xml.in.in > mate-desktop.xml.in.tmp \
	&& mv mate-desktop.xml.in.tmp mate-desktop.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
