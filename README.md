# ethereum-docker

tools for building Ethereum private network by Docker

## standalone

``` sh
# ジェネシスブロック用コンテナ	
$ cd standalone
$ docker build -t 'geth-init:0.0.1' -f 'geth/Dockerfile_gethinit' geth-init
$ docker run -d --name geth-init -v ~/ethereum-docker/standalone/gethdata:/tmp geth-init

# コンテナに入る
$ docker exec -it geth-init bash

# ジェネシスブロックをマウントしたディレクトリに同期
% rsync -a /root/gethdata /tmp/
% exit

# ジェネシスブロック用コンテナの停止		
$ docker kill geth-init

# マイニング用コンテナの起動
$ docker-compose up -d
# ログの確認
$ docker logs -f geth

```
