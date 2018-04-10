### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>Некоторые API-интерфейсы .NET причина первый шанс обработки (обрабатывать) EntryPointNotFoundExceptions

|   |   |
|---|---|
|Подробные сведения|В платформе .NET Framework 4.5 небольшое количество методов .NET начала генерации первый шанс обработки <xref:System.EntryPointNotFoundException?displayProperty=name>s. Эти исключения обрабатывались в .NET Framework, но могли нарушать работу службы автоматизации тестирования, которая не ожидала первых экземпляров исключений. Те же интерфейсы API препятствуют работе некоторых сценариев ApiVerifier, если включен тест HighVersionLie.|
|Предложение|Этой ошибки можно избежать путем обновления до .NET Framework 4.5.1. Кроме того, можно обновить автоматизации тестирования, чтобы не будет прерывать при первичном <xref:System.EntryPointNotFoundException?displayProperty=name>s.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

