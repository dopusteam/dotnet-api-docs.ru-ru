### <a name="xslt-style-sheet-exception-message-changed"></a>XSLT сообщение об исключении стиля таблицы изменен

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4.5, текст сообщения об ошибке при XSLT-файл является слишком сложным является &quot;таблица стилей слишком сложна.&quot; В предыдущих версиях был сообщение об ошибке &quot;ошибка компиляции XSLT.&quot; Код приложений, который зависит от текста сообщения об ошибке, больше не будет работать. Однако типы исключений остаются теми же, поэтому это изменение не должно иметь никаких реальных последствий.|
|Предложение|Обновить код приложения в зависимости от того, сообщение об исключении из этой ошибки следует ожидать нового сообщения или (даже лучше) обновите код, чтобы зависеть только от типа исключения (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), которая не была изменена.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

