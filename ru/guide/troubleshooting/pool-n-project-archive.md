# Архивация пулов и проектов

{% include [troubleshooting-key-combination](../_includes/troubleshooting/troubleshooting/id-troubleshooting/key-combination.md) %}


#### Можно ли удалить пул?

Полностью удалить пул невозможно, но можно переместить в архив. Система не удаляет пулы автоматически.

#### Как долго хранится пул?

Если в пуле нет активности в течение месяца, он архивируется. Его нельзя запустить, но можно клонировать или скачать размеченные данные.

#### Где хранятся пулы, закрытые несколько месяцев назад?

Неактивные пулы через месяц попадают в архив. Чтобы их увидеть, на вкладке **Пулы** выберите **Архивные**.

#### Как узнать параметры архивации пула?

Чтобы узнать дату архивации, получите [список операций]({{ get-operations-list }}) с типом `POOL.ARCHIVE`. В ответе будет номер пула и дата архивации. Получить способ отправки пула в архив через API невозможно.

Если между активностью в пуле и его архивацией прошло меньше месяца, можно предположить, что пул отправили в архив вручную, а если месяц — автоматически.

#### Как принять задания из архивированного пула или когда исполнитель написал мне позже допускаемого срока?

Просто [начислите толокеру бонус](../concepts/bonus.md) без изменения статуса задания. Изменить статус задания в пуле в этой ситуации уже невозможно.

[Другой вопрос](support.md#help)

{% include [contact-support](../_includes/contact-support-help.md) %}