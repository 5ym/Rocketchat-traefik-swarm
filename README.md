# slim-rocketchat
## 立ち上げ方

```sh
# サンプルをコピーして適宜カスタマイズ
cp docker-compose-sampleyml.yml docker-compose.yml
# https://github.com/5ym/Local-Dev-Traefikの環境の場合
cp docker-compose-traefik.yml docker-compose.yml
# 先にmongo-dbだけ起動
docker-compose up -d r-mongo
# logsを監視してmongoが完全に起動するのを待つ
docker-compose logs -f
# r-initを立ち上げてmongoのレプリカをイニシャライズ
docker-compose up -d r-init
# その後r-initの項目を削除
# 最後にrocketchatを立ち上げて完了
docker-compose up -d rocketchat
```
### docker swarm+traefikの場合
rocketchat-compose.ymlを参照(立ち上げ方準備中)