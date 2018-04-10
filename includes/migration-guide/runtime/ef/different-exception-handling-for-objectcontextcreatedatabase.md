### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>Обработка для методов ObjectContext.CreateDatabase и DbProviderServices.CreateDatabase другое исключение

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET 4.5, если происходит сбой создания базы данных, методы <code>CreateDatabase</code> будут пытаться удалить пустую базу данных. Если эта операция выполняется успешно, будет распространяться исходное исключение <xref:System.Data.SqlClient.SqlException?displayProperty=name> (вместо <xref:System.InvalidOperationException?displayProperty=name>, которое всегда создавалось в .NET 4.0).|
|Предложение|При перехвате <xref:System.InvalidOperationException?displayProperty=name> при выполнении <xref:System.Data.Objects.ObjectContext.CreateDatabase> или <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, SQLExceptions должны теперь также перехватываться.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

