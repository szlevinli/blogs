# Cross

## Warp

- [install docker CE](https://docs.docker.com/install/linux/docker-ce/centos/)
- [使用 Docker 部署 Cloudflare WARP Proxy](https://github.com/haoel/haoel.github.io#943-docker-%E4%BB%A3%E7%90%86).

```bash
docker run -v $HOME/.warp:/var/lib/cloudflare-warp:rw --restart=always --name=cloudflare-warp e7h4n/cloudflare-warp
```

这条命令会在容器上的 40001 开启一个 socks5 代理，接下来查看这个容器的 ip:

```bash
docker run --rm curlimages/curl --connect-timeout 2 -x "socks5://172.17.0.2:40001" ipinfo.io
```

返回的结果中 org 字段应该能看到 Cloudflare 相关的信息。

- 修改 `Xray config file`. 主要是 `routing` 和 `outbounds.tag="chatGPT_proxy"` 章节

```json
{
  "inbounds": [
    {
      "port": 20505,
      "protocol": "vless",
      "settings": {
        "clients": [
          {
            "id": "***",
            "flow": "xtls-rprx-direct",
            "level": 0
          }
        ],
        "decryption": "none",
        "fallbacks": [
          {
            "alpn": "http/1.1",
            "dest": 80
          },
          {
            "alpn": "h2",
            "dest": 81
          }
        ]
      },
      "streamSettings": {
        "network": "tcp",
        "security": "xtls",
        "xtlsSettings": {
          "serverName": "***",
          "alpn": ["http/1.1", "h2"],
          "certificates": [
            {
              "certificateFile": "***",
              "keyFile": "***"
            }
          ]
        }
      }
    }
  ],
  "outbounds": [
    {
      "protocol": "freedom",
      "settings": {}
    },
    {
      "tag": "chatGPT_proxy",
      "protocol": "socks",
      "settings": {
        "servers": [
          {
            "address": "172.17.0.2",
            "port": 40001
          }
        ]
      }
    },
    {
      "protocol": "blackhole",
      "settings": {},
      "tag": "blocked"
    }
  ],
  "routing": {
    "rules": [
      {
        "type": "field",
        "outboundTag": "chatGPT_proxy",
        "domain": ["chat.openai.com"]
      }
    ]
  }
}
```
