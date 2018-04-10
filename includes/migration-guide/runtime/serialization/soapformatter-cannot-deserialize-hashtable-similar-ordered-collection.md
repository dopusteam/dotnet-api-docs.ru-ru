### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter не удается выполнить десериализацию хэш-таблицы и подобные упорядоченных объекты-коллекции

|   |   |
|---|---|
|Подробные сведения|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> Выполняет успешно десериализует с другими версиями не гарантируется, что объекты сериализованы в рамках одной версии платформы .NET Framework. В частности, некоторые упорядоченные коллекции (например <xref:System.Collections.Hashtable?displayProperty=name>) добавлены элементы между 4.0 и 4.5, таким образом, что объекты этих типов не удается выполнить десериализацию с платформой .NET 4.0, если они были сериализованы с .NET 4.5. Обратите внимание, что если сериализованные данные сериализуются и десериализуются в одной версии .NET Framework, проблемы не возникают.|
|Предложение|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> необходимо заменить сериализации <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> сериализации или <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> было устойчиво к изменениям в .NET Framework.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

