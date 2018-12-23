include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=mtk-soc-wm8960
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/sdnavarrol/mtk-soc-wm8960.git

PKG_BUILD_DIR:=$(KERNEL_BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define KernelPackage/mtk-soc-wm8960
	SUBMENU:=Sound Support
	DEFAULT:=y
	TITLE:=ASoc MTK PCM/I2S machine
	FILES:= $(PKG_BUILD_DIR)\i2s_ctrl.$(LINUX_KMOD_SUFFIX)
endef

define Package/mtk-soc-wm8960/description
	Alsa Driver MT7688 WM8960
endef

define Package/mtk-soc-wm8960/install
	
endef

$(eval $(call KernelPackage,mtk-soc-wm8960))
