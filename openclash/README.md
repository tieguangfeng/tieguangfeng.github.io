自定义OpenClash
```
curl -# -o /etc/config/openclash https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openclash/openclash.ini
curl -# -o /etc/openclash/custom/openclash_custom_rules.list https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openclash/custom_rules.list
curl -# -o /etc/openclash/custom/openclash_custom_firewall_rules.sh https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openclash/firewall_rules.sh
```
自定义OpenWrt
```
curl -# -o /etc/crontabs/root https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openwrt/crontabs.txt
curl -# -o /www/macinstall.html https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openwrt/macinstall.html
curl -# -o /www/iptv.txt https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openwrt/iptv.txt
curl -# -o /www/tvbox.json https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openwrt/tvbox.json
```
更新Meta内核
```
rm -rf /etc/openclash/core/clash_meta
curl https://raw.githubusercontent.com/tieguangfeng/tieguangfeng.github.io/refs/heads/main/openclash/clash_meta > /etc/openclash/core/clash_meta && chmod 755 /etc/openclash/core/clash_meta
```
系统重置
```
rm -rvf /overlay/*  
```

 [OpenClash官方插件](https://github.com/vernesong/OpenClash/releases)
