include $(TOPDIR)/rules.mk

PKG_NAME:=lua-cqueues
PKG_VERSION:=rel-20190813
PKG_RELEASE:=1

PKG_MAINTAINER:=Pavel Stano <pavel.stano@websupport.sk>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=COPYRIGHT

PKG_SOURCE_URL:=https://github.com/wahern/lua-cqueues.git
PKG_SOURCE_VERSION:=813664c99c393acbcb007023b195b241a6b90a20
PKG_SOURCE_PROTO:=git
PKG_MIRROR_HASH:=24f1aa69b539e6796445c2228f921744ad64f9336498c7537bee97719d914804

HOST_BUILD_DEPENDS:=lua/host

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk

define Package/lua-cqueues
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=lua-cqueues
  URL:=https://github.com/wahern/lua-cqueues.git
  DEPENDS:=+lua +libopenssl
  PKGARCH:=all
endef

define Package/lua-cqueues/description
  Compresses Lua source code by removing unnecessary characters
endef

define Build/Compile
endef

define Package/lua-cqueues/install
    $(INSTALL_DIR) $(1)/usr/lib/lua
    $(CP) $(PKG_BUILD_DIR)/src/5.1/cqueues.so $(1)/lib/lua/_cqueues.so
endef

define Host/Compile
endef

define Host/Install
    $(INSTALL_DIR) $(1)/lib/lua/5.1
    $(CP) $(HOST_BUILD_DIR)/src/5.1/cqueues.so $(1)/lib/lua/5.1/_cqueues.so
endef

$(eval $(call HostBuild))
$(eval $(call BuildPackage,lua-cqueues))
