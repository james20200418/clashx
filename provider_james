mixed-port: 7890
allow-lan: false
mode: Rule
log-level: silent
external-controller: 127.0.0.1:60000
proxy-providers:
  fo:
    type: http
    path: ./profiles/proxies/bl.yaml
    url: https://
    interval: 3600
    filter: 'Hong Kong'
    health-check:
      enable: true
      url: http://www.gstatic.com/generate_204
      interval: 300
  ba:
    type: http
    path: ./profiles/proxies/ky.yaml
    url: https://
    filter: 'IEPL-香港'
    interval: 3600
    health-check:
      enable: true
      url: http://www.gstatic.com/generate_204
      interval: 300
  BLSG:
    type: http
    path: ./profiles/proxies/NETFLIX.yaml
    url: https://
    interval: 3600
    filter: 'Singapore'
    health-check:
      enable: true
      url: http://www.gstatic.com/generate_204
      interval: 300

proxy-groups:
  - name: PROXY
    type: url-test
    url: http://www.gstatic.com/generate_204
    interval: 300
    use:
      - fo
      - ba
    proxies:
      - DIRECT
  - name: Netflix
    type: url-test
    url: http://www.gstatic.com/generate_204
    interval: 300
    use:
      - BLSG
  - name: Youtube
    type: url-test
    url: http://www.gstatic.com/generate_204
    interval: 300
    use:
      - ba   
rule-providers:
  reject:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/reject.txt
    path: ./profiles/rules/reject.yaml
    interval: 86400
  icloud:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/icloud.txt
    path: ./profiles/rules/icloud.yaml
    interval: 86400
  apple:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/apple.txt
    path: ./profiles/rules/apple.yaml
    interval: 86400
  google:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/google.txt
    path: ./profiles/rules/google.yaml
    interval: 86400
  proxy:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/proxy.txt
    path: ./profiles/rules/proxy.yaml
    interval: 86400
  direct:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/direct.txt
    path: ./profiles/rules/direct.yaml
    interval: 86400
  private:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/private.txt
    path: ./profiles/rules/private.yaml
    interval: 86400
  gfw:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/gfw.txt
    path: ./profiles/rules/gfw.yaml
    interval: 86400
  greatfire:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/greatfire.txt
    path: ./profiles/rules/greatfire.yaml
    interval: 86400
  tld-not-cn:
    type: http
    behavior: domain
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/tld-not-cn.txt
    path: ./profiles/rules/tld-not-cn.yaml
    interval: 86400
  telegramcidr:
    type: http
    behavior: ipcidr
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/telegramcidr.txt
    path: ./profiles/rules/telegramcidr.yaml
    interval: 86400
  cncidr:
    type: http
    behavior: ipcidr
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/cncidr.txt
    path: ./profiles/rules/cncidr.yaml
    interval: 86400
  lancidr:
    type: http
    behavior: ipcidr
    url: https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/lancidr.txt
    path: ./profiles/rules/lancidr.yaml
    interval: 86400
rules:

  - DOMAIN-KEYWORD,youtube,Youtube
  - DOMAIN,youtubei.googleapis.com,Youtube
  - DOMAIN,yt3.ggpht.com,Youtube
  - DOMAIN-SUFFIX,googlevideo.com,Youtube
  - DOMAIN-SUFFIX,gvt2.com,Youtube
  - DOMAIN-SUFFIX,withyoutube.com,Youtube
  - DOMAIN-SUFFIX,youtu.be,Youtube
  - DOMAIN-SUFFIX,youtube-nocookie.com,Youtube
  - DOMAIN-SUFFIX,youtube.com,Youtube
  - DOMAIN-SUFFIX,youtubeeducation.com,Youtube
  - DOMAIN-SUFFIX,youtubegaming.com,Youtube
  - DOMAIN-SUFFIX,youtubekids.com,Youtube
  - DOMAIN-SUFFIX,yt.be,Youtube
  - DOMAIN-SUFFIX,ytimg.com,Youtube
  - DOMAIN-KEYWORD,netflixdnstest,Netflix
  - DOMAIN,netflix.com.edgesuite.net,Netflix
  - DOMAIN-SUFFIX,fast.com,Netflix
  - DOMAIN-SUFFIX,netflix.com,Netflix
  - DOMAIN-SUFFIX,netflix.net,Netflix
  - DOMAIN-SUFFIX,netflixdnstest0.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest1.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest2.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest3.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest4.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest5.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest6.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest7.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest8.com,Netflix
  - DOMAIN-SUFFIX,netflixdnstest9.com,Netflix
  - DOMAIN-SUFFIX,nflxext.com,Netflix
  - DOMAIN-SUFFIX,nflximg.com,Netflix
  - DOMAIN-SUFFIX,nflximg.net,Netflix
  - DOMAIN-SUFFIX,nflxso.net,Netflix
  - DOMAIN-SUFFIX,nflxvideo.net,Netflix
  - IP-CIDR,8.41.4.0/24,Netflix,no-resolve
  - IP-CIDR,23.246.0.0/18,Netflix,no-resolve
  - IP-CIDR,37.77.184.0/21,Netflix,no-resolve
  - IP-CIDR,38.72.126.0/24,Netflix,no-resolve
  - IP-CIDR,45.57.0.0/17,Netflix,no-resolve
  - IP-CIDR,64.120.128.0/17,Netflix,no-resolve
  - IP-CIDR,66.197.128.0/17,Netflix,no-resolve
  - IP-CIDR,69.53.224.0/19,Netflix,no-resolve
  - IP-CIDR,103.87.204.0/22,Netflix,no-resolve
  - IP-CIDR,108.175.32.0/20,Netflix,no-resolve
  - IP-CIDR,185.2.220.0/22,Netflix,no-resolve
  - IP-CIDR,185.9.188.0/22,Netflix,no-resolve
  - IP-CIDR,192.173.64.0/18,Netflix,no-resolve
  - IP-CIDR,198.38.96.0/19,Netflix,no-resolve
  - IP-CIDR,198.45.48.0/20,Netflix,no-resolve
  - IP-CIDR,207.45.72.0/22,Netflix,no-resolve
  - IP-CIDR,208.75.76.0/22,Netflix,no-resolve
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
