PKG_NAME=xipfs
PKG_URL=git@gitlab-ssh.univ-lille.fr:2xs/pip/xipfs.git
PKG_VERSION=50314bd11fa52442e4639ee10c8cc90ddb51375e
PKG_LICENSE=CeCILL-2.1

include $(RIOTBASE)/pkg/pkg.mk

CFLAGS += -DXIPFS_ENABLE_SAFE_EXEC_SUPPORT

export RIOT_INCLUDES=$(INCLUDES)
export RIOT_CFLAGS=$(CFLAGS)

all: $(BINDIR)/xipfs.a

$(BINDIR)/xipfs.a:
	$(QQ)"$(MAKE)" -C $(PKG_SOURCE_DIR)
	cp $(PKG_SOURCE_DIR)/$(BOARD)/xipfs.a $@

.PHONY: $(BINDIR)/xipfs.a
