## Akimio521/mosdns-config

**自用 Mosdns 配置**

### How to use
默认启动 TCP/UDP DNS 服务器，监听所有网卡的 53 端口，**！！注意端口占用**
```bash
mosdns start -c ./main.yaml -d ./
```

## Feature
- 避免 DNS 污染与 DNS 泄露，境内大众域名使用境内 DNS 服务器进行解析，其余域名使用 DoH 服务器进行域名解析
- 使用缓存加快 DoH 服务器的响应速度
- 支持优选 CloudFlare CDN IP，修改路径：`cdn.yaml -> plugin -> blackhole_cloudflare_ipv4 / blackhole_cloudflare_ipv6`
- 过滤部分域名不进行优选（Gitlab使用了CloudFlare CDN，但分配的 IP 是特殊 IP，支持 22 端口使用 SSH，优选出来的 IP 可能不支持该端口）