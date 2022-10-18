# Выполненные задания

Чтобы привлечь к задаче как можно больше исполнителей, ограничьте количество заданий в [пуле](../../glossary.md#pool) на каждого исполнителя или [установите лимит](income.md) на дневной заработок в [проекте](../../glossary.md#project).

## Когда использовать {#when-use}

Используйте это правило, чтобы:

- Получить ответы как можно большего числа исполнителей. В этом случае установите низкий порог, например, одну [страницу заданий](../../glossary.md#task-suite).

- Обеспечить защиту от роботов. В этом случае порог должен быть выше, например, 10% заданий пула.

{% note tip %}

Не устанавливайте большие значения правила в пулах, где исполнители не успеют выполнить необходимое количество заданий.

{% endnote %}

## Как настроить {#rule}

{% note warning %}

Все поля этого правила — обязательные. Если вы не заполните хотя бы одно из них, правило сохранить не получится.

{% endnote %}

#|
||**Поле**|**Описание**||
||{% if locale == "ru-ru" %}**Если**{% endif %}{% if locale == "en-com" %}**If**{% endif %} | Условие, при котором выполняется действие в поле {% if locale == "ru-ru" %}**то**{% endif %}{% if locale == "en-com" %}**then**{% endif %}:

- {% if locale == "ru-ru" %}**отправленных страниц заданий**{% endif %}{% if locale == "en-com" %}**submitted task suites**{% endif %} — количество страниц заданий в пуле, выполненных исполнителем.||
||{% if locale == "ru-ru" %}**то**{% endif %}{% if locale == "en-com" %}**then**{% endif %} | Действие, выполняемое при условии {% if locale == "ru-ru" %}**Если**{% endif %}{% if locale == "en-com" %}**If**{% endif %}:

- {% if locale == "ru-ru" %}**приостановить**{% endif %}{% if locale == "en-com" %}**suspend**{% endif %} — приостановить доступ исполнителя к пулу на указанное количество дней. Причина отображается только заказчику.

- {% if locale == "ru-ru" %}**установить значение навыка**{% endif %}{% if locale == "en-com" %}**assign skill value**{% endif %} — присвоить исполнителю фиксированное значение [навыка](nav.md).

- {% if locale == "ru-ru" %}**заблокировать**{% endif %}{% if locale == "en-com" %}**ban**{% endif %} — закрыть доступ к проекту или всем проектам заказчика на указанное количество дней. Причина блокировки отображается только заказчику.

    Если доступ к заданиям блокируется на ограниченный срок (например, на 7 дней), после снятия блокировки история ответов исполнителя не сохраняется. Навык рассчитывается на основании новых ответов.

- {% if locale == "ru-ru" %}**принять все ответы исполнителя в пуле**{% endif %}{% if locale == "en-com" %}**accept all assignments from this Toloker in the pool**{% endif %} — требует настройки [отложенной приемки](offline-accept.md).

    Пригодится, если исполнитель выполняет большинство заданий качественно. Пример: исполнитель выполнил больше 80% заданий правильно и вас устраивает такой результат. Правило сработает автоматически — все ответы в пуле будут приняты.
||
|#

## Пример правила {#examples}

**Задача**: вы проводите социологический опрос. Чтобы собрать ответы от максимального числа исполнителей, настройте правило **Выполненные задания**.

#### Правильная настройка

![](../_images/control-rules/submitted-answers/qcr-submitted-answers_example1.png)

Если исполнитель выполнит больше 20 страниц заданий, ему будет ограничен доступ к пулу и он больше не сможет выполнять ваши задания.

{% include [ban-banned-user-answers-note](../_includes/concepts/ban/id-ban/banned-user-answers-note.md) %}

## Решение проблем {#troubleshooting}

{% cut "Нужно ли создавать навык для каждого пула?" %}

Лучше использовать один [навык](../../glossary.md#skill) в проекте. Можно выбрать способ подсчета навыка:

- Подсчет навыка для каждого пула отдельно. Текущее значение навыка — это значение навыка в пуле, который выполнялся последним. Такой вариант удобен, если:

    - Пулы предназначены для разных групп исполнителей (например, настроены фильтры по городам, странам).

    - Пулы запускаются последовательно, и вы не хотите учитывать качество ответов в предыдущих пулах при подсчете навыка в выполняемом пуле.

    Этот способ подсчета действует по умолчанию при добавлении блока контроля качества в пул. Для блока по контрольным заданиям оставьте пустым поле **Учитывать последних ответов на контрольные и обучающие задания**.

- Подсчет навыка по всем выполненным заданиям в проекте. Такой вариант удобен, если пулы небольшие и вам не нужно рассчитывать навык для каждого пула.

    Этот способ подсчета доступен только для навыков по контрольным заданиям. Чтобы использовать его, заполните поле **Учитывать последних ответов на контрольные и обучающие задания** в блоках контроля качества в пулах.

{% endcut %}

{% cut "Можно ли использовать навык не только в пуле или в одном проекте, но и в разных проектах?" %}

Да, конечно, один и тот же навык можно назначать и использовать на различных проектах. Но чаще всего один навык используется в рамках одного проекта. Если исполнитель хорошо выполняет одно задание, это не значит, что он так же успешно справится с другим. Кроме того, используя фильтры по давно настроенным навыкам, вы ограничиваете количество доступных исполнителей.

{% endcut %}

{% cut "Может ли один работник попасть в два пула одного проекта? Можно ли этого избежать?" %}

Да, может, если оба пула ему доступны. Чтобы ограничить доступ исполнителя к следующим заданиям, используйте правило [Выполненные задания](submitted-answers.md) — выберите блокировку на проекте.

{% endcut %}

{% cut "У меня есть два варианта текста, который мне надо показывать респондентам: половине один вариант, половине другой (типа A/B-тестирования). Это возможно сделать в Толоке или надо создавать два отдельных проекта?' %}

Если вы передаете тексты во входные данные, то достаточно загрузить в пул 2 разных задания: в одном из них в поле `INPUT:<имя входного поля>` вы передадите текст № 1, в другом — текст № 2. А если текст в самом шаблоне задания в блоке HTML, то да, нужно клонировать проект. Чтобы исполнитель мог сделать только одно задание в вашем проекте, используйте правило [Выполненные задания](submitted-answers.md). Можно назначить навык или заблокировать исполнителя после того, как он отправит один ответ.

{% endcut %}

{% include [contact-support](../_includes/contact-support-help.md) %}