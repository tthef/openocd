include $(top_srcdir)/common.mk

noinst_LTLIBRARIES = libocdjtagdrivers.la

libocdjtagdrivers_la_SOURCES = \
	$(DRIVERFILES)

nobase_dist_pkglib_DATA =

ULINK_FIRMWARE = $(srcdir)/OpenULINK

EXTRA_DIST = $(ULINK_FIRMWARE)

DRIVERFILES =

# Standard Driver: common files
DRIVERFILES += driver.c

if USB
DRIVERFILES += usb_common.c
endif

if BITBANG
DRIVERFILES += bitbang.c
endif
if PARPORT
DRIVERFILES += parport.c
endif
if DUMMY
DRIVERFILES += dummy.c
endif
if FT2232_DRIVER
DRIVERFILES += ft2232.c
endif
if USB_BLASTER_DRIVER
DRIVERFILES += usb_blaster.c
endif
if AMTJTAGACCEL
DRIVERFILES += amt_jtagaccel.c
endif
if EP93XX
DRIVERFILES += ep93xx.c
endif
if AT91RM9200
DRIVERFILES += at91rm9200.c
endif
if GW16012
DRIVERFILES += gw16012.c
endif
if BITQ
DRIVERFILES += bitq.c
endif
if PRESTO_DRIVER
DRIVERFILES += presto.c
endif
if USBPROG
DRIVERFILES += usbprog.c
endif
if JLINK
DRIVERFILES += jlink.c
endif
if RLINK
DRIVERFILES += rlink.c rlink_speed_table.c
endif
if ULINK
DRIVERFILES += ulink.c
nobase_dist_pkglib_DATA += $(ULINK_FIRMWARE)/ulink_firmware.hex
endif
if VSLLINK
DRIVERFILES += versaloon/usbtoxxx/usbtogpio.c
DRIVERFILES += versaloon/usbtoxxx/usbtojtagraw.c
DRIVERFILES += versaloon/usbtoxxx/usbtoswd.c
DRIVERFILES += versaloon/usbtoxxx/usbtopwr.c
DRIVERFILES += versaloon/usbtoxxx/usbtoxxx.c
DRIVERFILES += versaloon/versaloon.c
DRIVERFILES += vsllink.c
endif
if ARMJTAGEW
DRIVERFILES += arm-jtag-ew.c
endif
if BUSPIRATE
DRIVERFILES += buspirate.c
endif
if REMOTE_BITBANG
DRIVERFILES += remote_bitbang.c
endif

noinst_HEADERS = \
	bitbang.h \
	bitq.h \
	minidriver_imp.h \
	rlink.h \
	rlink_dtc_cmd.h \
	rlink_ep1_cmd.h \
	rlink_st7.h \
	usb_common.h

MAINTAINERCLEANFILES = $(srcdir)/Makefile.in
