include $(top_rulesdir)/Makefile.inc

all:
# Inspect x86 objects, but execute the packaged tool on DEB_HOST_ARCH.
	$(MAKE) -C $(top_srcdir)/tools/objtool O=$(CURDIR) HOSTARCH=$(KERNEL_ARCH) ARCH=x86 HOSTCC=$(CC) HOSTLD=$(CROSS_COMPILE)ld HOSTAR=$(CROSS_COMPILE)ar V=$(KBUILD_VERBOSE)

install:
	install -D -m755 objtool $(DESTDIR)/$(installdir)/objtool
