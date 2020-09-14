PREFIX ?= /usr
SHAREPREFIX ?= $(PREFIX)/share
MANPREFIX ?= $(SHAREPREFIX)/man
INSTALL ?= install
CP ?= cp

BIN ?= bulifs

all: $(BIN)

install:
	$(INSTALL) -m 0755 -d $(DESTDIR)$(PREFIX)/bin
	$(INSTALL) -m 0755 $(BIN) $(DESTDIR)$(PREFIX)/bin
	$(INSTALL) -m 0755 -d $(DESTDIR)$(MANPREFIX)/man1
	$(INSTALL) -m 0644 manpages/*.1 $(DESTDIR)$(MANPREFIX)/man1
	$(INSTALL) -m 0755 -d $(DESTDIR)$(SHAREPREFIX)/$(BIN)
	$(INSTALL) -m 0755 $(BIN)_* $(DESTDIR)$(SHAREPREFIX)/$(BIN)
	$(CP) -r template $(DESTDIR)$(SHAREPREFIX)/$(BIN)

uninstall:
	$(RM) $(DESTDIR)$(PREFIX)/bin/$(BIN)
	$(RM) $(DESTDIR)$(MANPREFIX)/man1/$(BIN).1*
	$(RM) -r $(DESTDIR)$(SHAREPREFIX)/$(BIN)
