include $(TOPDIR)/rules.mk
PKG_NAME:=pwmSimulator
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_BUILD_DIR:=$(BUILD_DIR)/pwmSimulator-$(PKG_VERSION)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/sdnavarrol/pwmSimulator.git
PKG_SOURCE_DATE:=2018-04-21
PKG_SOURCE_VERSION:=c57f1bd5ffa13792701ed21a9812caaf9fbb63ad
PKG_MIRROR_HASH:=e7da08c4010d908f4eb32774b120d2cf9b0edf45df6ddf37177eb0dbff6af599

include $(INCLUDE_DIR)/package.mk

define Package/pwmSimulator
	SECTION:=hdl_legrand
	CATEGORY:=Audioporteiro
	URL:=http://pwmSimulator.sourceforge.net/
	TITLE:=Doorlock PWM Driver 
endef

define Package/pwmSimulator/description
	Doorlock PWM driver
endef

define Package/pwmSimulator/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/driver $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,pwmSimulator))
