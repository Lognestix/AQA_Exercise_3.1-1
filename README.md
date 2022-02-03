# Docker (AQA_Exercise_3.1-1)
## Домашнее задание по курсу "Автоматизированное тестирование"
## Тема: «3.1. Docker», задание №1: «PostgreSQL»
1. Создание Docker Container на базе PostgreSQL 12-alpine:
	- прописано создание БД, пользователя, пароля	
1. Запуск SUT (db-api.jar)
	- прописаны необходимые настройки в application.properties
	### Предварительные требования
1. Получить доступ к удаленному серверу
1. На удаленном сервере должны быть установлены и доступны:
	- GIT
	- Docker	
	- Bash
1. На компьютере пользователя должны быть установлены:
	- Intellij IDEA
	- Postman
### Установка и запуск
1. Залогиниться на удаленный сервер
1. Склонировать проект на удаленный сервер командой
	```
	git clone https://github.com/Lognestix/AQA_Exercise_3.1-1
	```
1. Перейти в созданный каталог командой
	```
	cd AQA_Exercise_3.1-1
	```
1. Создать и запустить Docker Container на базе PostgreSQL 12-alpine командой
	```
	docker-compose up
	```
1. Склонировать проект на свой компьютер
	- открыть терминал
	- ввести команду 
		```
		git clone https://github.com/Lognestix/AQA_Exercise_3.1-1
		```
1. Открыть склонированный проект в Intellij IDEA
1. В Intellij IDEA перейти во вкладку Terminal (Alt+F12) и запустить SUT командой
	```
	java -jar db-api.jar
	```
1. В Postman осуществить следующий запрос
	```
	GET http://localhost:9999/api/cards
	```
1. В ответ получить
	```
	[ 
		{ 
			"id":1,
			"name":"Альфа-Карта Premium",
			"description":"Альфа-Карта вернёт ваши деньги",
			"imageUrl":"/alfa-card-premium.png"
		},
		{ 
			"id":2,
			"name":"Alfa Travel Premium",
			"description":"Самая выгодная карта для путешествий",
			"imageUrl":"/alfa-card-travel.png"
		},
		{ 
			id":3,
			"name":"CashBack Premium",
			"description":"Заправь свою карту. Кэшбэк на АЗС, в кафе и ресторанах",
			"imageUrl":"/alfa-card-cashback.png"
		}
	]
	```