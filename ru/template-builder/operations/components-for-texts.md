# Компоненты для работы с текстом

{% include [deprecate](../../_includes/deprecate.md) %}

В этом разделе мы расскажем, как [отобразить текст](#insert-text), [добавить поле для ввода текста](#field-text), а также какие компоненты позволяют [менять текст](#text-transform).


## Отобразить текст {#insert-text}

Для отображения текста в интерфейсе задания используйте компонент [view.text](../reference/view.text.md). В свойстве `content` вставьте необходимый текст или укажите компонент с типом [data.*](work-with-data.md), который его возвращает.

{% list tabs %}

- Из входных данных

  Чтобы подставить текст из входных данных, используйте компонент `data.input`.

  [![](../_images/buttons/view-example.svg)](https://clck.ru/R6TpZ)

- Из выходных данных

  Чтобы подставить текст из выходных данных, используйте компонент `data.output`.

  [![](../_images/buttons/view-example.svg)](https://clck.ru/R6TqN)

{% endlist %}

Если вы хотите вставить отформатированный текст, посмотрите инструкцию и примеры в разделе [Форматирование текста](text-formatting.md).


## Добавить поле для ввода текста {#field-text}

Чтобы добавить поле для ввода однострочного текста, используйте компонент [field.text](../reference/field.text.md), для многострочного — [field.textarea](../reference/field.textarea.md).

[![](../_images/buttons/view-example.svg)](https://clck.ru/R6Tqr)

## Изменить текст {#text-transform}

Чтобы изменить текст, например, сделать все буквы большими или подставить значение переменной, используйте следующие компоненты:

- [helper.text-transform](../reference/helper.text-transform.md) — позволяет менять регистр. Для преобразования текста в свойстве `transformation` укажите соответствующее значение:
    - `uppercase` — сделает все буквы заглавными.
    - `lowercase` —сделает все буквы строчными.
    - `capitalize` — сделает первую букву текста заглавной, а все последующие — строчными.

  [![](../_images/buttons/view-example.svg)](https://clck.ru/R6Ts8)

- [helper.replace](../reference/helper.replace.md) — позволяет заменить одни части строки на другие. Для этого укажите в свойстве `find` значение, которое будет заменено на значение свойства `replace`.

  [![](../_images/buttons/view-example.svg)](https://clck.ru/R6PD2)

- [helper.join](../reference/helper.join.md) — позволяет соединить несколько строк в одну, в том числе через пробел или запятую.

  [![](../_images/buttons/view-example.svg)](https://clck.ru/R6Tsa)

[![](../_images/buttons/contact-support.svg)](../concepts/support.md)
