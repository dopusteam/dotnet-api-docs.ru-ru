### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml и EncryptedXml критические изменения

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4.6.2 исправления безопасности <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> и <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> привести к различные виды поведения во время выполнения. Например, примененная к объекту директива<ul><li>Если документ имеет несколько элементов с одинаковым <code>id</code> атрибута и подписи предназначен для одного из этих элементов в корневом подписи, документ будет теперь считаться недействительными.</li><li>Документы с помощью нестандартных алгоритмы преобразования XPath в ссылках считаются недопустимыми.</li><li>Документы с помощью нестандартных алгоритмы преобразования XSLT в ссылках Теперь рассмотрим недопустимый.</li><li>Любой программы используете подписи отсоединена внешний ресурс, будут недоступны для этого.</li></ul>|
|Предложение|Разработчикам может потребоваться рассмотреть использование <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> и <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>, а также типы, производные от <xref:System.Security.Cryptography.Xml.Transform> , так как документ получателя не удается обработать его.|
|Область|Дополнительный номер|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

