# Basic 認証用のファイルを作成
```
$ htpasswd -Bbc auth/htpasswd [USERNAME] [PASSWORD]
```

# HTTPS 用の証明書作成
HTTPS で通信する場合のみ作成
```
$ openssl req \
  -newkey rsa:4096 -nodes -sha256 -keyout certs/domain.key \
  -x509 -days 365 -out certs/domain.crt \
;
```

# Docker Registry にログイン
```
$ docker login localhost:5000
```

# イメージをプッシュ

## タグ設定
```
$ docker tag 対象のイメージ名:対象のタグ名 localhost:5000/イメージ名:タグ名
```

## プッシュ
```
$ docker push localhost:5000/イメージ名:タグ名
```

# イメージをプル
```
$ docker pull localhost:5000/イメージ名:タグ名
```
