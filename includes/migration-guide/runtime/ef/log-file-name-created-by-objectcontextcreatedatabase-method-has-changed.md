### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>Имя файла журнала, созданным с помощью метода ObjectContext.CreateDatabase изменилось на соответствует спецификациям SQL Server

|   |   |
|---|---|
|Подробные сведения|Когда <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> вызывается метод либо непосредственно или с помощью Code First с поставщиком SqlClient и значение AttachDBFilename в строке соединения, он создает файл журнала с именем filename_log.ldf вместо filename.ldf (где имя файла — имя файл, заданный параметром значение AttachDBFilename). Это изменение улучшает отладку, предоставляя файл журнала, имя которого соответствует спецификациям SQL Server.|
|Предложение|Если имя файла журнала важно для приложения, приложение следует обновить для использования стандартного формата имени файла _log.ldf.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

