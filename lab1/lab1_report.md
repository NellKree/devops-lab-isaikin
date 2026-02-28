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
<img width="588" height="104" alt="image" src="https://github.com/user-attachments/assets/1a544c6f-82ab-4983-8a44-20dd341fd416" />

## Запустить интерактивный контейнер: docker run -it ubuntu bash
Внутри контейнера установить пакет (например, curl): apt update && apt install -y curl
<img width="722" height="721" alt="image" src="https://github.com/user-attachments/assets/946105a2-254f-443a-a017-3359131d6722" />
<img width="727" height="755" alt="image" src="https://github.com/user-attachments/assets/e40adb10-3a3e-4ae6-ad36-72278c194ec6" />
<img width="727" height="755" alt="image" src="https://github.com/user-attachments/assets/b5606e2b-cedb-4e2e-91c0-2cfeea0ae05f" />

## Проверить установку: curl --version
<img width="727" height="153" alt="image" src="https://github.com/user-attachments/assets/99be29a5-7770-4694-bed7-dc9901d4a45e" />

# Запуск веб-сервера:

## Запустить контейнер с nginx: docker run -d -p 8080:80 --name web-server nginx:alpine
<img width="642" height="255" alt="image" src="https://github.com/user-attachments/assets/ef422a48-83dd-4867-8e23-9209533d6dff" />

## Проверить работу в браузере: http://localhost:8080
<img width="718" height="264" alt="image" src="https://github.com/user-attachments/assets/03c5dccc-ee3f-491c-b64f-f01353044733" />

## Посмотреть логи контейнера: docker logs web-server
<img width="728" height="740" alt="image" src="https://github.com/user-attachments/assets/859eb2d9-a82f-40cf-bdac-e23eec5c1af3" />

## Подключиться к контейнеру: docker exec -it web-server sh
<img width="457" height="77" alt="image" src="https://github.com/user-attachments/assets/b35bff2a-4822-4650-91a4-74a68339d584" />

# Управление контейнерами:

## Посмотреть запущенные контейнеры: docker ps
<img width="725" height="75" alt="image" src="https://github.com/user-attachments/assets/c4343526-7a59-4557-b39d-fe228d902792" />

## Посмотреть все контейнеры: docker ps -a
<img width="725" height="211" alt="image" src="https://github.com/user-attachments/assets/bb03cb4f-4b6a-4f9d-9a52-a98c6532900a" />

## Остановить и заупстить контейнер: docker stop web-server
<img width="409" height="60" alt="image" src="https://github.com/user-attachments/assets/0fba8183-220f-4a6f-9a62-baa626803950" />
<img width="971" height="353" alt="image" src="https://github.com/user-attachments/assets/3b7d6cc0-7b7d-4b35-b5d7-52e89b91787c" />
<img width="971" height="353" alt="image" src="https://github.com/user-attachments/assets/9f8dd161-4cbe-4d28-9b86-df985e64ff79" />

## Удалить контейнер: docker rm web-server
<img width="724" height="100" alt="image" src="https://github.com/user-attachments/assets/14ca5be2-73b6-45a8-ad78-dcf549581a39" />
<img width="967" height="374" alt="image" src="https://github.com/user-attachments/assets/0a38f67a-0295-4f4a-b283-67c27485d140" />

## Удалить образ: docker rmi nginx:alpine
<img width="579" height="53" alt="image" src="https://github.com/user-attachments/assets/8bd13cac-5135-441b-9698-86bc36bf12be" />

# Работа с томами (volumes):

## Создать том: docker volume create my-volume
<img width="464" height="31" alt="image" src="https://github.com/user-attachments/assets/7525ad46-422d-4185-bbaf-68d3a2a00a6b" />

## Запустить контейнер с томом: docker run -it --name volume-test -d -v my-volume:/data ubuntu bash
<img width="675" height="28" alt="image" src="https://github.com/user-attachments/assets/10dab1ac-339d-4c05-b8c2-daa00b1106f7" />
<img width="967" height="382" alt="image" src="https://github.com/user-attachments/assets/fe20d082-d60c-4d06-a9c3-513cc9e14aed" />

## Создать файл в томе: echo "Hello from volume" > /data/test.txt
<img width="697" height="45" alt="image" src="https://github.com/user-attachments/assets/73bdeca8-a43e-45e2-a14a-963bdf3410ae" />

## Удалить контейнер и создать новый с тем же томом
<img width="419" height="59" alt="image" src="https://github.com/user-attachments/assets/0a248a07-754d-4f49-a5a1-687c91d53d35" />
<img width="972" height="364" alt="image" src="https://github.com/user-attachments/assets/4bcdee61-1ea4-4e41-a35d-3fb5d0993321" />
<img width="705" height="50" alt="image" src="https://github.com/user-attachments/assets/b7b6e0e1-be08-463e-b3f6-cb3bd3f76666" />
<img width="969" height="390" alt="image" src="https://github.com/user-attachments/assets/3a64a4c4-8e67-4a43-bf34-2ea599a2b322" />

## Проверить, что файл сохранился
<img width="322" height="29" alt="image" src="https://github.com/user-attachments/assets/3625075c-8be3-4eb0-ac37-5da53b3bbf63" />
