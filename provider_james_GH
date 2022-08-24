###############################################################
# 本范例来源为网友
# 感谢网友 Ricky9w 私分享
# 新手用户专用版
###############################################################


mixed-port: 7890
#---------------------------------------------------#
## 配置文件需要放置在 $HOME/.config/clash/*.yaml
allow-lan: false
mode: Rule
log-level: silent
external-controller: 127.0.0.1:60000

# 节点配置文件统一存放在 ./profiles/proxies/ 目录中
proxy-providers:
  # 从链接导入的配置文件
  foo:
    type: http
    path: ./profiles/proxies/foo.yaml
    url: https://example-url
    interval: 3600 
    health-check:
      enable: true
      url: http://www.gstatic.com/generate_204
      interval: 300
proxy-groups:
  - name: PROXY
    type: url-test
    interval: 3600 
    url: http://www.gstatic.com/generate_204
    use:
      - foo

# clash-rules项目提供的规则集
# 规则文件统一存放在 ./profiles/rules/ 目录中
rule-providers:
  reject:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/reject.txt"
    path: ./profiles/rules/reject.yaml
    interval: 86400

  icloud:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/icloud.txt"
    path: ./profiles/rules/icloud.yaml
    interval: 86400

  apple:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/apple.txt"
    path: ./profiles/rules/apple.yaml
    interval: 86400

  google:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/google.txt"
    path: ./profiles/rules/google.yaml
    interval: 86400

  proxy:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/proxy.txt"
    path: ./profiles/rules/proxy.yaml
    interval: 86400

  direct:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/direct.txt"
    path: ./profiles/rules/direct.yaml
    interval: 86400

  private:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/private.txt"
    path: ./profiles/rules/private.yaml
    interval: 86400

  gfw:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/gfw.txt"
    path: ./profiles/rules/gfw.yaml
    interval: 86400

  greatfire:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/greatfire.txt"
    path: ./profiles/rules/greatfire.yaml
    interval: 86400

  tld-not-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/tld-not-cn.txt"
    path: ./profiles/rules/tld-not-cn.yaml
    interval: 86400

  telegramcidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/telegramcidr.txt"
    path: ./profiles/rules/telegramcidr.yaml
    interval: 86400

  cncidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/cncidr.txt"
    path: ./profiles/rules/cncidr.yaml
    interval: 86400

  lancidr:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/lancidr.txt"
    path: ./profiles/rules/lancidr.yaml
    interval: 86400

# 规则
rules:
  - PROCESS-NAME,v2ray,DIRECT
  - PROCESS-NAME,xray,DIRECT
  - PROCESS-NAME,naive,DIRECT
  - PROCESS-NAME,trojan,DIRECT
  - PROCESS-NAME,trojan-go,DIRECT
  - PROCESS-NAME,ss-local,DIRECT
  - PROCESS-NAME,privoxy,DIRECT
  - PROCESS-NAME,leaf,DIRECT
  - PROCESS-NAME,v2ray.exe,DIRECT
  - PROCESS-NAME,xray.exe,DIRECT
  - PROCESS-NAME,naive.exe,DIRECT
  - PROCESS-NAME,trojan.exe,DIRECT
  - PROCESS-NAME,trojan-go.exe,DIRECT
  - PROCESS-NAME,ss-local.exe,DIRECT
  - PROCESS-NAME,privoxy.exe,DIRECT
  - PROCESS-NAME,leaf.exe,DIRECT
  - PROCESS-NAME,Surge,DIRECT
  - PROCESS-NAME,Surge 2,DIRECT
  - PROCESS-NAME,Surge 3,DIRECT
  - PROCESS-NAME,Surge 4,DIRECT
  - PROCESS-NAME,Surge%202,DIRECT
  - PROCESS-NAME,Surge%203,DIRECT
  - PROCESS-NAME,Surge%204,DIRECT
  - PROCESS-NAME,Thunder,DIRECT
  - PROCESS-NAME,DownloadService,DIRECT
  - PROCESS-NAME,qBittorrent,DIRECT
  - PROCESS-NAME,Transmission,DIRECT
  - PROCESS-NAME,fdm,DIRECT
  - PROCESS-NAME,aria2c,DIRECT
  - PROCESS-NAME,Folx,DIRECT
  - PROCESS-NAME,NetTransport,DIRECT
  - PROCESS-NAME,uTorrent,DIRECT
  - PROCESS-NAME,WebTorrent,DIRECT
  - PROCESS-NAME,aria2c.exe,DIRECT
  - PROCESS-NAME,BitComet.exe,DIRECT
  - PROCESS-NAME,fdm.exe,DIRECT
  - PROCESS-NAME,NetTransport.exe,DIRECT
  - PROCESS-NAME,qbittorrent.exe,DIRECT
  - PROCESS-NAME,Thunder.exe,DIRECT
  - PROCESS-NAME,ThunderVIP.exe,DIRECT
  - PROCESS-NAME,transmission-daemon.exe,DIRECT
  - PROCESS-NAME,transmission-qt.exe,DIRECT
  - PROCESS-NAME,uTorrent.exe,DIRECT
  - PROCESS-NAME,WebTorrent.exe,DIRECT
  - DOMAIN,clash.razord.top,DIRECT
  - DOMAIN,yacd.haishan.me,DIRECT
  - RULE-SET,private,DIRECT
  - RULE-SET,reject,REJECT
  - RULE-SET,icloud,DIRECT
  - RULE-SET,apple,DIRECT
  - RULE-SET,google,DIRECT
  - RULE-SET,proxy,PROXY
  - RULE-SET,direct,DIRECT
  - RULE-SET,telegramcidr,PROXY
  - GEOIP,,DIRECT
  - GEOIP,CN,DIRECT
  - MATCH,PROXY
