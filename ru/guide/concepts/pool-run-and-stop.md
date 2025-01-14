# Запуск и остановка пула заданий

{% include [deprecate](../../_includes/deprecate.md) %}

[Пул](../../glossary.md#pool) можно запустить, если:

1. В него загружены задания.

1. На [вашем счете](budget.md) достаточно средств для оплаты всех его заданий с учетом [перекрытия](../../glossary.md#overlap).

Чтобы запустить пул, нажмите кнопку ![](../_images/other/b-start-pool.svg) на странице пула или ![](../_images/tutorials/content-moderation/pool-action-play.svg) в списке пулов на странице [проекта](../../glossary.md#project).

Запущенный пул имеет статус {% if locale == "ru-ru" %}«Открыт»{% endif %}{% if locale == "en-com" %}«Open»{% endif %}. Когда все задания пула выполнены, пул автоматически перейдет в статус {% if locale == "ru-ru" %}«Закрыт»{% endif %}{% if locale == "en-com" %}«Closed»{% endif %}.

Чтобы досрочно остановить выдачу заданий пула, нажмите кнопку ![](../_images/other/b-pause-pool.svg) на странице пула или ![](../_images/tutorials/content-moderation/pool-action-pause.svg) в списке пулов на странице проекта.

{% note tip %}

Новые задания можно загружать в открытый или закрытый пул.

{% endnote %}

## Что дальше {#what_next}

- [Получите и обработайте результаты](result-of-eval.md).

## Решение проблем {#troubleshooting}

{% cut "Я создал проект и пул, но не нажимается кнопка Далее или в предпросмотре белый экран." %}

Так Толока подает сигнал, что с проектом что-то не в порядке. Белый экран часто появляется при ошибках в [интерфейсе задания](../../glossary.md#task-interface), в том числе JavaScript-коде. Кнопка **Далее** может не реагировать, если в выходной спецификации не хватает какого-то поля, если в ней указаны недопустимые значения или, например, если у вас в JavaScript настроена валидация по несуществующему полю.

{% endcut %}

{% cut "Какое перекрытие лучше установить?" %}

Перекрытие определяет, сколько исполнителей будут выполнять задание в пуле.

Оптимальное перекрытие — это перекрытие, по результатам которого заказчик получает устраивающее его качество ответов. Для большинства заданий без [отложенной приемки](../../glossary.md#assignment-review) достаточно перекрытия от «3» до «5». Если у вас простое задание, скорее всего, вам хватит перекрытия «3». Для заданий с отложенной приемкой установите перекрытие «1».

{% endcut %}

{% cut "Можно ли изменить перекрытие после запуска пула?" %}

Да. [Откройте режим редактирования пула](pool-edit.md) и установите новое значение перекрытия. Перезапускать пул не требуется. Обновление настроек обычно происходит быстро, но если заданий много, то может занять несколько минут.

{% endcut %}

{% cut "Может ли быть такое, что при динамическом перекрытии пул закрывается раньше времени, когда закончились задания для минимального перекрытия? Перекрытие увеличилось, а пул закрылся, и надо его запускать вручную." %}

Да, такое может произойти. Необходимо установить достаточный интервал закрытия пула.

{% endcut %}

{% include [contact-support](../_includes/contact-support.md) %}