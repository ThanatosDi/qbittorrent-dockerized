# qbittorrent-dockerized

qbittorrent 伺服器並使用 VueTorrent 作為 WebUI


# 佈署
```bash
cp .env.example .env
```

將你目前的使用者帳號 UID 和 GUI 填入到 .env 中的 PUID 和 PGID 中

```bash
id {your_username}
```
Example output: 
```bash
uid=1000(your_user) gid=1000(your_user) groups=1000(your_user)
```

啟動容器
```bash
docker compose up -d qbittorrent
```

如果有要透過 cloudflare 的 tunnel 代理 WebUI，就將 tunnel 的 token 貼到 .env 的 `TUNNEL=` 後
並使用以下命令啟動服務即可
```bash
docker compose up -d
```
