### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task больше не вызывают ObjectDisposedException после удаления объекта

|   |   |
|---|---|
|Подробные сведения|За исключением <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> больше не вызывают методы <xref:System.ObjectDisposedException?displayProperty=name> исключение после удаления объекта. Это изменение обеспечивает возможность использования кэшированных задач. Например, метод может возвратить кэшированную задачу для представления уже выполненной операции вместо выделения новой задачи. В предыдущих версиях платформы .NET Framework это было невозможно, поскольку любой потребитель задачи мог удалить ее, что делало ее непригодной для использования.|
|Предложение|Имейте в виду, что больше не может вызывать методы задач <xref:System.ObjectDisposedException?displayProperty=name> в случаях, когда удаляется объект. Если приложение было в зависимости от этого исключения, чтобы знать, что задача была удалена, ее должны быть обновлены до явно не проверять состояние задачи с помощью <xref:System.Threading.Tasks.Task.Status>.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|

