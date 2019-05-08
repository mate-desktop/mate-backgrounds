AC_INIT([mate-backgrounds],
	[1.22.0],
	[http://www.mate-desktop.org])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])
AM_INIT_AUTOMAKE([1.9 no-dist-gzip dist-xz tar-ustar check-news])

# Internationalization:
GETTEXT_PACKAGE=mate-backgrounds
AC_SUBST(GETTEXT_PACKAGE)
AC_DEFINE_UNQUOTED([GETTEXT_PACKAGE],
	["$GETTEXT_PACKAGE"], [The domain name to use with gettext.])

AM_GNU_GETTEXT_VERSION([0.19.8])
AM_GNU_GETTEXT([external])

AM_MAINTAINER_MODE

AC_OUTPUT([
Makefile
abstract/Makefile
desktop/Makefile
nature/Makefile
po/Makefile.in
])
