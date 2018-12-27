include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=mtk-soc-wm8960
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/sdnavarrol/mtk-soc-wm8960.git
PKG_SOURCE_VERSION:=dev
PKG_BUILD_DIR:=$(KERNEL_BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk


MTK_SOC_WM8960_AUTOLOAD:=\
						mtk_ralink_gdma \
						i2c_wm8960 \
						snd-soc-mt76xx-i2s-ctl \
						snd-soc-mt76xx-i2s \
						snd-soc-mt76xx-pcm \
						snd-soc-wm8960 \
						snd-soc-mt76xx-machine

define KernelPackage/mtk-soc-wm8960
	SUBMENU:=Sound Support
	DEFAULT:=y
	TITLE:=ASoc MTK PCM/I2S machine WM8960 Glue Logic
	FILES:=\
		$(PKG_BUILD_DIR)/mtk_ralink_gdma.ko \
		$(PKG_BUILD_DIR)/i2c_wm8960.ko \
		$(PKG_BUILD_DIR)/snd-soc-mt76xx-i2s-ctl.ko \
		$(PKG_BUILD_DIR)/snd-soc-mt76xx-i2s.ko \
		$(PKG_BUILD_DIR)/snd-soc-mt76xx-pcm.ko \
		$(PKG_BUILD_DIR)/snd-soc-wm8960.ko \
		$(PKG_BUILD_DIR)/snd-soc-mt76xx-machine.ko
	AUTOLOAD:=$(call AutoLoad,50,$(MTK_SOC_WM8960_AUTOLOAD))
	DEPENDS:=+kmod-i2c-core +kmod-sound-soc-core 
endef

define Package/mtk-soc-wm8960/description
	Alsa Driver MT7688 WM8960
endef

MAKE_OPTS:= ARCH="$(LINUX_KARCH)" \
			CROSS_COMPILE="$(TARGET_CROSS)" \
			M="$(PKG_BUILD_DIR)"

define Build/Compile
	$(MAKE) -C "$(LINUX_DIR)" \
			$(MAKE_OPTS) \
			modules
endef

$(eval $(call KernelPackage,mtk-soc-wm8960))
