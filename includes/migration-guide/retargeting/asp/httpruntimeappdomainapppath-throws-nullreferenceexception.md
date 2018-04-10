### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>Создает исключение NullReferenceException, HttpRuntime.AppDomainAppPath

|   |   |
|---|---|
|Подробные сведения|В платформе .NET Framework 4.6.2 среда выполнения создает <code>T:System.NullReferenceException</code> при получении <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> значением, которое содержит символы null. В .NET Framework 4.6.1 и более ранних версий, среда выполнения создает <code>T:System.ArgumentNullException</code>.|
|Предложение|Либо выполните реагировать на это изменение можно сделать:<ul><li>Обрабатывать <code>T:System.NullReferenceException</code> Если после этого приложение выполняется на платформе .NET Framework 4.6.2.</li><li>Обновление до 4.7 Framework .NET, который восстанавливает прежнее поведение и возникает исключение <code>T:System.ArgumentNullException</code>.</li></ul>|
|Область|Пограничный случай|
|Версия|4.6.2|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

