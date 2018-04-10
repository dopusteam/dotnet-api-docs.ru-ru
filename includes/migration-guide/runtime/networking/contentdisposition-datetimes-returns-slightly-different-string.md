### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>Возвращает строку, немного отличается, ContentDisposition даты

|   |   |
|---|---|
|Подробные сведения|Строковые представления объекта <xref:System.Net.Mime.ContentDisposition?displayProperty=name>были обновлены, начиная с 4.6, чтобы всегда представляют компонент часов <xref:System.DateTime?displayProperty=name> с двумя цифрами. Это сделано в соответствии с [RFC822](http://www.ietf.org/rfc/rfc0822.txt) и [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). В результате <xref:System.Net.Mime.ContentDisposition.ToString> возвращает немного другую строку в 4.6 в сценариях, где один из элементов времени расположения имел значение, предшествующее 10:00. Обратите внимание, что ContentDispositions сериализуются иногда посредством преобразования их в строки, поэтому любой <xref:System.Net.Mime.ContentDisposition.ToString> вызовов GetHashCode, операции или сериализации, необходимо проверить.|
|Предложение|Не ожидается, что строковые представления ContentDispositions из разных версий .NET Framework будут правильно сравниваться друг с другом. Если возможно, перед сравнением преобразуйте строки обратно в ContentDispositions.|
|Область|Дополнительный номер|
|Версия|4.6|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

