### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException теперь задает позиции строки должным образом

|   |   |
|---|---|
|Подробные сведения|Если <xref:System.Xml.Linq.LoadOptions.SetLineInfo> значение передается в метод Load и возникновении ошибки проверки, <xref:System.Xml.Schema.XmlSchemaException.LineNumber> и <xref:System.Xml.Schema.XmlSchemaException.LinePosition> теперь содержат сведения о строке.|
|Предложение|Код обработки исключений, который предполагается <xref:System.Xml.Schema.XmlSchemaException.LineNumber> и <xref:System.Xml.Schema.XmlSchemaException.LinePosition> не будет набора должны быть обновлены, поскольку эти свойства будет установлено должным образом при использовании SetLineInfo при загрузке XML.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

