backgrounddir = $(datadir)/pixmaps/backgrounds/mate/desktop

background_DATA =\
	GreenTraditional.jpg \
	Stripes.png

metadata_in_files = mate-desktop.xml.in
metadatadir = $(datadir)/mate-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)
@INTLTOOL_XML_RULE@

noinst_DATA = mate-desktop.xml.in
CLEANFILES = mate-desktop.xml mate-desktop.xml.in

EXTRA_DIST = $(background_DATA) mate-desktop.xml.in.in

mate-desktop.xml.in: mate-desktop.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/mate-desktop.xml.in.in > mate-desktop.xml.in.tmp \
	&& mv mate-desktop.xml.in.tmp mate-desktop.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
