### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>Доступ к WPF DataGrid выбранные элементы из обработчика события UnloadingRow элемента управления DataGrid может вызвать исключение NullReferenceException

|   |   |
|---|---|
|Подробные сведения|Из-за ошибки в .NET Framework 4.5, обработчики событий для <xref:System.Windows.Controls.DataGrid> событий, связанных с удаление строки может привести к <xref:System.NullReferenceException?displayProperty=name> исключение, если они обращаются к <xref:System.Windows.Controls.DataGrid> <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> или <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> свойства.|
|Предложение|Эта проблема была устранена в платформе .NET Framework 4.6 и можно обращаться путем обновления для этой версии платформы .NET Framework.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

