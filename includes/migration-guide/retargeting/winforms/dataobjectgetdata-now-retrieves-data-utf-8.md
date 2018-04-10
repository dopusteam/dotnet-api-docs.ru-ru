### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>Теперь DataObject.GetData получает данные в формате UTF-8

|   |   |
|---|---|
|Подробные сведения|Для приложений, предназначенных для .NET Framework 4 или выполняющихся в .NET Framework 4.5.1 или более ранних версиях <code>DataObject.GetData</code> Получает HTML данные в виде строки ASCII. В результате символа ASCII (символы с кодами ASCII больше 0x7F), представляются двумя случайными символами. Для приложений, ориентированных на .NET Framework 4.5 или более поздней версии и запуска в .NET Framework 4.5.2 <code>DataObject.GetData</code> Получает HTML-данные в формате UTF-8, который правильно представляет символы с кодами более 0x7F.|
|Предложение|Если реализован обходной путь для проблемы с HTML-строк кодировкой (например, явная кодировка HTML-строки, полученной из буфера обмена путем ее передачи <xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) и выполняется изменение целевой платформы приложения с версии 4 4.5, решение должно быть удалено. Если для какой-либо причине требуется прежнее поведение, приложение можно выбрать целевую платформу .NET Framework 4.0, чтобы добиться этого поведения.|
|Область|Пограничный случай|
|Версия|4.5.2|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

