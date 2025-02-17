# В детализации по биллинг-аккаунту стало неожиданно отображаться потребление по сервису Cloud Logging

## Описание проблемы {#issue-description}

В детализации потребления услуг Yandex Cloud неожиданно появился сервис Cloud Logging, несмотря на то, что лог-группы не создавались явным образом.

## Решение {#issue-resolution}
С 1 ноября 2022 года в рамках сервиса Cloud Logging тарифицируется объем записываемых данных и время их хранения. В лог-группу, которая по умолчанию создается для каждого каталога, автоматически пишутся журналы работы сервисов Cloud Functions, API Gateway и Serverless Containers.

{% note info %}

Лог-группа по умолчанию создается автоматически даже после того, как она была ранее удалена вручную. Отключить или удалить ее полностью не получится.

{% endnote %}

Если вам не требуется хранение журналов работы Cloud Functions, API Gateway и Serverless Containers в вашем облаке, вы можете [установить минимальный срок хранения записей в 1 час](../../../logging/operations/retention-period.md). 

Для этого следует выполнить следующую команду средствами YC CLI:

```
yc logging group update --name=<имя группы> --retention-period=1h
```
Установить и настроить CLI можно по этой [инструкции](../../../cli/quickstart.md).

С тарификацией Cloud Logging можно ознакомиться на этой [странице](../../../logging/pricing.md).