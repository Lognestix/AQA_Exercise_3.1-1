## Созданы файлы docker-compose.yml, application.properties для работы с Docker.
```yml
version: '3.7'
services:
  postgresql:
    image: postgres:12-alpine
    ports:
      - '5432:5432'
    volumes:
      - ./data:/var/lib/postgres
    environment:
      - POSTGRES_DB=base
      - POSTGRES_USER=adm
      - POSTGRES_PASSWORD=9mRE
```
```Java
spring.datasource.url=jdbc:postgresql://185.119.57.164:5432/base
spring.datasource.username=adm
spring.datasource.password=9mRE
```
