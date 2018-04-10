### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>Предоставление состояния сеанса с Asp.Net StateServer требуется всех серверов в веб-фермы, чтобы использовать ту же версию .NET Framework

|   |   |
|---|---|
|Подробные сведения|При включении <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> состояние сеанса, все серверы в данной веб-фермы необходимо используют ту же версию платформы .NET Framework в порядке для состояния для совместного использования должным образом.|
|Предложение|Убедитесь, что обновление версии платформы .NET Framework на веб-серверах, которые совместно используют состояние, в то же время.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

