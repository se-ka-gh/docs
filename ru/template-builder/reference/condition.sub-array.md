# condition.sub-array

{% include [deprecate](../../_includes/deprecate.md) %}

Проверяет, что массив в `data` является подмассивом для `parent`.

[![](../_images/buttons/view-example.svg)](https://clck.ru/T9a4k)

## Свойства компонента {#properties}

#|
|| **Название** | **Тип** | **Описание** ||
|| `type`<span style="color: red">\*</span> | "condition.sub-array" | Задает тип компонента. ||
|| `data` | _any_ | Подмассив, наличие которого проверяется в `parent` ||
|| `hint` | _string_ | Сообщение об ошибке валидации, которое увидит исполнитель ||
|| `parent` | _any_ | Массив, в котором осуществляется поиск `data` ||
|#
