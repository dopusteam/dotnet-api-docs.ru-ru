### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Рабочий процесс теперь создает исходное исключение вместо NullReferenceException в некоторых случаях

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4.6.2 и более ранних версий, если метод Execute действия рабочего процесса создает исключение с <code>null</code> значение для <xref:System.Exception.Message> , System.Activities рабочего процесса вызывает <xref:System.NullReferenceException?displayProperty=name>, маскировка исходное исключение. В .NET Framework 4.7 ранее маскированные исключения.|
|Предложение|Если код основан на обработку <xref:System.NullReferenceException?displayProperty=name>, измените его, чтобы перехватывать исключения, которые могут быть созданы из настраиваемых действий.|
|Область|Дополнительный номер|
|Версия|4.7|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

