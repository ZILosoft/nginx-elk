Репозиторий для разворачивания ELK стека с 4 Nginx которые проксируют запросы 
а так же собирает логи из папки .docker/logs/* и тегирует их для лучшего понимания откуда пришел зарпос

схема следующая:

nginx-cloudflare -> nginx-node* -> nginx-web

 для запуска нужно выполнить: 
 ```$xslt
docker-compose up 
```

после того как все контейнеры поднимутся можно зайти по адресу

`http://loclahost` и увидеть страницу Hello World!

для доступа к кибане

`http://localhost:5601`

Авторизация
- Username: elastic
- Password: zilpassword