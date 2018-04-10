### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView создает исключение ArgumentOutOfRangeException

|   |   |
|---|---|
|Подробные сведения|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> будет работать асинхронно, если включена виртуализация столбцов, но ширина столбцов еще не было определено.  Если столбцы удаляются до выполнения асинхронной работы, <xref:System.ArgumentOutOfRangeException?displayProperty=name> может произойти.|
|Предложение|Одно из следующих действий:<ol><li>Обновление до .NET 4.7.</li><li>Установите обновление, последняя версия обслуживания для .NET 4.6.2.</li><li>Избежание удаления столбцов до асинхронный ответ <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> завершена.</li></ol>|
|Область|Пограничный случай|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

