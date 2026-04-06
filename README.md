# Task Manager (Spring Boot)

Простой REST API для управления задачами, реализованный на Java с использованием Spring Boot.

---

## Функционал

* Создание задачи
* Получение списка всех задач
* Получение задачи по ID
* Обновление задачи
* Удаление задачи
* Фильтрация задач по статусу

---

## Технологии

* Java
* Spring Boot
* Spring Web
* Spring Data JPA
* H2 Database

---

## Структура проекта

```
controller/   # REST контроллеры
service/      # бизнес-логика
repository/   # работа с БД
model/        # сущности (Task)
```

---

## Запуск проекта

### 1. Клонировать репозиторий

```
git clone <your-repo-url>
```

### 2. Перейти в папку проекта

```
cd task-manager
```

### 3. Запустить приложение

Через IntelliJ IDEA или командой:

```
mvn spring-boot:run
```

---

## API эндпоинты

### Создать задачу

```
POST /tasks
```

Пример JSON:

```json
{
  "title": "Learn Java",
  "description": "Prepare for interview",
  "status": "TODO",
  "priority": "HIGH"
}
```

---

### Получить все задачи

```
GET /tasks
```

---

### Получить задачу по ID

```
GET /tasks/{id}
```

Пример:

```
GET /tasks/1
```

---

### Обновить задачу

```
PUT /tasks/{id}
```

---

### Удалить задачу

```
DELETE /tasks/{id}
```

---

### Фильтр по статусу

```
GET /tasks/status/{status}
```

Пример:

```
GET /tasks/status/TODO
```

---

## База данных

Используется встроенная база данных H2.

Консоль доступна по адресу:

```
http://localhost:8080/h2-console
```

Параметры подключения:

* JDBC URL: `jdbc:h2:mem:testdb`
* User: `sa`
* Password: *(пусто)*

---

## Цель проекта

Проект создан для изучения:

* Spring Boot
* REST API
* работы с базой данных
* базовой архитектуры backend-приложения

---

## Примечание

Проект является учебным и демонстрирует базовые принципы разработки backend-приложений на Java.

---
