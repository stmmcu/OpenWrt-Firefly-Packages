#
# Copyright (C) 2006-2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=automount
PKG_RELEASE:=2014-06-03

include $(INCLUDE_DIR)/package.mk

define Package/automount
  CATEGORY:=Firefly Extra
  SUBMENU:=Application
  DEPENDS:=+blkid +losetup +ntfs-3g +fdisk +@BUSYBOX_CONFIG_FUSER
  TITLE:= Auto mount the usb disk.
endef

define Build/Compile
endef

define Package/automount/install
	$(INSTALL_DIR) $(1)/etc/hotplug.d/block
	$(INSTALL_BIN) ./automount $(1)/etc/hotplug.d/block/30-mount
endef


$(eval $(call BuildPackage,automount))
