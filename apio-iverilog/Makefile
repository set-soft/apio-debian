INST_DIR := /usr/lib/apio/packages/toolchain-iverilog

all:

install:
	install -m 0755 -d $(DESTDIR)$(INST_DIR)/bin/
	ln -s /usr/bin/iverilog $(DESTDIR)$(INST_DIR)/bin/iverilog
	ln -s /usr/bin/iverilog-vpi $(DESTDIR)$(INST_DIR)/bin/iverilog-vpi
	ln -s /usr/bin/vvp $(DESTDIR)$(INST_DIR)/bin/vvp
	ln -s /usr/lib/x86_64-linux-gnu/ $(DESTDIR)$(INST_DIR)/lib
	install -m 0755 -d $(DESTDIR)$(INST_DIR)/vlib/
	install -m 0644 system.v $(DESTDIR)$(INST_DIR)/vlib/
	install -m 0644 package.json $(DESTDIR)$(INST_DIR)/

