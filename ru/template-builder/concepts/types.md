# Типы свойств

{% include [deprecate](../../_includes/deprecate.md) %}

В описаниях компонентов у каждого свойства указан тип. На этой странице собраны пояснения к этим типам.

#### "component.name"
Для свойства `type` везде указывается название компонента. Если указать другое название, то это будет уже другой компонент.
#### action
Любой [компонент действия](../reference/actions.md). Компоненты с именем `actions.*` позволяют выполнять различные действия, например показывать уведомления.
#### any

Любое значение. Это могут быть:
- Стандартные элементы JSON: строка, число, `true`, `false`, объект или массив.
- [Хелперы](../reference/helpers.md), возвращающие значение.
- Другие компоненты, если это допустимо конфигурацией.
- Ссылки на другое место в конфигурации с помощью конструкции `{ "$ref": "path.to.element" }`. Такие ссылки [позволяют переиспользовать](../best-practices/reuse.md) уже написанный код.

#### array

Массив элементов, разделенных запятой. Элементом может быть что
{% cut "угодно" %}

Любое значение. Это могут быть:
- Стандартные элементы JSON: строка, число, `true`, `false`, объект или массив.
- [Хелперы](../reference/helpers.md), возвращающие значение.
- Другие компоненты, если это допустимо конфигурацией.
- Ссылки на другое место в конфигурации с помощью конструкции `{ "$ref": "path.to.element" }`. Такие ссылки [позволяют переиспользовать](../best-practices/reuse.md) уже написанный код.

{% endcut %}

. Массив выделяется квадратными скобками `[]`:

```json
"cities": ["Moscow", "Tokyo", "New York"]
```

#### boolean
Логическое значение без кавычек: `true` (истина) или `false` (ложь).
#### condition
Любой компонент [условия](../reference/conditions.md). Компоненты с именем `conditions.*` позволяют проверять, соответствует ли выражение какому-то условию. Например, чтобы проверить, что поле с текстом заполнено.
#### integer
Целое число без кавычек, например `25`.
#### number
Число без кавычек, например `25.5`.
#### object
Список пар `"ключ": значение`, разделенных запятой. Выделяется фигурными скобками `{}`.
```json
{
  "name": "John",
  "surname": "Smith"
}
```

#### ref

Указатель на визуальный компонент в виде конструкции `{ "$ref": "path.to.element" }`.

.

{% note info %}

Список компонентов, на которые можно ссылаться, может быть ограничен. Например, [action.play-pause](../reference/action.play-pause.md) работает только с компонентами, которые позволяют проиграть аудио или видео.

{% endnote %}


#### string
Cтрока, выделяется кавычками, например `"Hello world"`.
#### writable
Компонент, в который можно записывать данные: `data.internal` или `data.output`. В некоторых компонентах можно использовать `data.relative`. [Подробнее об этих компонентах](../operations/work-with-data.md).
#### visual
Визуальный компонент (`layout.*`, `view.*`, `field.*`) или [хелпер](../reference/helpers.md), который его возвращает. Список см. в [справочнике компонентов](../reference/index.md).
