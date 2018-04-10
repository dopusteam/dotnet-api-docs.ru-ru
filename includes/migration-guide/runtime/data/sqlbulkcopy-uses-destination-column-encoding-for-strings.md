### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>Использует SqlBulkCopy целевой столбец кодирования строк

|   |   |
|---|---|
|Подробные сведения|При вставке данных в столбец <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> использует кодировку целевого столбца, а не кодировку по умолчанию для типов <code>VARCHAR</code> и <code>CHAR</code>. Это изменение исключает возможность повреждения данных, вызванного использованием кодировки по умолчанию, если в целевом столбце не используется кодировка по умолчанию. В редких случаях существующее приложение может вызывать исключение SqlException при изменении кодировки создаются слишком большие для целевого столбца данные.|
|Предложение|Ожидать, что <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> больше не приведет к повреждению данных из-за различия кодировки. Если копируются строки рядом с ограничение размера целевого столбца, может оказаться необходимым кодируемый либо предварительно (копирования данных для проверки того, что данные помещаются в целевом столбце) или перехватить <xref:System.Data.SqlClient.SqlException?displayProperty=name>s.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

