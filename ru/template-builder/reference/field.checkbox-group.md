# field.checkbox-group

Добавляет группу переключателей с галочками для выбора независимых вариантов ответа. Пригодится, если у вас несколько вариантов. Можно добавить только один переключатель, но это легче сделать с [field.checkbox](field.checkbox.md).

[Посмотреть пример в песочнице](https://clck.ru/T6Vyw).

## Свойства компонента {#properties}

| Название                                            | Тип                                                                                    | Описание                                                                                                                                                                                                                                                                  |
| --------------------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type`<span style="color: red">\*</span>            | "field.checkbox-group"                                                                 | <p>Задает тип компонента.</p>                                                                                                                                                                                                                                             |
| `data`<span style="color: red">\*</span>            | <a class="xref popup-link" href="../concepts/types.dita#types/writable">writable</a>   | <p>Данные, значения которых будут обработаны или изменены.</p>                                                                                                                                                                                                            |
| `label`                                             | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Надпись над компонентом.</p>                                                                                                                                                                                                                                           |
| `disabled`                                          | <a class="xref popup-link" href="../concepts/types.dita#types/boolean">boolean</a>     | <p>Если `true`, переключатели неактивны.</p>                                                                                                                                                                                                                              |
| `hint`                                              | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Текст подсказки.</p>                                                                                                                                                                                                                                                   |
| `options`<span style="color: red">\*</span>         | <a class="xref popup-link" href="../concepts/types.dita#types/array">array</a>         | <p>Массив переключателей, где `value` — изменяемое значение, а `label` — текст возле переключателя.</p>                                                                                                                                                                   |
| `options[]`                                         | <a class="xref popup-link" href="../concepts/types.dita#types/object">object</a>       | <p>Переключатель.</p>                                                                                                                                                                                                                                                     |
| `options[].hint`                                    | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Текст с дополнительной информацией об опции.</p>                                                                                                                                                                                                                       |
| `options[].label`<span style="color: red">\*</span> | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Текст рядом с переключателем.</p>                                                                                                                                                                                                                                      |
| `options[].value`<span style="color: red">\*</span> | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Возвращаемое значение.</p>                                                                                                                                                                                                                                             |
| `preserveFalse`                                     | <a class="xref popup-link" href="../concepts/types.dita#types/boolean">boolean</a>     | <p>Свойство указывающее, надо ли возвращать значения `false` в результатах. По умолчанию, если компонент возвращает `false`, то в выходные данные этот результат не будет добавлен. Чтобы в результаты добавлялись значения `false`, укажите `"preserveFalse": true`.</p> |
| `validation`                                        | <a class="xref popup-link" href="../concepts/types.dita#types/condition">condition</a> | <p>Валидация на основе условия <em>(condition)</em>.</p>                                                                                                                                                                                                                  |