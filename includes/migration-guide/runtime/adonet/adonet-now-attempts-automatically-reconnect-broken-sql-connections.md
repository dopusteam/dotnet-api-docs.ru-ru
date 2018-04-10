### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>Теперь пытается автоматически подключиться прерванных соединений SQL ADO.NET

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.5.1, .NET Framework будет пытаться автоматически переподключаться прерванных соединений SQL. Несмотря на то, что обычно станет приложений более надежным, существуют крайние случаи, в которых приложение должно быть известно, что соединение было потеряно, что может занять какое-либо действие после восстановления подключения.|
|Предложение|Если эта функция нежелательно из-за проблем совместимости, его можно отключить, задав <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> свойстве строки соединения (или <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) значение 0.|
|Область|Пограничный случай|
|Версия|4.5.1|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

