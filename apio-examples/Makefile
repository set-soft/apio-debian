DIRS := Cat-board go-board iCE40-HX8K icestick icezum icoboard leds Makefile_example wire kefir TinyFPGA-B2
INST_DIR := /usr/lib/apio/packages/examples

all:

install:
	install -m 0755 -d $(DESTDIR)$(INST_DIR)
	cp -r $(DIRS) $(DESTDIR)$(INST_DIR)
	find $(DESTDIR)$(INST_DIR) -type d -print0 | xargs -0 chmod 755 
	find $(DESTDIR)$(INST_DIR) -type f -print0 | xargs -0 chmod 644
	install -m 0644 package.json $(DESTDIR)$(INST_DIR)/




