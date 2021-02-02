# docker起動
```
docker-compose up -d
```

# docker起動確認
```
docker-compose ps
```

# DB初期化(シェル実行)
```
./init-mysql.sh
```

# 注意
### Windowsの場合
- change command in file init-mysql.sh as below

```
winpty docker-compose exec db bash -c "chmod 0775 docker-entrypoint-initdb.d/init-database.sh"
winpty docker-compose exec db bash -c "./docker-entrypoint-initdb.d/init-database.sh"
```
