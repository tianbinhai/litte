#### 说明

* 软件不定期同步大神库更新，适合一键下载到package目录下，用于openwrt编译

* lede/package$下运行 或者openwrt/package$下运行

```bash
 git clone https://github.com/kenzok8/litte.git
```

* Lean源码下快捷编译

```bash
rm -rf package/litte/microsocks && rm -rf package/litte/redsocks2 && rm -rf package/litte/tcpping
cp -f package/litte/commit/default-settings package/lean/default-settings/files/zzz-default-settings
cp -f package/litte/commit/banner package/base-files/files/etc/banner
cp -f package/litte/commit/Leandiffconfig .config && make defconfig
git pull && ./scripts/feeds update -a
./scripts/feeds install -a
make download -j7 V=s && find dl -size -1024c -exec ls -l {} \;
make download && make -j$(nproc) V=s
```

* Lienol源码下快捷编译

```bash
rm -rf package/litte/adguardhome && rm -rf package/litte/luci-app-adguardhome
cp -f package/litte/commit/zzz-default-settings package/default-settings/files/zzz-default-settings
cp -f package/litte/commit/banner package/base-files/files/etc/banner
cp -f package//litte/commit/Lienoldiffconfig .config && make defconfig
./scripts/feeds update -a
./scripts/feeds install -a
make download -j7 V=s && find dl -size -1024c -exec ls -l {} \;
make download && make -j$(nproc) V=s
```

* ctc team源码下快捷编译

```bash
rm -rf package/lienol/luci-app-passwall && rm -rf package/lean/luci-app-ssr-plus
rm -rf package/litte/microsocks && rm -rf package/litte/redsocks2 && rm -rf package/litte/tcpping
rm -rf package/ntlf9t/AdGuardHome && rm -rf package/ctcgfw/luci-app-adguardhome
rm -rf package/litte/luci-app-advancedsetting && rm -rf package/litte/luci-app-aliddns && rm -rf package/litte/luci-app-clash
rm -rf package/litte/gost && rm -rf package/litte/luci-app-gost && rm -rf package/litte/luci-app-eqos
rm -rf package/ctcgfw/luci-app-openclash && rm -rf package/litte/luci-app-smartdns && rm -rf package/litte/smartdns
rm -rf package/ctcgfw/luci-theme-atmaterial && rm -rf package/ctcgfw/luci-theme-opentomato && rm -rf package/ctcgfw/luci-theme-mcat
cp -f package/litte/commit/default-settings package/lean/default-settings/files/zzz-default-settings
cp -f package/litte/commit/banner package/base-files/files/etc/banner
cp -f package/litte/commit/ctcdiffconfig .config && make defconfig
./scripts/feeds update -a && ./scripts/feeds install -a
make download -j7 V=s && find dl -size -1024c -exec ls -l {} \;
make download && make -j$(nproc) V=s
```

- openwrt 固件编译自定义主题与软件
- luci-app-openclash           
- clash图形简易版
- luci-theme-atmaterial        
- atmaterial 三合一主题
- luci-theme-argon-new
- argon二合一主题 Lean Lienol 19.07适配
- ifit 透明主题
- luci-app-ADG        
- 去广告
- luci-app-passwall           
- Lienol大神passwall
- luci-app-ssr-plus           
- lean大神的ssr

#### 注意


* 本人自用的插件并不能保证没有bug，diffconfig是自己用于编译的备份文件，不乱改的话能确保编译成功




![暗黄主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-9.jpg)
![暗黄主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-10.jpg)
![暗黄主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-11.jpg)
![暗黑红主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-5.jpg)
![暗黑红主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-6.jpg)
![暗黑红主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-7.jpg)
![暗黑红主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-8.jpg)
![抹茶绿主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-12.jpg)
![抹茶绿主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-13.jpg)
![抹茶绿主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-14.jpg)
![argon主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-1.png)
![argon主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-2.png)
![argon主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-3.png)
![argon主题](https://raw.githubusercontent.com/kenzok8/openwrt-packages/master/screenshot/sshot-4.png)


