# Скачать файл

{% include [announce](../_includes/announce.md) %}

Скачивает прикрепленный к ответу в задании файл.

## Запрос {#request}

{% list tabs %}

- Боевая версия

    ```plaintext
    GET https://toloka.dev/api/v1/attachments/<file_id>/download
    Authorization: OAuth <OAuth token>
    ```

- Песочница

    ```plaintext
    GET https://sandbox.toloka.dev/api/v1/attachments/<file_id>/download
    Authorization: OAuth <OAuth token>
    ```

{% endlist %}

## Path-параметры {#path-params}

Параметр | Описание
----- | -----
**file_id** | Идентификатор файла.

## Заголовки {#headers}

{% include [reusables-auth](../_includes/reusables/id-reusables/auth.md) %}

## Ответ {#response}

Файл сохраняется на ваш компьютер.