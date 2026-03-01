University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)
Year: 2025/2026
Group: U4125
Author: Исайкин Евгений Дмитриевич @euiskn
Lab: Lab3
Date of create: 01.03.2026
Date of finished:

Настройка мониторинга с Prometheus и Grafana:

# Создание конфигурации Prometheus:

## Создать папку prometheus для конфигурации

## Создать файл prometheus/prometheus.yml

# Запуск Node Exporter:

## Запустить контейнер Node Exporter для сбора системных метрик:
<img width="602" height="314" alt="image" src="https://github.com/user-attachments/assets/5652222e-0a1a-4db7-9e79-a961fbf0c738" />

## Проверить работу: curl http://localhost:9100/metrics
<img width="728" height="275" alt="image" src="https://github.com/user-attachments/assets/7b0b94a7-f678-4c2a-9a4d-a02fd09d4b35" />

# Запуск Prometheus:

## Создать том для данных Prometheus:

docker volume create prometheus-data
##  Prometheus - приложение, которое отвечает за сбор метрик. Для их визуализации позже будет запущено другое приложение - Grafana. Чтобы они могли работать вместе, нужно создать для них общую сеть:
docker network create monitoring
<img width="587" height="59" alt="image" src="https://github.com/user-attachments/assets/55027e96-11c0-4d72-adbd-c6fcd0288b8f" />

## Выйти на папку выше в консоли, убедиться что вы находитесь над уровнем папки prometheus. Запустить контейнер Prometheus:
<img width="638" height="451" alt="image" src="https://github.com/user-attachments/assets/2c587d67-4ca8-447d-b86e-23fee5fec41f" />

## Проверить работу: открыть http://localhost:9090 в браузере
<img width="720" height="402" alt="image" src="https://github.com/user-attachments/assets/7b67e2f1-463b-4530-9c57-6f6187a001e3" />

# Запуск Grafana:

## Создать том для данных Grafana:

docker volume create grafana-data
## Запустить контейнер Grafana:
<img width="709" height="541" alt="image" src="https://github.com/user-attachments/assets/d1c132c9-9a47-4fb4-bc43-ea3ad54e6f2e" />

## Проверить работу: открыть http://localhost:3000 в браузере (логин: admin, пароль: admin)
<img width="714" height="710" alt="image" src="https://github.com/user-attachments/assets/01dc0df4-009a-4983-a53b-324a46c11a4a" />

# Настройка Grafana:

## Войти в Grafana (admin/admin)
<img width="716" height="703" alt="image" src="https://github.com/user-attachments/assets/e235afe2-3a42-4182-a4db-aafb3933e93f" />

## Добавить источник данных Prometheus:
Configuration → Data Sources → Add data source
Выбрать Prometheus
URL: http://prometheus:9090
Save & Test
<img width="718" height="155" alt="image" src="https://github.com/user-attachments/assets/9c6e9e5e-77a0-408f-814f-943f1a6f0151" />

## Создать дашборд:
Create → Dashboard → Add visualization
Выбрать источник данных Prometheus
Добавить метрику: node_cpu_seconds_total
Сохранить дашборд
<img width="725" height="783" alt="image" src="https://github.com/user-attachments/assets/be4439fc-17bc-4bc8-8f45-964b7be65d48" />

# Тестирование системы:

## Проверить все контейнеры: docker ps
<img width="724" height="135" alt="image" src="https://github.com/user-attachments/assets/ce938af2-bdb5-4d95-adcc-e16d2d8945c3" />

## Открыть Prometheus и убедиться, что метрики собираются
<img width="721" height="592" alt="image" src="https://github.com/user-attachments/assets/93540a6a-31cb-48a6-b4d0-a63c8915c9f3" />
<img width="726" height="261" alt="image" src="https://github.com/user-attachments/assets/f8c0c424-f7a6-415d-86c8-3244bef8cbaa" />

## Открыть Grafana и проверить отображение графиков
<img width="722" height="448" alt="image" src="https://github.com/user-attachments/assets/e3dc1648-5b35-423d-9585-712f7eff3b2e" />

## Создать несколько графиков для разных метрик (CPU, память, диск)
<img width="1151" height="624" alt="image" src="https://github.com/user-attachments/assets/1632d8b6-20cc-45d5-8097-77c545d68e5a" />
