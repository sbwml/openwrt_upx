## OpewnWRT Official SnapShots

```shell
svn export https://github.com/sbwml/openwrt_upx/trunk/tools/ucl tools/ucl
svn export https://github.com/sbwml/openwrt_upx/trunk/tools/upx tools/upx
sed -i '/patchelf pkgconf/i\tools-y += ucl upx' tools/Makefile
sed -i '\/autoconf\/compile :=/i\$(curdir)/upx/compile := $(curdir)/ucl/compile' tools/Makefile
```
