#
# Copyright (C) 2015 John Crispin <blogic@openwrt.org>
#
# This is free software, licensed under the GPL 2 license.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=oc3c-ntp-clock
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/oc3c-ntp-clock
  TITLE:=OC3C Ntp Clock
  DEPENDS:=@TARGET_ramips_mt7688_LinkIt7688
  HIDDEN:=1
  CATEGORY:=Base system
  DEFAULT:=y
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
	true
endef

define Build/Compile
	true
endef

define Package/oc3c-ntp-clock/extra_provides
	echo 'libnetsnmp.so.30'; \
	echo 'libnetsnmpagent.so.30'; \
	echo 'libnetsnmpmibs.so.30'; \
	echo 'libnetsnmptrapd.so.30'; \
	echo 'libpthread.so.0'; \
	echo 'libev.so.4'; \
	echo 'librt.so.0';
endef

define Package/oc3c-ntp-clock/install
	$(CP) -fpR ./files/* $(1)
endef

$(eval $(call BuildPackage,oc3c-ntp-clock))
