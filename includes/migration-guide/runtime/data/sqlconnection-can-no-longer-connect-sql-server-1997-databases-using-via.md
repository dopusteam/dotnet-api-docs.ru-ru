### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection больше не может подключиться к SQL Server 1997 или баз данных с помощью адаптера VIA

|   |   |
|---|---|
|Подробные сведения|Подключения к базам данных SQL Server с помощью [протокол Virtual Interface Adapter (VIA)](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) больше не поддерживаются. Протокол, используемый для подключения к базе данных SQL Server отображается в строке подключения. Соединение VIA содержит через:&lt;имя_сервера&gt;. Если это приложение подключается к SQL протокол, отличный от VIA (tcp: или np: например), а затем встречается не критическое изменение. Кроме того подключения к SQL Server 7 (1997) больше не поддерживаются.|
|Предложение|Протокол VIA является устаревшим, поэтому это альтернативный протокол следует использовать для подключения к базам данных SQL. TCP/IP — наиболее распространенные протокола, используемого. Инструкции для включения протокола TCP/IP можно найти [здесь](https://msdn.microsoft.com/library/bb909712.aspx). Если базы данных осуществляется только из интрасети, протокол общего каналов может обеспечить более высокую производительность, если сеть слишком медленно.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

