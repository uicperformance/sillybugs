TARGET = rltotiff
OBJS   = rltotiff.o tiff_rgba_io.o

include ../../../Makefile.config

LDFLAGS := $(LDFLAGS) -ltiff -ljpeg -lz -lm -llzma -ljbig

clean:
	rm -rf $(OBJS) $(TARGET)
