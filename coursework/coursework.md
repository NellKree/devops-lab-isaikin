<img width="382" height="219" alt="image" src="https://github.com/user-attachments/assets/d93a25f2-1742-4625-ad01-d1303bfb6439" />University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)
Year: 2025/2026
Group: U4125
Author: Исайкин Евгений Дмитриевич
Date of create: 01.03.2026
Date of finished:

Ход работы

# Этап 1: Подготовка и установка


## Установка MkDocs:

## Установить MkDocs: pip install mkdocs
<img width="699" height="695" alt="image" src="https://github.com/user-attachments/assets/e3ad6b53-bbcf-4589-8ad7-d641023596d6" />

## Установить тему Material: pip install mkdocs-material
## Проверить установку: mkdocs --version
<img width="726" height="46" alt="image" src="https://github.com/user-attachments/assets/c72030e7-2400-44b5-8ef3-ef63fb1310ab" />

## Создание нового проекта:

## Создать новую папку для проекта: mkdir my-personal-site
Перейти в папку: cd my-personal-site
Инициализировать MkDocs проект: mkdocs new .
<img width="721" height="211" alt="image" src="https://github.com/user-attachments/assets/73931a7e-a494-4272-8bf8-81fe2ecf5c1f" />

<img width="457" height="45" alt="image" src="https://github.com/user-attachments/assets/d8ec600e-d1d9-4d68-ab8a-0cf410b8d62b" />

## Изучить созданную структуру файлов
<img width="452" height="194" alt="image" src="https://github.com/user-attachments/assets/7f97867d-3ac8-4bfb-9eb6-a47736928e4f" />

# Этап 2: Настройка конфигурации

## Настройка mkdocs.yml:
Открыть файл mkdocs.yml
Настроить базовые параметры:
site_name - название вашего сайта
site_description - описание сайта
site_author - ваше имя
site_url - URL сайта (если планируете публикацию)
<img width="527" height="87" alt="image" src="https://github.com/user-attachments/assets/11be333b-3af1-4620-a4ab-52c61b818b2a" />

## Добавить тему Material: yaml theme: name: material features: - navigation.tabs - navigation.sections - navigation.top - search.highlight - search.share
<img width="643" height="608" alt="image" src="https://github.com/user-attachments/assets/284e80a4-e6ae-4eb0-96ff-abc8a0e4a351" />

## Настройка навигации:

Создать структуру навигации в mkdocs.yml
Добавить разделы: Главная, О себе, Проекты, Контакты
<img width="382" height="219" alt="image" src="https://github.com/user-attachments/assets/a85f02eb-0df1-41e3-9a57-ca13ad48d102" />

# Этап 3: Создание контента

## Главная страница (index.md):

## Страница "О себе" (about.md):



## Страница "Проекты" (projects.md):



## Страница "Контакты" (contacts.md):



# Этап 4: Дополнительные возможности

## Добавление изображений:
Создать папку docs/images/
Добавить свое фото или логотип
Использовать изображения в контенте
<img width="238" height="68" alt="image" src="https://github.com/user-attachments/assets/f6de49cd-3dee-4008-98b2-1b0b241c4803" />

## Настройка поиска:

Убедиться, что поиск включен в конфигурации
Протестировать функциональность поиска
<img width="198" height="75" alt="image" src="https://github.com/user-attachments/assets/6649ac2e-fc82-4e01-a8be-9fc73d9c037e" />
<img width="719" height="395" alt="image" src="https://github.com/user-attachments/assets/89436094-f205-4983-89a8-78361e510c3b" />


## Добавление дополнительных страниц:

## Создать страницу с резюме
## Добавить страницу с достижениями
## Включить блог или заметки (опционально)

# Этап 5: Стилизация и кастомизация

## Настройка цветовой схемы:
## Выбрать цветовую палитру в mkdocs.yml
## Настроить primary и accent цвета

## Добавление логотипа:

## Создать или найти логотип
## Настроить отображение в шапке сайта

## Настройка футера:

## Добавить информацию в футер
## Включить ссылки на социальные сети

# Этап 6: Тестирование и публикация

## Локальное тестирование:
## Запустить локальный сервер: mkdocs serve
## Проверить все страницы и ссылки
## Убедиться в корректности отображения

## Сборка сайта:

## Создать статические файлы: mkdocs build
## Проверить содержимое папки site/

## Публикация (опционально):

## Изучить возможности GitHub Pages
## Настроить автоматическую публикацию
