### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Отсутствует моникер целевой платформы результаты в поведении 4.0

|   |   |
|---|---|
|Подробные сведения|Приложения без <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> применяется на уровне будут сборки, автоматическое выполнение с использованием семантики платформы .NET Framework 4.0 (совместимости). Для обеспечения высокого качества, рекомендуется явно объяснить все двоичные файлы с <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> , указывающая версию платформы .NET Framework, они были созданы. Обратите внимание, использование моникера целевой платформы в файл проекта приведет MSBuild для автоматического применения <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Предложение|Объект <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> должен быть получен, либо добавив атрибут непосредственно к сборке или путем указания целевой платформы в [файл проекта или через Visual Studio проекта свойства графического пользовательского интерфейса](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Область|Значительно|
|Версия|4.5|
|Тип|Среда выполнения|

