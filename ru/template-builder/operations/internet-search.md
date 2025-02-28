# Вставка ссылок

{% include [deprecate](../../_includes/deprecate.md) %}

В этом разделе вы узнаете, как добавить обычную ссылку или запрос в поисковой системе и убедиться, что исполнитель по ним прошел. Ссылки можно открывать при наступлении события, объединять в группы и устанавливать им горячие клавиши для более быстрой работы.


## Вставить обычную ссылку {#view.link}

Если вы хотите вставить простую ссылку без дополнительного оформления, то используйте компонент [view.link](../reference/view.link.md). Ссылка будет отображаться подчеркнутым текстом, а после перехода по ней поменяет свой цвет.

```json
{
  "type": "view.link",
  "content": "Текст ссылки",
  "url": "url"
}
```

[![](../_images/buttons/view-example.svg)](https://clck.ru/RvckN)


## Создать поисковой запрос {#helper.search-query}

Вам может понадобиться создать ссылку, которая бы открывала введенный запрос в выбранной поисковой системе. Для этого используйте компонент [helper.search-query](../reference/helper.search-query.md). Список доступных поисковых систем перечислен в свойстве `engine`.

```json
{
  "type": "view.link",
  "content": "Текст ссылки",
  "url": {
    "type": "helper.search-query",
    "query": "текст поискового запроса",
    "engine": "google"
  }
}
```

{% note info %}

Если вам нужно вставить ссылки на несколько поисковых систем с одинаковым запросом, то можно вынести `query` во входные данные, а в коде сослаться на них через `"path": "query"`, чтобы не дублировать запрос.

{% endnote %}


[![](../_images/buttons/view-example.svg)](https://nda.ya.ru/t/pArYIypP3XBTUX)

Если нужной вам поисковой системы нет в свойстве `engine`, то оставьте это поле пустым и введите запрос в `query` с помощью компонента [helper.join](../reference/helper.join.md).

[![](../_images/buttons/view-example.svg)](https://clck.ru/RvdNy)


## Объединить ссылки в группу {#view.link-group}

Чтобы объединить несколько ссылок в группу, используйте компонент [view.link-group](../reference/view.link-group.md). Ссылки будут отображаться подчеркнутым текстом. Одну из ссылок можно выделить рамкой и убрать подчеркивание: для этой ссылки в свойстве `theme` установите значение `primary`.

[![](../_images/buttons/view-example.svg)](https://clck.ru/TYUZE)


## Создать ссылку на кнопке {#action.open-link}

Вы можете оформить ссылку в виде кнопки с помощью компонента [action.open-link](../reference/action.open-link.md). За добавление кнопки отвечает компонент [view.action-button](../reference/view.action-button.md). В свойстве `payload` укажите адрес или компонент [helper.search-query](../reference/helper.search-query.md) с поисковым запросом.

```json
{
  "type": "view.action-button",
  "label": "Текст на кнопке",
  "action": {
    "type": "action.open-link",
    "payload": "url"
  }
}
```

{% note info %}

Чтобы кнопка выглядела аккуратно и не растягивалась на весь экран, пропишите [view.action-button](../reference/view.action-button.md) как элемент массива `items` компонента [view.list](../reference/view.list.md).

{% endnote %}


При добавлении нескольких кнопок можно поменять их расположение с вертикального на горизонтальное в свойстве `direction`.

[![](../_images/buttons/view-example.svg)](https://clck.ru/Rvx2C)

Чтобы назначить кнопке [горячую клавишу](../best-practices/hotkeys.md), используйте компонент [plugin.hotkeys](../reference/plugin.hotkeys.md).

[![](../_images/buttons/view-example.svg)](https://clck.ru/TjrKy)


## Проверить переход по ссылке {#condition.link-opened}

Чтобы убедиться, что исполнитель переходил по ссылке, используйте компонент [condition.link-opened](../reference/condition.link-opened.md), прописав его в свойстве `validation`.

Помните, что условие сработает, только если исполнитель перейдет из интерфейса. Оно не сработает при открытии ссылки через адресную строку.

[![](../_images/buttons/view-example.svg)](https://clck.ru/RveLE)


## Добавить горячие клавиши {#hotkeys}

Для ссылок можно добавить горячие клавиши. Они помогут ускорить работу исполнителя — ссылку можно будет открыть нажатием клавиши на клавиатуре.

Чтобы добавить горячие клавиши, используйте плагин [plugin.hotkeys](../reference/plugin.hotkeys.md). Выберите клавишу и назначьте ей открытие ссылки через [action.open-link](../reference/action.open-link.md).

```json
{
  "type": "plugin.hotkeys",
  "y": {
    "type": "action.open-link",
    "payload": "url"
  }
}
```

[![](../_images/buttons/view-example.svg)](https://clck.ru/Rx3LX)

Подробнее о работе горячих клавиш читайте в разделе [Настройте горячие клавиши](../best-practices/hotkeys.md).


## Открыть ссылку по событию {#plugin.trigger}

Вы можете настроить открытие ссылки при наступлении события. Например, чтобы в зависимости от нажатого переключателя исполнителю открывался определенный поисковый запрос. Для этого используйте плагин [plugin.trigger](../reference/plugin.trigger.md).

[![](../_images/buttons/view-example.svg)](https://clck.ru/Rx5YK)


## Переиспользовать код {#vars}

Как и любое место кода, открытие ссылки и ее адрес можно переиспользовать с помощью конструкции `{"$ref": "path.to.element"}`. Это пригодится при добавлении горячих клавиш: чтобы не дублировать код для визуального отображения ссылки и для [plugin.hotkeys](../reference/plugin.hotkeys.md), его можно один раз прописать в `vars`.

[![](../_images/buttons/view-example.svg)](https://clck.ru/Rx5NP)

Подробнее о переиспользовании читайте в разделе [Переиспользуйте код](../best-practices/reuse.md).


[![](../_images/buttons/contact-support.svg)](../concepts/support.md)
