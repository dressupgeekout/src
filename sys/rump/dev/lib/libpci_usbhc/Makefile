#	$NetBSD: Makefile,v 1.6 2020/11/06 15:35:33 christos Exp $
#

RUMPTOP=${TOPRUMP}

.PATH:	${RUMPTOP}/../dev/pci ${RUMPTOP}/../dev/usb

LIB=	rumpdev_pci_usbhc
COMMENT=PCI USB host controller drivers

IOCONF=	PCI_USBHC.ioconf
RUMP_COMPONENT=ioconf

SRCS+=	ohci_pci.c ohci.c
SRCS+=	uhci_pci.c uhci.c
SRCS+=	ehci_pci.c ehci.c
SRCS+=	xhci_pci.c xhci.c
SRCS+=	usb_pci.c

CPPFLAGS+= -I${RUMPTOP}/librump/rumpkern -I${RUMPTOP}/../dev

.include "${RUMPTOP}/Makefile.rump"
.include <bsd.lib.mk>
.include <bsd.klinks.mk>
