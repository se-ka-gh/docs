# Как загрузить задания

{% include [deprecate](../../_includes/deprecate.md) %}

Чтобы загрузить [файл с заданиями](../../glossary.md#tsv) в [пул](pool-main.md):

1. Нажмите кнопку {% if locale == "ru-ru" %}**Загрузить данные**{% endif %}{% if locale == "en-com" %}**Upload data**{% endif %}.

1. Скачайте шаблон и добавьте свои данные.

    #### Использовать пример данных

    Если вы хотите посмотреть, как ваш проект будет выглядеть после запуска, но у вас еще нет заданий для разметки, вы можете загрузить в пул готовый пример данных. Примеры данных доступны для шаблонов:

    - {% if locale == "ru-ru" %}**Классификация изображений**{% endif %}{% if locale == "en-com" %}**Image classification**{% endif %}
    - {% if locale == "ru-ru" %}**Релевантность поиска товаров**{% endif %}{% if locale == "en-com" %}**Product search relevance**{% endif %}
    - {% if locale == "ru-ru" %}**Распознавание объектов и выделение областей**{% endif %}{% if locale == "en-com" %}**Object recognition & detection**{% endif %}
    - {% if locale == "ru-ru" %}**Кликбейт или нет?**{% endif %}{% if locale == "en-com" %}**Clickbait or not?**{% endif %}

    Нажмите {% if locale == "ru-ru" %}**Использовать пример данных**{% endif %}{% if locale == "en-com" %}**Use sample data**{% endif %} справа от надписи {% if locale == "ru-ru" %}**Прикрепите подготовленный файл с данными**{% endif %}{% if locale == "en-com" %}**Attach the prepared file with data**{% endif %}. Это позволит избежать дополнительных действий с файлами.

    После того, как вы поработали с примером данных и вас все устроило, подготовьте свои данные и загрузите их в пул.

1. Прикрепите файл с заданиями.

1. Нажмите кнопку {% if locale == "ru-ru" %}**Продолжить**{% endif %}{% if locale == "en-com" %}**Continue**{% endif %}.

1. Выберите способ распределения заданий и укажите количество заданий на странице. Подробнее об этих настройках см. в разделе [Способы распределения заданий](distribute-tasks-by-pages.md).

1. Нажмите кнопку {% if locale == "ru-ru" %}**Разделить задания на страницы**{% endif %}{% if locale == "en-com" %}**Combine tasks into suites**{% endif %}.

1. Дождитесь результата обработки.

Чтобы удалить все задания в пуле, нажмите кнопку {% if locale == "ru-ru" %}**Удалить**{% endif %}{% if locale == "en-com" %}**Delete**{% endif %}.

{% note alert "Ограничение" %}

Можно добавить не более одного миллиона заданий в пул. Если вам надо загрузить больше заданий, создайте новый пул.

{% endnote %}

## Советы и рекомендации {#tips}

- Устанавливайте количество заданий на странице в зависимости от сложности и времени на выполнение задания.

    Рекомендуем распределять количество так, чтобы на одну страницу уходило не больше пяти минут.

- Если получена ошибка обработки — формат данных внутри файла некорректный. Например, в файле есть лишние табы, не хватает строк, заголовков или кавычек.

    В таком случае нажмите кнопку {% if locale == "ru-ru" %}**Отменить**{% endif %}{% if locale == "en-com" %}**Cancel**{% endif %} и исправьте ошибки, а затем загрузите файл снова.

## Ошибки обработки {#table-with-errors}

Если при загрузке файла возникла ошибка, воспользуйтесь таблицей.

{% include [concept_iy1_3kh_5mb-how-to-see-log](../_includes/troubleshooting/adding-tasks-to-the-pool/id-concept_iy1_3kh_5mb/how-to-see-log.md) %}

{% cut "Таблицы ошибок обработки" %}

```json
"parsing_error_of": "https://tlk.s3.yandex.net/wsdm2020/photos/2d5f63a3184919ce7e3e7068cf93da4b.jpg\t\t", "exception_msg": "the nameMapping array and the sourceList should be the same size (nameMapping length = 1, sourceList size = 3)"
```

#|
|| **Описание** | **Как исправить** ||
||**Лишние знаки табуляции.**

Если в загружаемом файле после данных или ссылки стоит количество разделителей столбцов `\t` больше, чем задано число столбцов во [входных данных](../../glossary.md#input-output-data), то появится сообщение об ошибке.

Например, когда во входных определен 1 столбец, а в файле после ссылки прописано ещё два знака табуляции `\t\t`, то получится 3 столбца, 2 из которых лишние. | Удалите лишние разделители столбцов, в приведенном выше примере ошибки — оба знака (`\t\t`).||
|#

```json
"exception_msg": "the nameMapping array and the sourceList should be the same size (nameMapping length = 4, sourceList size = 6)"
```

#|
|| **Описание** | **Как исправить** ||
||**Не совпадает количество полей в заголовке и в строке.** | Проверьте, что:

- указано верное количество знаков табуляции в структуре файла;

- строковые значения, содержащие знак табуляции, заключены [в кавычки](pool_csv.md#string)`" "`.||
|#

```json
"code": "VALUE_REQUIRED", "message": "Value must be present and not equal to null"
```

#|
|| **Описание** | **Как исправить** ||
||**Не указано значение обязательного поля входных данных.** | Проверьте, что заполнены все столбцы с обязательными полями входных данных.||
|#

```json
"code": "INVALID_URL_SYNTAX", "message": "Value must be in valid url format"
```

#|
|| **Описание** | **Как исправить** ||
||**Данные в поле с типом «ссылка» («url») некорректны.** | Проверьте, что:

- Все ссылки начинаются с префикса `http://`, `https://` или `www`.

- {% if locale == "ru-ru" %}При [загрузке файла с Яндекс Диска](prepare-data.md) по относительной ссылке, указан тип данных **строка** для [поля входных данных](incoming.md).{% endif %}||
|#

```json
"exception_msg": "unexpected end of file while reading quoted column beginning on line 2 and ending on line 4"
```

#|
|| **Описание** | **Как исправить** ||
||**В строке стоит непарная кавычка.** | Проверьте, что все кавычки [экранированы](pool_csv.md#string).||
|#

{% endcut %}

## Что дальше {#what_next}

- Узнайте про [способы распределения заданий по страницам](distribute-tasks-by-pages.md).

- Если вы еще не разметили [контрольные](../../glossary.md#control-task) и [обучающие](../../glossary.md#training-task) задания в файле, [разметьте задания в интерфейсе](task_markup.md).

## Решение проблем {#troubleshooting}

{% cut "Ошибки в заголовках столбцов" %}

Если [заголовки столбцов](pool_csv.md) некорректны, файл будет полностью отклонен. В остальных случаях указано количество заданий с ошибками обработки.

{% endcut %}

{% cut "Почему после запуска первого проекта не приходят ответы и все загруженные задания отмечаются как "Обучающие"?" %}

Проверьте поле `hint`. Для обычных заданий это поле должно быть пустым.

{% endcut %}

{% cut "Сколько заданий должно быть на странице?" %}

Количество заданий зависит от сложности и длительности выполнения. Не делайте страницы заданий слишком большими: они неудобны для исполнителей (например, при сбоях в соединении с интернетом) и не пользуются спросом.

{% endcut %}

{% cut "Как определить время на выполнение задания?" %}

Попробуйте выполнить задания сами, попросите своих друзей и коллег. Найдите среднее время выполнения и добавьте к нему 50%.

{% endcut %}

{% cut "Почему при загрузке задания, в котором нужно просмотреть изображение и написать фидбэк, появляется ошибка синтаксиса?" %}

Ошибка будет возникать, если на вход ожидается тип URL, а приходит строка.

Причин может быть две:

- Входное поле имеет тип "ссылка".

- Пул работает на неактуальной версии проекта. То есть создан до того, как вы изменили тип входного поля.

{% endcut %}

{% cut "Какое максимальное количество заданий может быть на одной странице?" %}

Зависит от задания. Технически можно много.

Но, во-первых, исполнители неохотно берутся за задания, которые требуют много времени на выполнение. То есть, они скорее сделают 10 заданий по одной минуте, чем одно задание на 10 минут.

Во-вторых, при большом количестве заданий на странице может быть проблема с загрузкой файлов для разметки. Например, картинок.

Третий момент — контроль качества и оценка выполнения всей страницы. Если вы используете дооценку заблокированных исполнителей, то лучше дробить задание на более мелкие части, чтобы в переразметку отправлялось меньше заданий. Это позволит уложиться в бюджет.

{% endcut %}

{% cut "Почему в задании с классификацией фотографий, если на странице больше 5-ти фотографий, то Толока разделяет их на 2 страницы?" %}

Загруженные ссылки на картинки в файле Толока разделит на страницы в зависимости от того, какой способ распределения заданий вы выбрали. Подробнее читайте на странице [Способы распределения заданий](distribute-tasks-by-pages.md).

{% endcut %}

{% cut "Чем отличаются task и task_suite?" %}

Task — это отдельное задание. Task suite — страница с заданиями. Исполнитель получает оплату за страницу заданий.

{% endcut %}

{% include [contact-support](../_includes/contact-support.md) %}