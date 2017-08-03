CFLAGS += `pkg-config --cflags libusb-1.0` `pkg-config --cflags libftdi`
LDLIBS += `pkg-config --libs libusb-1.0`   `pkg-config --libs libftdi`
# TODO: En realidad esto debería ser así, pero apio sólo soporta 1 directorio
#ARCHDIR ?= x86_64-linux-gnu/
INST_DIR := /usr/lib/$(ARCHDIR)apio/packages/tools-system

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
	install -m 0755 -d $(DESTDIR)$(INST_DIR)/bin/
	install -m 0755 lsftdi $(DESTDIR)$(INST_DIR)/bin/
	install -m 0755 lsusb $(DESTDIR)$(INST_DIR)/bin/
	install -m 0644 package.json $(DESTDIR)$(INST_DIR)/

