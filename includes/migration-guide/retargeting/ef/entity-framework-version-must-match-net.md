### <a name="entity-framework-version-must-match-the-net-framework-version"></a>Версии Entity Framework должна соответствовать версии платформы .NET Framework

|   |   |
|---|---|
|Подробные сведения|Версии платформы entity framework должны совпадать с версией платформы .NET framework. Entity Framework 5 рекомендуется .NET 4.5. Существуют некоторые известные проблемы с EF 4.x в проекте .NET 4.5 вокруг <xref:System.ComponentModel.DataAnnotations>. В .NET 4.5 эти были перемещены в другой сборке, поэтому существуют проблемы, определение которого заметок для использования.|
|Предложение|Обновление до платформы Entity Framework 5 для .NET Framework 4.5|
|Область|Значительно|
|Версия|4.5|
|Тип|Изменение целевой платформы|

