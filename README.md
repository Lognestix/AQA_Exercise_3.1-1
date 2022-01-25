## Созданы файлы docker-compose.yml, application.properties для работы с Docker.
```yml
version: '3.7'
services:
  postgres:
    image: postgres:latest
    ports:
      - '3306:3306'
    volumes:
      - ./data:/var/lib/postgres
    environment:
      - POSTGRES_DB=base
      - POSTGRES_USER=adm
      - POSTGRES_PASSWORD=9mRE
```
```Java
spring.datasource.url=jdbc:postgres://localhost:3306/base
spring.datasource.username=adm
spring.datasource.password=9mRE
```
