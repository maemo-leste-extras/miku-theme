EXTRA_DIST 			= wallpaper1.png wallpaper2.png wallpaper3.png wallpaper4.png \
				  wallpaper1-thumb.png wallpaper2-thumb.png wallpaper3-thumb.png wallpaper4-thumb.png \
				  theme_bg.desktop

install: 

	$(mkinstalldirs) $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)
	
	convert -resize 125x75 wallpaper1.png wallpaper1-thumb.png
	convert -resize 125x75 wallpaper2.png wallpaper2-thumb.png
	convert -resize 125x75 wallpaper3.png wallpaper3-thumb.png
	convert -resize 125x75 wallpaper4.png wallpaper4-thumb.png
	
	hildon-theme-dither wallpaper1.png wallpaper1-tmp.png
	hildon-theme-dither wallpaper2.png wallpaper2-tmp.png
	hildon-theme-dither wallpaper3.png wallpaper3-tmp.png
	hildon-theme-dither wallpaper4.png wallpaper4-tmp.png
	
	hildon-theme-dither wallpaper1-thumb.png
	hildon-theme-dither wallpaper2-thumb.png
	hildon-theme-dither wallpaper3-thumb.png
	hildon-theme-dither wallpaper4-thumb.png

	install -c -m 644 wallpaper1-tmp.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper1.png
	install -c -m 644 wallpaper2-tmp.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper2.png
	install -c -m 644 wallpaper3-tmp.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper3.png
	install -c -m 644 wallpaper4-tmp.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper4.png
	
	install -c -m 644 wallpaper1-thumb.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper1-thumb.png
	install -c -m 644 wallpaper2-thumb.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper2-thumb.png
	install -c -m 644 wallpaper3-thumb.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper3-thumb.png
	install -c -m 644 wallpaper4-thumb.png $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)/wallpaper4-thumb.png

	install -c -m 644 theme_bg.desktop $(DESTDIR)/$(BACKGROUNDS_FULL_DIR)

MAINTAINERCLEANFILES			= Makefile.in

CLEANFILES				= wallpaper1-tmp.png \
					  wallpaper2-tmp.png \
					  wallpaper3-tmp.png \
					  wallpaper4-tmp.png \
					  wallpaper1-thumb.png \
					  wallpaper2-thumb.png \
					  wallpaper3-thumb.png \
					  wallpaper4-thumb.png
