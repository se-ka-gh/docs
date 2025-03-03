# view.list

{% include [deprecate](../../_includes/deprecate.md) %}

Блок для отображения данных списком.

## Свойства компонента {#properties}

#|
|| **Название** | **Тип** | **Описание** ||
|| `type`<span style="color: red">\*</span> | "view.list" | Задает тип компонента. ||
|| `label` | _string_ | Надпись над компонентом. ||
|| `direction` | _string_ | Определяет направление списка:

- `vertical` (по умолчанию) — вертикальный список
- `horizontal` — горизонтальный список. ||
  || `hint` | _string_ | Текст подсказки. ||
  || `items`<span style="color: red">\*</span> | _array_ | Массив элементов списка. ||
  || `items[]` | _view_ | Элемент списка. ||
  || `rtl` | _object_ | Тексты на арабском, иврите и некоторых других языках принято писать слева направо. Используйте это свойство, чтобы задать правильный режим отображения для компонента.

[![](../_images/buttons/view-example.svg)](https://clck.ru/amHBJ)

[Подробнее про RTL-языки](https://www.w3.org/International/questions/qa-scripts).
||
|| `rtl.mode` | _string_ | Режим отображения:

- `ltr` — слева направо;
- `rtl` — справа налево.

Выбранное значение подставится в атрибут `dir` в HTML-коде компонента. [Подробнее про свойство dir](https://www.w3.org/International/questions/qa-html-dir). ||
|| `size` | _string_ | Определяет размер отступов между элементами. Доступные значения по возрастанию: `s`, `m` (значение по умолчанию). ||
|| `validation` | _condition_ | Валидация на основе условия _(condition)_. ||
|#
