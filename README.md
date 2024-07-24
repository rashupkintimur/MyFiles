# Проект My Files

"My Files" - Облачное хранилище файлов. Проект выполняет различные операции через HTTP-запросы. Ниже перечислены доступные конечные точки и их функциональность.

## возможные HTTP-запросы

### HTTP-запросы для пользователей

- **GET /users/list**
  - Получить список пользователей (массив) с ограниченным количеством полей данных пользователя (возраст, пол и т.д.).

- **GET /users/get/{id}**
  - Получить информацию о конкретном пользователе по его ID.

- **POST /users/update**
  - Обновить профиль авторизованного пользователя.

### HTTP-запросы для администратора

- **GET /admin/users/list**
  - Получить список всех пользователей.

- **GET /admin/users/get/{id}**
  - Получить информацию о конкретном пользователе по его ID.

- **POST /admin/users/delete/{id}**
  - Удалить пользователя по его ID.

- **POST /admin/users/update/{id}**
  - Обновить информацию о пользователе по его ID.

### HTTP-запросы для для файлов

- **GET /files/list**
  - Получить список всех файлов.

- **GET /files/get/{id}**
  - Получить информацию о конкретном файле по его ID.

- **POST /files/add**
  - Добавить новый файл.

- **POST /files/rename**
  - Переименовать существующий файл.

- **POST /files/delete/{id}**
  - Удалить файл по его ID.

### HTTP-запросы для для директорий

- **POST /directories/add**
  - Добавить новую директорию.

- **POST /directories/rename**
  - Переименовать существующую директорию.

- **GET /directories/get/{id}**
  - Получить информацию о конкретной директории, включая список файлов в ней.

- **POST /directories/delete/{id}**
  - Удалить директорию по её ID.

### HTTP-запросы для для обмена файлами

- **GET /files/share/{id}**
  - Получить список пользователей, имеющих доступ к конкретному файлу.

- **POST /files/share/{id}/{user_id}**
  - Предоставить пользователю доступ к конкретному файлу.

- **POST /files/share/delete/{id}/{user_id}**
  - Прекратить доступ пользователя к конкретному файлу.

## Начало работы

### Требования
- PHP 7.4 или выше
- Веб-сервер (например, Apache, Nginx)
- Composer для управления зависимостями
- MySQL

### Установка

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/rashupkintimur/my_files.git
    ```
2. Перейдите в директорию проекта:
    ```bash
    cd my_files
    ```
3. Установите зависимости:
    ```bash
    composer install
    ```

### Конфигурация
1. Скопируйте файл `template.env.php` в `env.php` и обновите необходимые настройки:
    ```bash
    cp template_env.php env.php

### Использование

Запустите встроенный сервер PHP:
```bash
php -S localhost:8000
