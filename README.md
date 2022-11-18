# Docker-cakephp

## 最初に行う設定

### ディレクトリを作成
```
mkdir -p mysql/data projects
```

### docker-compose.ymlの編集
MYSQL_ROOT_PASSWORD に MySQL のパスワードを記入する

### コンテナを起動・生成
```
docker-compose up -d
```

## 新規で案件を追加する場合
+ *projectsディレクトリ*配下にclone
+ *docker-compose.yml*のnginxにポートを追加
+ *nginxディレクトリ*下にconfファイルを作成(ポート番号は.ymlと揃える)

+ コンテナを起動・生成
```
docker-compose up -d
```
