### <a name="unicode-standard-version-80-categories-now-supported"></a>Теперь поддерживается категории стандартной версии 8.0 Юникода

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4.6.2 данных в Юникоде в framework была обновлена с Юникода стандартной версии 6.3 до версии 8.0.  При запросе категории символов Юникода в .NET Framework 4.6.2, некоторые результаты могут не соответствовать результатов в предыдущих версиях .NET Framework.  Это изменение, главным образом влияет слогов чероки и новый тай значение гласные знаки и знаки ударения.|
|Предложение|Проверьте код и удалить/изменить логику, зависящую от жестко категории символов Юникода.|
|Область|Дополнительный номер|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

