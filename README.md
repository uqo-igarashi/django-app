# django-app
djangoアプリのベース

構成
```
Nginx + Django + MySQL
```


コンテナ立ち上げ
```
docker-compose up -d
```

プロジェクト作成
```
docker-compose run --rm app sh -c "django-admin startproject app ."
```

再起動
```
docker compose restart
```

http://localhost:8000

![image](https://user-images.githubusercontent.com/79821503/187807905-5413b270-4961-4ad5-9782-7fb62f97c9aa.png)
