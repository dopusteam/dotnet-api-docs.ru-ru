### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>Десериализация объектов MailMessage, сериализованные в .NET Framework 4.5 может завершиться ошибкой

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.5 <xref:System.Web.Mail.MailMessage> объекты могут включать другие символы. В .NET Framework 4 поддерживаются только символы ASCII. <xref:System.Web.Mail.MailMessage> объекты, содержащие символы, отличные от ASCII, и, сериализуются в .NET Framework 4.5 или более поздней версии не может быть десериализован в .NET Framework 4.|
|Предложение|Убедитесь, что код обеспечивает обработку исключений при десериализации <xref:System.Web.Mail.MailMessage> объекта.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

