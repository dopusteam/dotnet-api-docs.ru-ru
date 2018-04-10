### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Больше не вызывает Application.FilterMessage повторным входом реализаций IMessageFilter.PreFilterMessage

|   |   |
|---|---|
|Подробные сведения|Перед .NET Framework 4.6.1, вызывая <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> с <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> которого вызывается <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> или <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (также в ходе вызова <xref:System.Windows.Forms.Application.DoEvents>) используется для перевода <xref:System.IndexOutOfRangeException?displayProperty=name>. Начиная с приложений, предназначенных для .NET Framework 4.6.1, это исключение не вызывается и повторным входом Вышеописанное может использовать фильтры.|
|Предложение|Имейте в виду, что <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> больше не вызывает исключение для повторного <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> поведения, описанных выше. Это относится только к приложениям, предназначенным для платформы .NET Framework 4.6.1.Apps для различных версий .NET Framework 4.6.1 можно отказаться от этого изменения (или может включить нацеливания более старых платформ приложений) с помощью [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) переключатель совместимости.|
|Область|Пограничный случай|
|Версия|4.6.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

