INST_DIR := /usr/lib/apio/packages/toolchain-icestorm

all:

install:
	install -m 0755 -d $(DESTDIR)$(INST_DIR)/bin/
	ln -s /usr/bin/arachne-pnr $(DESTDIR)$(INST_DIR)/bin/arachne-pnr
	ln -s /usr/bin/icebram $(DESTDIR)$(INST_DIR)/bin/icebram
	ln -s /usr/bin/icepack $(DESTDIR)$(INST_DIR)/bin/icepack
	ln -s /usr/bin/icepll $(DESTDIR)$(INST_DIR)/bin/icepll
	ln -s /usr/bin/iceprog $(DESTDIR)$(INST_DIR)/bin/iceprog
	ln -s /usr/bin/icetime $(DESTDIR)$(INST_DIR)/bin/icetime
	ln -s /usr/bin/yosys $(DESTDIR)$(INST_DIR)/bin/yosys
	ln -s /usr/bin/yosys-abc $(DESTDIR)$(INST_DIR)/bin/yosys-abc
	install -m 0644 package.json $(DESTDIR)$(INST_DIR)/



