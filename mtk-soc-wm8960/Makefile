include $(TOPDIR)/rules.mk
PKG_NAME:=mtk-soc-wm8960
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/sdnavarrol/mtk-soc-wm8960.git
PKG_SOURCE_VERSION:=dev

include $(INCLUDE_DIR)/package.mk

define Package/mtk-soc-wm8960
	SECTION:=hdl_legrand
	CATEGORY:=Audioporteiro
	URL:=http://pwmSimulator.sourceforge.net/
	TITLE:=Alsa Driver MT7688 WM8960
endef

define Package/mtk-soc-wm8960/description
	Alsa Driver MT7688 WM8960
endef

define Package/mtk-soc-wm8960/install
	
endef

$(eval $(call BuildPackage,mtk-soc-wm8960))
