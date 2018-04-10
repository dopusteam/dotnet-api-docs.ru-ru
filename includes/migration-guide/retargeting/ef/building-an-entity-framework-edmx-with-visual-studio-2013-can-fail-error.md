### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>Создание edmx Entity Framework с Visual Studio 2013 может завершиться ошибкой MSB4062 при использовании в EntityDeploySplit или EntityClean задач

|   |   |
|---|---|
|Подробные сведения|Средства MSBuild 12.0 (включенный в Visual Studio 2013) изменить расположения файлов MSBuild, вызывают старых файлов целей Entity Framework недопустим. В результате задачи <code>EntityDeploySplit</code> и <code>EntityClean</code> завершаются ошибкой, так как они не могут найти <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Обратите внимание, что этот разрыв связи с изменениями набор инструментов (MSBuild/VS) из-за изменения .NET Framework. Оно происходит только при обновлении средств разработчика, а не просто при обновлении .NET Framework.|
|Предложение|Для работы с новой начало макета MSBuild в .NET Framework 4.6 фиксируются Entity Framework целевых файлов. Проблема будет решена после обновления до этой версии. Кроме того, [это](http://stackoverflow.com/a/24249247/131944) решение можно использовать для исправления файлов целей построения напрямую.|
|Область|Значительно|
|Версия|4.5.1|
|Тип|Изменение целевой платформы|

