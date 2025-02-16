# Тестовое задание для стажёра Frontend-направления
# (зимняя волна 2025)
Техническое задание можно найти здесь – [Техническое задание](https://github.com/avito-tech/tech-internship/blob/main/Tech%20Internships/Frontend/Frontend-trainee-assignment-winter-2025/Frontend-trainee-assignment-winter-2025.md)

# Запуск проекта
1. Клонирование репозитория в IDE
```bash
   git clone https://github.com/temaaaar/Frontend-Trainee-Assignment.git
```
## Сервер
- Файл .env.example предоставлен в репозитории в качестве шаблона. Перед запуском **сервера** его необходимо переименовать в .env и заменить <PASSWORD> на реальный пароль ```"ruGpHbZ5Ga1G2NI9"``` от базы данных MongoDB.
- Пароли пользователей хранятся в зашифрованном виде с использованием BcryptJS.

## Пояснение
> Данные объявлений и пользователей хранятся в базе данных MongoDB, доступ к которой осуществляется через Mongoose.
Такое решение мне показалось более корректным ввиду наличия необходимости реалиизовать также и авторизацию, поэтому API было расширено для поддержки CRUD-операций с объявлениями и пользователями.
> Пароли пользователей хранятся в безопасном виде с использованием BcryptJS.

```bash

   cd  Server
   npm install
   npm start

```
## Клиент

```bash

   cd  Client
   npm install
   npm start
   
```
- Клиент работает на PORT=2999, сервер на PORT=3000.
- С помощью docker compose: (docker compose build, затем docker compose up)

# Технический стек
### Клиент
- React, TypeScript – создание интерфейса, типизация
- MaterialUI – UI-компоненты и стилизация
- React Router Dom – маршрутизация страниц
- Redux – управление состоянием приложения
- Axios – HTTP-запросы к API

### Сервер
- Express – основной фреймворк
- MongoDB, Mongoose – база данных и ORM для работы с MongoDB
- CORS – управление политиками безопасности для API
- Body-Parser – обработка данных в запросах
- JWT – аутентификация пользователей с токенами
- BcryptJS – хеширование паролей
- Dotenv (dotenv) – управление переменными окружения

### Разработка и тестирование
- Nodemon – автоматический перезапуск сервера при изменениях кода
- ESLint – линтинг кода
- Prettier – автоформатирование кода
- Vite – инструмент для сборки и разработки
- Jest – тестирование
- Testing Library – тестирование компонентов
- MSW – мокирование API-запросов

### Маршрутизация
- /form — для размещения объявлений
- /form/:id — для редактирования объявления с предзаполненной формой
- /list — для отображения списка объявлений
- /item/:id — для просмотра конкретного объявления
- /register — регистрация пользователя
- /login — авторизация пользователя

### В проекте реализованы
- Размещение, редактирование и удаление объявлений
- Отображение всех размещённых объявлений
- Отображение всех объявлений, созданных авторизованным пользователем
- Возможность просмотра конкретного объявления
- Валидация полей
- Поиск объявлений по названию с историей поиска и возможностью удаления отдельных записей
- Пагинация
- Фильтрация объявлений по категориям (с категорийными фильтрами)
- Автосохранение черновика объявления, привязанного к пользователю, при перезагрузке страницы
- Регистрация, авторизация пользователей
- Валдиация полей размещения объявления и регистрации
- Хранение объявлений и пользователей в MongoDB
- Юнит-тестирование
- Обработка ошибки 404
- Возможность запуска проекта при помощи docker compose

