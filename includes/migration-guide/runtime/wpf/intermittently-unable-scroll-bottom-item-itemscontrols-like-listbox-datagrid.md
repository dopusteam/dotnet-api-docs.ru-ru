### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>Периодически удается выполнить прокрутку к элементу нижней ItemsControls (например, сетка и ListBox) при использовании пользовательских DataTemplates

|   |   |
|---|---|
|Подробные сведения|В некоторых случаях ошибки в .NET Framework 4.5 вызывает ItemsControls (как <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>и т.д.) не выполнить прокрутку их нижний элемент при использовании пользовательских DataTemplates. Если попытка прокрутки предпринимается повторно (после прокрутки вверх), прокрутка будет работать.|
|Предложение|Эта проблема была устранена в .NET Framework 4.5.2 и может быть решена путем обновления до этой версии (или более поздней) платформы .NET Framework. Кроме того, пользователи по-прежнему могут перетаскивать полосы прокрутки к последним элементам в этих коллекциях, однако для успешного выполнения этой задачи это может потребоваться сделать дважды.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|

