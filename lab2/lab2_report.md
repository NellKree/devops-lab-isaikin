University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)
Year: 2025/2026
Group: U4125
Author: Исайкин Евгений Дмитриевич
Lab: Lab2
Date of create: 28.02.2026
Date of finished: 

Настройка CI/CD пайплайна с GitHub Actions:

# Подготовка проекта:

## Скопировать файлы из первой лабораторной (app.py, requirements.txt, Dockerfile) в новый репозиторий

## Создать аккаунт на Docker Hub (если нет)

## Создать новый репозиторий на Docker Hub для вашего образа
<img width="709" height="470" alt="image" src="https://github.com/user-attachments/assets/ef30c979-8f58-4bd3-9d8d-f1c5a718f722" />

# Настройка GitHub Actions:

## Создать папку .github/workflows/ в корне проекта
<img width="549" height="237" alt="image" src="https://github.com/user-attachments/assets/9f60252a-e232-48cc-ab8e-c3b3e8f65f5b" />

## Создать файл docker-build.yml с пайплайном, который должен:
Запускаться при пуше в main ветку
Использовать Ubuntu как runner
Выполнять checkout кода
Настраивать Docker Buildx
Логиниться в Docker Hub используя секреты
Собирать и пушить образ с тегом username/my-flask-app:latest
Добавлять шаг деплоя (можно просто echo сообщение)
<img width="434" height="435" alt="image" src="https://github.com/user-attachments/assets/a5f6bb77-0eb8-4fd0-9cc0-83b3bf10f9f2" />

# Настройка секретов:

## В настройках GitHub репозитория добавить секреты:
DOCKER_USERNAME - ваш логин на Docker Hub
DOCKER_PASSWORD - ваш пароль или токен доступа Docker Hub
<img width="653" height="506" alt="image" src="https://github.com/user-attachments/assets/6859a3c1-a6cd-46c3-82dc-469d72f0b091" />
<img width="494" height="448" alt="image" src="https://github.com/user-attachments/assets/f635f8b8-e7d5-4d54-8cab-98d1565436c6" />

# Тестирование пайплайна:

## Сделать коммит и пуш в main ветку
<img width="728" height="641" alt="image" src="https://github.com/user-attachments/assets/7dd7b91b-1a10-4cec-a449-6f1c8720212e" />

## Проверить выполнение пайплайна в разделе Actions
<img width="723" height="492" alt="image" src="https://github.com/user-attachments/assets/6bfa9d8d-1f5b-4ca6-966e-5ee4b3efd383" />
<img width="720" height="606" alt="image" src="https://github.com/user-attachments/assets/12b73947-542e-4809-a788-f9244a256d57" />

## Убедиться, что образ появился в Docker Hub
<img width="714" height="691" alt="image" src="https://github.com/user-attachments/assets/86558684-00fe-4109-861f-0a7860dea61d" />

## Проверить логи выполнения каждого шага
<img width="729" height="661" alt="image" src="https://github.com/user-attachments/assets/0a18439f-b32f-4389-91bd-e9c11f7bf875" />
