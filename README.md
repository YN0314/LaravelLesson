1. Install docker
2. setting .env file

```
# timezone
TZ=Asia/Tokyo
# mysql root password
DB_ROOT_PASS=p@ssw0rd
# mysql database
DB_NAME=sample_app
# mysql db_user
DB_USER=sample
# mysql db_password
DB_PASS=sample
```

3. create and start container
   - docker-compose up -d --build
4. execute bash on container
   - docker-compose exec app ash
5. execute library install
   - cd sample_app
   - composer install
6. setting enviroment and application key
   - cp -ip .env.example .env
   - php artisan key:generate
