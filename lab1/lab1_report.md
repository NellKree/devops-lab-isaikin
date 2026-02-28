University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)
Year: 2025/2026
Group: U4125
Author: Исайкин Евгений Дмитриевич
Lab: Lab1
Date of create: 28.02.2026
Date of finished: 

Изучение основ Docker:

# Установка Docker:

Установить Docker Desktop (для Windows/Mac) или Docker Engine (для Linux)
## Проверить установку командой docker --version
<img width="365" height="93" alt="image" src="https://github.com/user-attachments/assets/8639715b-1405-4d3c-aec4-4fe64eea1b82" />

## Запустить тестовый контейнер: docker run hello-world
<img width="595" height="425" alt="image" src="https://github.com/user-attachments/assets/24ca1cb6-d53b-461f-9134-c9bed4610cc4" />

## Изучить базовые команды: docker images, docker ps, docker ps -a
<img width="730" height="154" alt="image" src="https://github.com/user-attachments/assets/7ff752e0-286c-450a-a2da-1e89d5b57468" />

# Работа с готовыми образами:

## Скачать образ Ubuntu: docker pull ubuntu:latest
## Запустить интерактивный контейнер: docker run -it ubuntu bash
## Внутри контейнера установить пакет (например, curl): apt update && apt install -y curl
## Проверить установку: curl --version
## Выйти из контейнера: exit
# Запуск веб-сервера:

## Запустить контейнер с nginx: docker run -d -p 8080:80 --name web-server nginx:alpine
## Проверить работу в браузере: http://localhost:8080
## Посмотреть логи контейнера: docker logs web-server
## Подключиться к контейнеру: docker exec -it web-server sh
# Управление контейнерами:

## Посмотреть запущенные контейнеры: docker ps
## Посмотреть все контейнеры: docker ps -a
## Остановить контейнер: docker stop web-server
## Запустить остановленный контейнер: docker start web-server
## Удалить контейнер: docker rm web-server
## Удалить образ: docker rmi nginx:alpine
# Работа с томами (volumes):

## Создать том: docker volume create my-volume
## Запустить контейнер с томом: docker run -it --name volume-test -d -v my-volume:/data ubuntu bash
## Подключиться к контейнеру: docker exec -it volume-test bash
## Создать файл в томе: echo "Hello from volume" > /data/test.txt
## Удалить контейнер и создать новый с тем же томом
## Проверить, что файл сохранился
