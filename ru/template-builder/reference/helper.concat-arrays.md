# helper.concat-arrays

{% include [deprecate](../../_includes/deprecate.md) %}

Объединение нескольких массивов в один.

Например, у вас есть несколько массивов:

```json
([1, 2, 3], [4, 5, 6], [7, 8, 9])
```

Их элементы можно объединить в один массив, чтобы показать одновременно:

```json
[1, 2, 3, 4, 5, 6, 7, 8, 9]
```

[![](../_images/buttons/view-example.svg)](https://clck.ru/QRfHv)

## Свойства компонента {#properties}

#|
|| **Название** | **Тип** | **Описание** ||
|| `type`<span style="color: red">\*</span> | "helper.concat-arrays" | Задает тип компонента. ||
|| `items` | _array_ | Массивы, которые нужно объединить. ||
|| `items[]` | _any_ | Элемент массива. ||
|#
