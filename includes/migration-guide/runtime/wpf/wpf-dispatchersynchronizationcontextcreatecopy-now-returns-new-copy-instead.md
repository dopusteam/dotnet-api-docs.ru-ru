### <a name="wpf-dispatchersynchronizationcontextcreatecopy-now-returns-a-new-copy-instead-of-the-current-instance"></a>WPF DispatcherSynchronizationContext.CreateCopy теперь возвращает новую копию вместо текущего экземпляра

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4 <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> возвращает ссылку на текущий экземпляр, как оптимизировать производительность. В .NET Framework 4.5 он возвращает новый экземпляр, что позволяет впервые делать заключение о том, что одинаковые ссылки указывают на то, что выполняющийся поток находится в правильном контексте синхронизации.  Маловероятно, что код, который проверяет подлинность эти ссылки будут затронуты, но из-за изменения код, вызовы <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> следует тестировать в рамках миграции на .NET Framework 4.5 или более поздней версии.|
|Предложение|Имейте в виду, что <xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy> теперь возвращают новый <xref:System.Threading.SynchronizationContext?displayProperty=name> объекта. Ранее код, который использовал эквивалентность ссылок, на самом деле не проверялся на нахождение в правильном контексте, но проверяется при создании в .NET 4.5 или более поздних версиях.  Хотя маловероятно, что это приведет к серьезным проблемам, проверки путей к затронутому коду должно быть достаточно для определения проблемы.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Threading.DispatcherSynchronizationContext.CreateCopy?displayProperty=nameWithType></li></ul>|

