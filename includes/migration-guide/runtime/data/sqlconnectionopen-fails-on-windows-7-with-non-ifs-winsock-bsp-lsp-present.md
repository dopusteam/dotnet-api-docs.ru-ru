### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>SqlConnection.Open завершается в Windows 7 не - IFS Winsock BSP или LSP присутствует

|   |   |
|---|---|
|Подробные сведения|<xref:System.Data.SqlClient.SqlConnection.Open> и <xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)> ошибкой в .NET Framework 4.5, если на компьютере Windows 7 с не - IFS Winsock BSP или LSP присутствуют на компьютере. Чтобы определить, установлен ли загрузочный IFS Процессор или LSP, используйте <code>netsh WinSock Show Catalog</code> команды и проверять каждые <code>Winsock Catalog Provider Entry</code> элемент, который возвращается. Если в качестве значения флагов службы задано <code>0x20000</code> бит, поставщик использует маркеры IFS и будет работать правильно. Если флаг <code>0x20000</code> бит снят (значение не задано), это поставщик BSP или LSP, не относящийся к IFS.|
|Предложение|Это ошибка исправлена в .NET Framework 4.5.2, поэтому ее можно избежать путем обновления .NET Framework. Кроме того, ее можно избежать, удалив все установленные поставщики LSP Winsock, не относящиеся к IFS.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

