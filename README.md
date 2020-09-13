# Basic 認証用のファイルを作成
```
$ htpasswd -Bbc auth/htpasswd [USERNAME] [PASSWORD]
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
