# cloudflared + nginx TCP/UDP Proxy
Cloudflare Zero Trustにて指定したドメインにアクセス時のIPv4アドレスを固定するためのcloudflaredとnginxによるTCP/UDPプロキシのセット

# 利用方法

## 1. 環境変数を設定する

- example.envを.envにコピー

```shell
cp example.env .env
```

- .envの TUNNEL_TOKEN を埋める
- Dockerネットワーク設定はDockerネットワーク内部のIPアドレスの固定に用いているだけなので、基本的には変更する必要はない

例)

```
# Cloudflare Tunnel用に発行したトークン
TUNNEL_TOKEN=eyJ（略）

# Dockerネットワーク設定
（略）
```

## 2. 起動

```shell
docker compose up
```
