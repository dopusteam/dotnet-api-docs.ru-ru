### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase больше не задается произвольно, UseRandomizedStringHashAlgorithm

|   |   |
|---|---|
|Подробные сведения|До .NET Framework 4.6, значение <xref:System.AppDomainSetup.DynamicBase> может быть произвольно между доменами приложений или между процессами, если UseRandomizedStringHashAlgorithm был включен в файле конфигурации приложения. Начиная с .NET Framework 4.6 <xref:System.AppDomainSetup.DynamicBase> вернет значение стабильный между различными экземплярами работающего приложения, а также между различных доменов приложений. Динамические базовых классов по-прежнему будут различаться для разных приложений; Это изменение удаляет только случайный элемент именования для различных экземпляров одного приложения.|
|Предложение|Имейте в виду, что разрешение <code>UseRandomizedStringHashAlgorithm</code> не приводит к <xref:System.AppDomainSetup.DynamicBase> произвольно. Требуется случайных базы, должна быть произведена в коде приложения, а не через этот интерфейс API.|
|Область|Пограничный случай|
|Версия|4.6|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

