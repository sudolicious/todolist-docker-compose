ToDoList - приложение для управления списком задач.

Функционал:
- Добавление новых задач;
- Просмотр списка всех задач;
- Выделение задачи выполненной;
- Удаление задачи

![ToDoList Preview](https://github.com/sudolicious/todolist/blob/main/frontend/public/Screenshot.png?raw=true)

Технологии:
Frontend: React c Typescript
Backend: Golang
База данных: PostgreSql
Контейнеризация: Docker

Требования:
Docker (версия 20.10.0+)
Docker Compose (версия 1.29.0+)
Git (для клонирования репозитория)

Установка и запуск.

1. Клонирование репозитория
git clone https://github.com/sudolicious/todolist-docker-compose.git

2. Скопируйте файлы .env.example и заполните
cd todolist-docker-compose
cp .env.example .env # заполните переменные для БД
cd backend 
cp .env.example .env # заполните переменные для БД

3. Соберите и запустите приложение
cd todolist-docker-compose
docker-compose up --build -d

4. Откройте приложение
Фронтенд: http://localhost:3000
Бэкенд API: http://localhost:3000/api/tasks

Структура проекта
todolist-docker-compose/
├── ├── backend/          # Go-бэкенд
│   ├── Dockerfile        # Dockerfile для бэкенда
│   └── .env.example      # Пример файла с переменными окружения для бэкенда
│   └── migrations/       # Миграции БД
│
├── frontend/             # React-приложение
│   ├── src/              # Исходные файлы фронтенда
│   ├── public/           # Статические файлы
│   ├── Dockerfile        # Dockerfile для фронтенда
│   └── package.json      # Зависимости React
│
├── openapi.yml           # OpenAPI спецификация
├── docker-compose.yml    # Основной файл конфигурации Docker Compose
└── README.md             # Этот файл
