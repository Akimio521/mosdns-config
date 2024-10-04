## Akimio521/mosdns-config

**自用 Mosdns 配置**

- 默认启动 TCP/UDP DNS 服务器，监听所有网卡的 5533 端口
- 支持优选 CloudFlare CDN IP，修改路径：`cdn.yaml -> plugin -> blackhole_cloudflare_ipv4 / blackhole_cloudflare_ipv6`