自定义固件 [红米AX6000-ImmortalWrt](https://firmware-selector.immortalwrt.org/?version=23.05.4&target=mediatek%2Ffilogic&id=xiaomi_redmi-router-ax6000)

```
===OpenClash
luci-i18n-base-zh-cn luci-i18n-firewall-zh-cn luci-i18n-opkg-zh-cn vsftpd openssh-sftp-server coreutils-nohup bash dnsmasq-full curl ca-certificates ipset ip-full libcap libcap-bin ruby ruby-yaml kmod-tun kmod-inet-diag unzip kmod-nft-tproxy luci-compat luci luci-base luci-theme-argon luci-app-openclash

===首次启动时运行的脚本
# Configure Password
(echo 'TieGF@1981'; sleep 1; echo 'TieGF@1981') | passwd > /dev/null
# Configure System
uci set system.@system[0].zonename='Asia/Shanghai'
uci set system.@system[0].timezone='CST-8'
uci set system.@system[0].hostname='Redmi6K'
# Configure Lan
uci set network.lan.ipaddr='192.168.123.1'
# uci set dhcp.@dnsmasq[0].filter_aaaa='1' #过滤 IPv6 AAAA 记录
# uci set dhcp.lan.ra='server' #设置后，局域网设备获取IPv6地址
# Configure Wan
uci set network.wan.proto='pppoe'
uci set network.wan.username='13700005410@net'
uci set network.wan.password='12345678'
# Configure WiFi-2.4G
uci set wireless.@wifi-device[0].disabled='0'
uci set wireless.@wifi-device[0].htmode='HE40'
uci set wireless.@wifi-device[0].country='US'
uci set wireless.@wifi-device[0].channel='auto'
uci set wireless.@wifi-device[0].noscan='1'
uci set wireless.@wifi-iface[0].encryption='psk2'
uci set wireless.@wifi-iface[0].ssid='HomeNet@2.4G'
uci set wireless.@wifi-iface[0].key='13700005410'
uci set wireless.@wifi-iface[0].hidden='1'
# Configure WiFi-5G
uci set wireless.@wifi-device[1].disabled='0'
uci set wireless.@wifi-device[1].htmode='HE80'
uci set wireless.@wifi-device[1].country='US'
uci set wireless.@wifi-device[1].channel='40'
uci set wireless.@wifi-iface[1].encryption='psk2'
uci set wireless.@wifi-iface[1].ssid='HomeNet@WiFi'
uci set wireless.@wifi-iface[1].key='13700005410'
# commit All uci
uci commit
echo 'All done!'

===
# 自定义DNS服务器
uci set network.wan.peerdns='0'
uci set network.wan.dns='119.29.29.29 223.5.5.5'
```
