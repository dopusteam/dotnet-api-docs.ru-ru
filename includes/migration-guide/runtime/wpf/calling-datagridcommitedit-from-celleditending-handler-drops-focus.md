### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>Вызов DataGrid.CommitEdit из обработчика CellEditEnding удаляет фокус

|   |   |
|---|---|
|Подробные сведения|Вызов <xref:System.Windows.Controls.DataGrid.CommitEdit> из одного из <xref:System.Windows.Controls.DataGrid?displayProperty=name> <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> вызывает обработчики событий <xref:System.Windows.Controls.DataGrid?displayProperty=name> потеряет фокус.|
|Предложение|Это ошибка исправлена в .NET Framework 4.5.2, поэтому ее можно избежать путем обновления .NET Framework. Кроме того, его можно избежать, явно повторно при выборе <xref:System.Windows.Controls.DataGrid?displayProperty=name> после вызова <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

