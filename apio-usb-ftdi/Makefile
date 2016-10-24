CFLAGS += `pkg-config --cflags libusb-1.0` `pkg-config --cflags libftdi`
LDLIBS += `pkg-config --libs libusb-1.0`   `pkg-config --libs libftdi`
# TODO: En realidad esto debería ser así, pero apio sólo soporta 1 directorio
#ARCHDIR ?= x86_64-linux-gnu/

all: find_all listdevs

# debian/control: debian/packages debian/yada
# 	debian/yada rebuild control
# 
# debian/rules: debian/packages debian/yada
# 	debian/yada rebuild rules

deb: all
	fakeroot dpkg-buildpackage -b -uc

clean:
	-rm -f find_all listdevs .*~

install: all
	install -m 0755 -d $(DESTDIR)/usr/lib/$(ARCHDIR)apio/packages/system
	install -m 0755 find_all $(DESTDIR)/usr/lib/$(ARCHDIR)apio/packages/system
	install -m 0755 listdevs $(DESTDIR)/usr/lib/$(ARCHDIR)apio/packages/system

