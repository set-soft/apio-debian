CFLAGS += `pkg-config --cflags libusb-1.0` `pkg-config --cflags libftdi`
LDLIBS += `pkg-config --libs libusb-1.0`   `pkg-config --libs libftdi`
# TODO: En realidad esto debería ser así, pero apio sólo soporta 1 directorio
#ARCHDIR ?= x86_64-linux-gnu/

all: lsftdi lsusb

# debian/control: debian/packages debian/yada
# 	debian/yada rebuild control
# 
# debian/rules: debian/packages debian/yada
# 	debian/yada rebuild rules

deb: all
	fakeroot dpkg-buildpackage -b -uc

clean:
	-rm -f lsftdi lsusb .*~

install: all
	install -m 0755 -d $(DESTDIR)/usr/lib/$(ARCHDIR)apio/packages/system/bin/
	install -m 0755 lsftdi $(DESTDIR)/usr/lib/$(ARCHDIR)apio/packages/system/bin
	install -m 0755 lsusb $(DESTDIR)/usr/lib/$(ARCHDIR)apio/packages/system/bin

