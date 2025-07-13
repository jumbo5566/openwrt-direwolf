#
# Copyright (C) 2023 SQ2MO
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=direwolf
PKG_VERSION:=1.7-dev-A
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/wb2osz/direwolf/archive/refs/tags/
PKG_HASH:=4666d09041b467cf3b2d047be948cb8cafb99105353b681099bd6980a811c012

PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=LICENSE

#PKG_BUILD_DEPENDS:=alsa-lib

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/direwolf
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=AX.25 soundcard TNC, digipeater, APRS IGate, GPS tracker, and APRStt gateway
  URL:=https://github.com/wb2osz/direwolf/
  DEPENDS:= +alsa-lib+libudev
endef

define Package/direwolf/description
  Dire Wolf is a software "soundcard" AX.25 packet modem/TNC and APRS encoder/decoder. It can be used stand-alone to observe APRS traffic, as a tracker, digipeater, APRStt gateway, or Internet Gateway (IGate).
endef

define Package/direwolf/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/direwolf $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/cm108 $(1)/usr/bin
endef

$(eval $(call BuildPackage,direwolf))
