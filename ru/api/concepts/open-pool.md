# Открыть пул

{% include [announce](../_includes/announce.md) %}

Открывает пул.

Задания будут доступными для исполнителей, только если пул открыт.

В результате запроса создается операция. Чтобы отслеживать ход операции, отправьте запрос к ресурсу `/operations`.

## Запрос {#request}

{% list tabs %}

- Боевая версия

    ```bash
    POST https://toloka.dev/api/v1/pools/<pool_id>/open
    Authorization: OAuth <OAuth token>
    ```

- Песочница

    ```bash
    POST https://sandbox.toloka.dev/api/v1/pools/<pool_id>/open
    Authorization: OAuth <OAuth token>
    ```

{% endlist %}

## Path-параметры {#path-params}

Параметр | Описание
----- | -----
**pool_id** | Идентификатор пула.

## Заголовки {#headers}

{% include [reusables-auth](../_includes/reusables/id-reusables/auth.md) %}

## Ответ {#response}

{% note info %}

Если пул уже открыт, то возвращается пустой ответ со статусом 204.

Если пул не может быть открыт, то возвращается ответ с описанием ошибки и статусом 409.

{% endnote %}

```json
{
  "id": "fadfe3jk-fdafue2-fda32890-fdafdi23",
  "type": "POOL.OPEN",
  "status": "PENDING",
  "submitted": "2015-22-12T14:18:35",
  "started" : "2016-04-07T16:06:15.902",
  "finished" : "2016-04-07T16:06:15.902",
  "progress" : 100,
  "parameters": {
    "pool_id": "21"
  }
}
```

#|
||**Параметр** | **Описание**||
||**id** | **string**

Идентификатор операции.||
||**type** | **string**

Тип операции: `POOL.OPEN` — открытие пула.||
||**status** | **string**

Статус операции:

- `PENDING` — выполнение не началось;
- `RUNNING` — выполняется;
- `SUCCESS` — успешно выполнена;
- `FAIL` — не выполнена.
||
||**submitted** | **string**

Дата и время отправки запроса по UTC в формате ISO 8601: `YYYY-MM-DDThh:mm:ss[.sss]`.||
||**started** | **string**

Дата и время начала операции по UTC в формате ISO 8601: `YYYY-MM-DDThh:mm:ss[.sss]`.||
||**finished** | **string**
Дата и время окончания операции по UTC в формате ISO 8601: `YYYY-MM-DDThh:mm:ss[.sss]`.||
||**progress** | **integer**
Ход выполнения операции в процентах.||
||**parameters.pool_id** | **string**
Идентификатор пула.||
|#