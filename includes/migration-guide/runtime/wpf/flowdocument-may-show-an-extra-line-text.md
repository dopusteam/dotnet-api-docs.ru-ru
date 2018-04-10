### <a name="flowdocument-may-show-an-extra-line-of-text"></a>Документ нефиксированного формата могут отображаться дополнительные строки текста

|   |   |
|---|---|
|Подробные сведения|В некоторых случаях <xref:System.Windows.Documents.FlowDocument> элемент будет отображаться дополнительная строка текста, при выполнении на платформе .NET Framework 4.5, по сравнению с отображением при запуске на платформе .NET Framework 4.0. Нет известных случаях изменения вызывает любой текст, который отображается неправильно или illegibly, но это может привести к текст, отображаемый, ранее было <xref:System.Windows.Documents.FlowDocument>просмотра.|
|Предложение|В некоторых случаях уменьшается на единицу свойство PageHeight отображаемого элемента можно восстановить предыдущего количества отображаемых строк.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

