SVG = d-and-d-cartoon.svg
PNG = $(SVG).png
JPEG = $(SVG).jpg
WEBP = $(SVG).webp

WIDTH = 600

all: $(PNG) $(JPEG) $(WEBP)

$(PNG): $(SVG)
	inkscape --export-type=png --export-filename=$@ --export-width=$(WIDTH) --export-background='#ffffff' --export-background-opacity=1.0 $<

$(JPEG): $(PNG)
	gm convert $< $@

$(WEBP): $(PNG)
	gm convert $< $@

clean:
	rm -f $(PNG) $(JPEG) $(WEBP)


# vim:ft=make
#
