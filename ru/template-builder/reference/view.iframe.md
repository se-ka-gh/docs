# view.iframe

Отображает веб-страницу по URL-адресу во встроенном окне.

## Свойства компонента {#properties}

| Название                                 | Тип                                                                                    | Описание                                                                                                                                                                 |
| ---------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `type`<span style="color: red">\*</span> | "view.iframe"                                                                          | <p>Задает тип компонента.</p>                                                                                                                                            |
| `label`                                  | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Надпись над компонентом.</p>                                                                                                                                          |
| `fullHeight`                             | <a class="xref popup-link" href="../concepts/types.dita#types/boolean">boolean</a>     | <p>Если `true`, элемент занимает все свободное пространство по вертикали. При этом элементу устанавливается минимальная высота 400 пикселей.</p>                         |
| `hint`                                   | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Текст подсказки.</p>                                                                                                                                                  |
| `maxWidth`                               | <a class="xref popup-link" href="../concepts/types.dita#types/number">number</a>       | <p>Максимальная ширина элемента в пикселях, которая не может быть меньше `minWidth`.</p>                                                                                 |
| `minWidth`                               | <a class="xref popup-link" href="../concepts/types.dita#types/number">number</a>       | <p>Минимальная ширина элемента в пикселях. Имеет приоритет над `maxWidth`.</p>                                                                                           |
| `ratio`                                  | <a class="xref popup-link" href="../concepts/types.dita#types/array">array</a>         | <p>Массив из двух чисел, устанавливающий относительные размеры сторон: ширины (первое число) к высоте (второе число).</p><p>Не действует, если `"fullHeight": true`.</p> |
| `ratio[]`                                | <a class="xref popup-link" href="../concepts/types.dita#types/number">number</a>       | <p>Относительный размер одной стороны.</p>                                                                                                                               |
| `url`<span style="color: red">\*</span>  | <a class="xref popup-link" href="../concepts/types.dita#types/string">string</a>       | <p>Адрес веб-страницы.</p>                                                                                                                                               |
| `validation`                             | <a class="xref popup-link" href="../concepts/types.dita#types/condition">condition</a> | <p>Валидация на основе условия <em>(condition)</em>.</p>                                                                                                                 |