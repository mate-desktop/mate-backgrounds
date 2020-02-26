backgrounddir = $(datadir)/backgrounds/mate/nature

background_DATA =\
	Aqua.jpg \
	Blinds.jpg \
	Dune.jpg \
	FreshFlower.jpg \
	Garden.jpg \
	GreenMeadow.jpg \
	LadyBird.jpg \
	RainDrops.jpg \
	Storm.jpg \
	TwoWings.jpg \
	Wood.jpg \
	YellowFlower.jpg

metadata_in_files = mate-nature.xml.in
metadatadir = $(datadir)/mate-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)

$(metadata_DATA): $(metadata_in_files)
	$(AM_V_GEN) GETTEXTDATADIR=$(top_srcdir) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

noinst_DATA = mate-nature.xml.in
CLEANFILES = mate-nature.xml mate-nature.xml.in

EXTRA_DIST = \
	$(background_DATA) \
	mate-nature.xml.in.in \
	meson.build

mate-nature.xml.in: mate-nature.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/mate-nature.xml.in.in > mate-nature.xml.in.tmp \
	&& mv mate-nature.xml.in.tmp mate-nature.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
