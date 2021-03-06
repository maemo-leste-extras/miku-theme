AC_INIT(Makefile.am)
AM_INIT_AUTOMAKE(hildon-theme-variant-template, 2.9)
AM_CONFIG_HEADER(config.h)

AC_PROG_INSTALL

dnl Add parameters for aclocal 
AC_CONFIG_MACRO_DIR(m4)

dnl theme directory name, ie: default
THEME_DIR="miku"

dnl user-friendly theme name, ie: My default theme
THEME_NAME="Miku"

dnl a layout this theme is based on
LAYOUT_NAME="hildon-theme-layout-5"

dnl check the layout installation
PKG_CHECK_MODULES(HILDON_LAYOUT, "$LAYOUT_NAME" >= 0.14.0)

AC_SUBST(THEME_DIR)
AC_SUBST(THEME_NAME)
AS_AC_EXPAND(LAYOUT_DIR, `$PKG_CONFIG --variable=pkgdatadir $LAYOUT_NAME`)
AS_AC_EXPAND(THEME_FULL_DIR, "${datadir}/themes/$THEME_DIR")
AS_AC_EXPAND(MATCHBOX_LEGACY_FULL_DIR, "${datadir}/themes/$THEME_DIR/matchbox")
AS_AC_EXPAND(MATCHBOX_FULL_DIR, "${datadir}/themes/$THEME_DIR/matchbox2")
AS_AC_EXPAND(IMAGES_FULL_DIR, "${datadir}/themes/$THEME_DIR/images")
AS_AC_EXPAND(GTK_FULL_DIR, "${datadir}/themes/$THEME_DIR/gtk-2.0")
AS_AC_EXPAND(CSS_FULL_DIR, "${datadir}/themes/$THEME_DIR/css")
AS_AC_EXPAND(BACKGROUNDS_FULL_DIR, "${datadir}/themes/$THEME_DIR/backgrounds")
AS_AC_EXPAND(CALENDAR_FULL_DIR, "${datadir}/themes/$THEME_DIR/calendar")
AS_AC_EXPAND(CALLUI_FULL_DIR, "${datadir}/themes/$THEME_DIR/call-ui")
AS_AC_EXPAND(MEDIAPLAYER_FULL_DIR, "${datadir}/themes/$THEME_DIR/mediaplayer")
AS_AC_EXPAND(WIZARD_FULL_DIR, "${datadir}/themes/$THEME_DIR/startup-wizard")
AS_AC_EXPAND(MESSAGING_FULL_DIR, "${datadir}/themes/$THEME_DIR/rtcom-messaging-ui")

dnl check the tools installation
PKG_CHECK_MODULES(TOOLS, hildon-theme-tools >= 0.5.0)

AC_OUTPUT([Makefile				\
           template/Makefile			\
           data/Makefile			\
           matchbox-1/Makefile			\
           matchbox-2/Makefile			\
	   applications/Makefile		\
	   applications/backgrounds/Makefile	\
	   applications/calendar/Makefile	\
	   applications/call-ui/Makefile	\
	   applications/mediaplayer/Makefile	\
	   applications/startup-wizard/Makefile	\
	   applications/rtcom-messaging-ui/Makefile	\
	   applications/hildon-desktop/Makefile		\
	   applications/hildon-desktop/theme_bg.desktop])

dnl some nicey output
AC_MSG_RESULT([
$PACKAGE $VERSION

        Theme name              : $THEME_NAME
        Theme dir               : $THEME_DIR 
        Theme full dir          : $THEME_FULL_DIR
        Matchbox 1 dir          : $MATCHBOX_LEGACY_FULL_DIR
        Matchbox 2 dir          : $MATCHBOX_FULL_DIR
        Gtk full dir            : $GTK_FULL_DIR
	CSS full dir            : $CSS_FULL_DIR

Extra stuff:
	Background images       : $BACKGROUNDS_FULL_DIR
	Startup Wizard images   : $WIZARD_FULL_DIR
	Calendar images         : $CALENDAR_FULL_DIR
	Call UI images          : $CALLUI_FULL_DIR
	Media Player images     : $MEDIAPLAYER_FULL_DIR
	Messaging UI images     : $MESSAGING_FULL_DIR

        Layout name   : $LAYOUT_NAME
        Layout dir    : $LAYOUT_DIR
])
