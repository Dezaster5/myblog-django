# Проект MyBlog

**MyBlog** — это платформа для ведения блогов, созданная на основе Django. Она позволяет пользователям создавать, управлять и делиться своими постами. Проект включает такие функции, как работа с тегами, поиск, комментарии и пагинация.

## Основные функции

- **Управление постами**: Создание, редактирование и удаление постов.
- **Система тегов**: Организация постов с использованием тегов (реализовано через `django-taggit`).
- **Поддержка Markdown**: Написание постов с использованием Markdown для удобного форматирования.
- **Комментарии**: Возможность добавлять комментарии к постам.
- **Поиск**: Полнотекстовый поиск с использованием триграммного сходства для точных результатов.
- **Пагинация**: Удобное отображение постов с разделением на страницы.
- **Адаптивный дизайн**: Шаблоны оптимизированы для различных экранов.

## Требования

Для работы проекта необходимы следующие зависимости:

- Python 3.8 или выше
- Django 4.2.16
- PostgreSQL (рекомендуется)

Установить зависимости можно с помощью команды:

```bash
pip install -r requirements.txt
```

## Установка и настройка

1. **Клонирование репозитория**:
```bash
git clone https://github.com/Dezaster5/myblog-django.git
cd myblog
```

2. **Установка зависимостей**:
```bash
pip install -r requirements.txt
```

3. **Настройка переменных окружения**: Скопируйте файл `.env.sample` в `.env` и укажите необходимые значения:
```bash  
cp .env.sample .env
```
   
4. **Применение миграций**:
```bash
python manage.py migrate
```

5. **Загрузка демонстрационных данных** (опционально):
```bash
python manage.py loaddata myblog_data.json
```

6. **Запуск сервера разработки**:
```bash
python manage.py runserver
```

Приложение будет доступно по адресу http://127.0.0.1:8000/.

## Структура проекта

- **`blog`**: Основное приложение с моделями, представлениями, шаблонами и формами.
- **`myblog`**: Настройки проекта, маршруты и конфигурации.
- **Шаблоны**: Кастомные HTML-шаблоны с возможностью повторного использования.

## Основной функционал

- **Список постов**:
    - Отображение списка постов с пагинацией.
    - Фильтрация постов по тегам.
	
- **Поиск**:
    - Полнотекстовый поиск через `TrigramSimilarity`.
	
- **Комментарии**:
    - Добавление, редактирование и управление комментариями.# myblog-django
