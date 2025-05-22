# ЛР 7-8: Java-сервис: JavaServiceSteamsMessages

---

## 1. Запуск проекта

### 1.1 Сборка и запуск контейнеров

```bash
docker-compose up --build
```

## 2. Интерфейсы и доступы

| Сервис        | URL                                              | Описание                              |
|---------------|--------------------------------------------------|----------------------------------------|
| Swagger UI    | http://localhost:8080/swagger-ui/index.html      | Документация и тестирование API       |
| Postman       | —                                                | Используйте коллекцию postman_collection.json |
| Actuator      | http://localhost:8080/actuator                   | Health-check и метрики Spring Boot    |
| Prometheus    | http://localhost:9090/targets                    | Интерфейс Prometheus                  |
| Grafana       | http://localhost:3000                            | Визуализация метрик                   |
|               | Логин: admin, Пароль: admin              |                                        |

---

## 3. Тестирование API

### 3.1 Через Swagger UI
1. Откройте:  
   http://localhost:8080/swagger-ui/index.html
2. Тестируйте эндпоинты прямо в браузере.

### 3.2 Через Postman
1. Откройте Postman.
2. Импортируйте коллекцию [collection.postman_collection.json](./collection.postman_collection.json).
3. Используйте готовые запросы для проверки API.

---

## 4. Мониторинг и метрики

### 4.1 Spring Boot Actuator
- Общая информация:  
  GET http://localhost:8080/actuator

### 4.2 Prometheus
1. Проверка статусов таргетов:  
   http://localhost:9090/targets

### 4.3 Grafana
1. Перейдите: http://localhost:3000
2. Авторизуйтесь:  
   Логин: admin  
   Пароль: admin
3. Импортируйте дашборд из [grafana.json](./grafana/grafana.json).

---

## 5. Проверка работоспособности
Все ОК, если:
- Сервис доступен через Swagger/Postman.
- Health-check возвращает {"status": "UP"}.
- Prometheus отображает цель actuator/prometheus как UP.
- Grafana показывает метрики на дашборде.

---

## 6. Остановка проекта
```bash
docker-compose down
```