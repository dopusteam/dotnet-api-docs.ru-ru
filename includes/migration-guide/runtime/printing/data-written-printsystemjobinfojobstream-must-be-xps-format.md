### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>Данные, записанные в PrintSystemJobInfo.JobStream должно быть в формате XPS

|   |   |
|---|---|
|Подробные сведения|<xref:System.Printing.PrintSystemJobInfo.JobStream> Свойство предоставляет поток задания печати. Пользователь может отправить необработанные данные в компоненты печати базовой операционной системы путем записи в этот поток. Начиная с .NET Framework 4.5 в Windows 8 и более поздних версиях операционной системы Windows, записываются в этот поток данных должен быть в формате XPS, как поток пакета.|
|Предложение|Для вывода содержимого печати выполните одно из следующих действий.<ul><li>Используйте класс <xref:System.Windows.Xps.XpsDocumentWriter> класса для вывода содержимого печати. Это рекомендуемый вариант.</li><li>Убедитесь, что данные, отправляемые в поток, возвращенный <xref:System.Printing.PrintSystemJobInfo.JobStream> свойства находится в формате XPS, как поток пакета.</li></ul>|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

