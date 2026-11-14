## API Yatube final
API проекта для публикаций, создания комментариев пользователей

## Установка
1. Создайте и активируйте виртуальное окружение в папке проекта
2. Установите зависимости из файла: `pip install -r requirements.txt`.
3. Перейдите в папку `yatube_api`.
4. Выполните миграции: `python manage.py migrate`.
5. Запустите сервер: `python manage.py runserver`.

## Получение JWT-токена
Отправьте POST-запрос на `/api/v1/jwt/create/` с полями `username` и `password`.
Для авторизованных запросов передавайте также заголовок `Authorization: Bearer <access-токен>`.

## Примеры эндпоинтов
- `GET, POST /api/v1/posts/`
- `GET, PUT, PATCH, DELETE /api/v1/posts/{post_id}/`
- `GET /api/v1/groups/`
- `GET /api/v1/posts/{post_id}/comments/`
- `GET, POST /api/v1/follow/`
