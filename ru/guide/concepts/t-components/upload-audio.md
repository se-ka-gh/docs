# Кнопка для записи и загрузки аудио

{% include [deprecate](../../../_includes/deprecate.md) %}

{% note info %}

Справочник по настройке интерфейса описывает работу редактора HTML/JS/CSS. Вы также можете попробовать создать кнопку для загрузки аудио в {% if locale == "ru-ru" %}[Конструкторе шаблонов](../../../template-builder/reference/field.audio.md){% endif %}{% if locale == "en-com" %}[Template Builder](../../../../en/docs/template-builder/reference/field.audio.md){% endif %}.

{% endnote %}

Чтобы добавить в задание кнопку для записи и загрузки аудио, используйте компонент `{{field type="file" sources="RECORDER" fileType="AUDIO" name="<название выходного поля>" sources="<параметр sources>" fileType="<параметр fileType>"}}`. Например:

{% if locale == "ru-ru" %}

```plaintext
{{field type="file" name="result" sources="RECORDER" fileType="AUDIO" label="Записать аудио"}}
```

{% endif %}{% if locale == "en-com" %}

```plaintext
{{field type="file" name="result" sources="RECORDER" fileType="AUDIO" label="Record audio"}}
```

{% endif %}

Полный список параметров см. в [таблице](#parametry).

В описании [выходных данных](../incoming.md) добавьте поле с типом `file`. Например:

```json
{
  "result": {
    "type": "file",
    "required": true
  }
}
```

Задания с кнопкой для записи и загрузки аудио запускайте для мобильных устройств, так как на них есть встроенный диктофон. В [пуле](../../../glossary.md#pool) установите [фильтр](../filters.md) **Клиент = Мобильная Толока**.

#### Параметры

#|
||**Параметр**|**Описание**|**Обязательный**|**Значение по умолчанию**||-
||`type` | Тип поля: `file` — кнопка для загрузки файла. | да | нет||
||`name` | Атрибут для поля выходных данных. Содержит имя поля выходных данных. | да | нет||
||`sources` |

{% note info %}

Параметр применяется к заданиям, которые выполняются в мобильном приложении.

{% endnote %}

Источник файла.

Возможно задать несколько значений в формате `sources="<значение 1> <значение 2>"` (с пробелом, без запятой).

Допустимые значения:

- `RECORDER` — встроенный диктофон устройства;

- `FILE_MANAGER` — файловый менеджер. | да | нет||
||`fileType` |

{% note info %}

Параметр применяется к заданиям, которые выполняются в мобильном приложении.

{% endnote %}

Тип файла: `AUDIO` — аудиозапись. | да | нет||
||`label` | Надпись на кнопке. Например, `label="Нажми меня"`. | нет | В зависимости от языка интерфейса «Загрузить файл» (русский), «Upload file» (английский), «Dosya yükle» (турецкий), «Faylni yuklash» (узбекский).||
||`multipleSelect` | Количество файлов для одновременной загрузки.

Чтобы добавить возможность загрузки одного файла, задайте значение `false`.

Чтобы добавить возможность загрузки нескольких файлов:

1. Задайте значение `true`;

1. В описании выходных данных добавьте поле с типом `array_file` или другим типом массива. | нет | `true` (при наличии в описании выходных данных поля с типом`array_file` или другим типом массива).||
||`validation-show` | Расположение всплывающих подсказок (отображаются, если ответ не прошел валидацию). Расположение указывается относительно поля ввода.

Допустимые значения:

- Над полем ввода: `"top-left"` (слева), `"top-center"` (посередине), `"top-right"` (справа).

- Под полем ввода: `"bottom-left"` (слева), `"bottom-center"` (посередине), `"bottom-right"` (справа).

- Слева от поля ввода: `"left-top"` (сверху), `"left-center"` (посередине), `"left-bottom"` (внизу).

- Справа от поля ввода: `"right-top"` (сверху), `"right-center"` (посередине), `"right-bottom"` (внизу).

- Не показывать сообщение (`"false"`). | нет | `"top-left"`||
|#

{% include [contact-support](../../_includes/contact-support.md) %}