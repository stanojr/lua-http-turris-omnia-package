include $(TOPDIR)/rules.mk

PKG_NAME:=lua-cqueues
PKG_VERSION:=rel-20190813
PKG_RELEASE:=1

PKG_MAINTAINER:=Pavel Stano <pavel.stano@websupport.sk>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=COPYRIGHT

PKG_SOURCE_URL:=https://github.com/wahern/cqueues.git
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
  URL:=https://github.com/wahern/cqueues.git
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
    $(INSTALL_DIR) $(1)/usr/share/lua/5.1/
    $(INSTALL_DIR) $(1)/usr/share/lua/5.1/cqueues
    $(INSTALL_DIR) $(1)/usr/share/lua/5.1/cqueues/dns
    $(CP) $(PKG_BUILD_DIR)/src/cqueues.lua $(1)/share/lua/5.1/cqueues.lua
    $(CP) $(PKG_BUILD_DIR)/src/socket.lua $(1)/share/lua/5.1/cqueues/socket.lua
    $(CP) $(PKG_BUILD_DIR)/src/errno.lua $(1)/share/lua/5.1/cqueues/errno.lua
    $(CP) $(PKG_BUILD_DIR)/src/signal.lua $(1)/share/lua/5.1/cqueues/errno.lua
    $(CP) $(PKG_BUILD_DIR)/src/thread.lua $(1)/share/lua/5.1/cqueues/thread.lua
    $(CP) $(PKG_BUILD_DIR)/src/condition.lua $(1)/share/lua/5.1/cqueues/condition.lua
    $(CP) $(PKG_BUILD_DIR)/src/promise.lua $(1)/share/lua/5.1/cqueues/promise.lua
    $(CP) $(PKG_BUILD_DIR)/src/auxlib.lua $(1)/share/lua/5.1/cqueues/auxlib.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.lua $(1)/share/lua/5.1/cqueues/dns.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.resolver.lua $(1)/share/lua/5.1/cqueues/dns/resolver.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.config.lua $(1)/share/lua/5.1/cqueues/dns/config.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.hosts.lua $(1)/share/lua/5.1/cqueues/dns/hosts.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.hints.lua $(1)/share/lua/5.1/cqueues/dns/hints.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.record.lua $(1)/share/lua/5.1/cqueues/dns/record.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.packet.lua $(1)/share/lua/5.1/cqueues/dns/packet.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.resolvers.lua $(1)/share/lua/5.1/cqueues/dns/resolvers.lua
endef

define Host/Compile
endef

define Host/Install
    $(INSTALL_DIR) $(1)/lib/lua/5.1
    $(CP) $(HOST_BUILD_DIR)/src/5.1/cqueues.so $(1)/lib/lua/5.1/_cqueues.so
    $(INSTALL_DIR) $(1)/usr/share/lua/5.1/
    $(INSTALL_DIR) $(1)/usr/share/lua/5.1/cqueues
    $(INSTALL_DIR) $(1)/usr/share/lua/5.1/cqueues/dns
    $(CP) $(PKG_BUILD_DIR)/src/cqueues.lua $(1)/share/lua/5.1/cqueues.lua
    $(CP) $(PKG_BUILD_DIR)/src/socket.lua $(1)/share/lua/5.1/cqueues/socket.lua
    $(CP) $(PKG_BUILD_DIR)/src/errno.lua $(1)/share/lua/5.1/cqueues/errno.lua
    $(CP) $(PKG_BUILD_DIR)/src/signal.lua $(1)/share/lua/5.1/cqueues/errno.lua
    $(CP) $(PKG_BUILD_DIR)/src/thread.lua $(1)/share/lua/5.1/cqueues/thread.lua
    $(CP) $(PKG_BUILD_DIR)/src/condition.lua $(1)/share/lua/5.1/cqueues/condition.lua
    $(CP) $(PKG_BUILD_DIR)/src/promise.lua $(1)/share/lua/5.1/cqueues/promise.lua
    $(CP) $(PKG_BUILD_DIR)/src/auxlib.lua $(1)/share/lua/5.1/cqueues/auxlib.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.lua $(1)/share/lua/5.1/cqueues/dns.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.resolver.lua $(1)/share/lua/5.1/cqueues/dns/resolver.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.config.lua $(1)/share/lua/5.1/cqueues/dns/config.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.hosts.lua $(1)/share/lua/5.1/cqueues/dns/hosts.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.hints.lua $(1)/share/lua/5.1/cqueues/dns/hints.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.record.lua $(1)/share/lua/5.1/cqueues/dns/record.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.packet.lua $(1)/share/lua/5.1/cqueues/dns/packet.lua
    $(CP) $(PKG_BUILD_DIR)/src/dns.resolvers.lua $(1)/share/lua/5.1/cqueues/dns/resolvers.lua
endef

$(eval $(call HostBuild))
$(eval $(call BuildPackage,lua-cqueues))
