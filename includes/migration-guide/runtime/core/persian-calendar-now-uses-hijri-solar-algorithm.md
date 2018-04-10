### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>Персидский календарь теперь использует алгоритм солнечного календаря хиджры

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6 <xref:System.Globalization.PersianCalendar?displayProperty=name> класс использует алгоритм солнечного календаря хиджры. Преобразование даты между <xref:System.Globalization.PersianCalendar?displayProperty=name> и других календарей могут привести к немного другой результирующий начиная с .NET Framework 4.6 для дат ранее 1800 или более поздней, чем 2023 гг (по григорианскому календарю). Кроме того <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> теперь <code>March 22, 0622 instead of March 21, 0622</code>.|
|Предложение|Имейте в виду, что при использовании персидского календаря в .NET 4.6 некоторые даты в прошлом или будущем могут несколько отличаться. Кроме того, даты, сериализуемые между процессами, которые могут выполняться в различных версиях .NET Framework, не следует хранить в виде строк дат персидского календаря (поскольку эти значения могут быть разными).|
|Область|Дополнительный номер|
|Версия|4.6|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

