# condition.played-fully

Компонент проверяет окончание воспроизведения. Валидация пройдет, если воспроизведение закончено. Для воспроизведения медиа с проверкой `condition.played-fully` можно использовать [view.audio](view.audio.md) и [view.video](view.video.md). `condition.played-fully` работает только в свойстве `validation` плеера.

[Посмотреть пример в песочнице](https://clck.ru/QPXvo).

## Свойства компонента {#properties}

| Название                                 | Тип                                                                              | Описание                                                          |
| ---------------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| `type`<span style="color: red">\*</span> | "condition.played-fully"                                                         | <p>Задает тип компонента.</p>                                     |
| `hint`                                   | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a> | <p>Сообщение об ошибке валидации, которое увидит пользователь</p> |