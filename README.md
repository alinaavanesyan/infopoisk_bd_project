# infopoisk_bd_project


# Lyrics Search API

## Описание

API для поиска песен в корпусе текстов песен. Поддерживаются два метода поиска: `TF-IDF` и `BERT`.

### Эндпоинты

1. **GET /search/methods/** - Возвращает доступные методы поиска.
2. **GET /corpus/info/** - Возвращает информацию о корпусе.
3. **POST /search/** - Выполняет поиск по запросу.

### Запуск проекта

1. Установите зависимости:

    ```bash
    pip install -r requirements.txt
    ```

2. Запустите приложение:

    ```bash
    uvicorn main:app --reload
    ```

3. Запуск через Docker:

    ```bash
    docker build -t lyrics-search-api .
    docker run -p 8000:8000 lyrics-search-api
    ```

### Форматы запросов и ответов

#### Пример запроса:

```json
{
  "query": "love song",
  "top_n": 10,
  "method": "tfidf"
}
