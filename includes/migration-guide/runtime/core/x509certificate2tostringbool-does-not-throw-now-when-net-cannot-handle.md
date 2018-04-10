### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) не создает исключение, теперь при .NET не удается обработать сертификата

|   |   |
|---|---|
|Подробные сведения|Ранее, вызывает этот метод, если <code>true</code> был передан для параметра verbose и были установлены сертификаты, которые не поддерживаются платформой .NET Framework. Теперь метод завершиться успешно и возвращать допустимое строковое выражение, пропускает недоступной части сертификата.|
|Предложение|Любой код, в зависимости от <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> должны обновляться следует ожидать, возвращаемая строка может исключить некоторые данные сертификата (например, открытый ключ, закрытый ключ и расширения), в некоторых случаях, в которых API будет ранее исключение.|
|Область|Пограничный случай|
|Версия|4.6|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

