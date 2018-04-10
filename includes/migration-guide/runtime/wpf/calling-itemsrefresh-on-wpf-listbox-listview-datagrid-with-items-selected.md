### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>Вызов Items.Refresh WPF ListBox, ListView или DataGrid с выбранных элементов может вызвать повторяющиеся элементы для отображения в элементе

|   |   |
|---|---|
|Подробные сведения|В .NET Framework 4.5, вызов ListBox.Items.Refresh из кода, при выборе элементов в <xref:System.Windows.Controls.ListBox?displayProperty=name> может привести к выбранные элементы в дублироваться в списке. Возникает аналогичная проблема возникает с <xref:System.Windows.Controls.ListView?displayProperty=name> и <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Эта проблема устранена в EntityFramework 4.6.|
|Предложение|Может обойти эту проблему, программным путем, сняв элементов перед <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> вызывается и повторно выбрав их после завершения вызова. Кроме того, эта проблема была устранена в .NET Framework 4.6 и может быть решена путем обновления до этой версии платформы .NET Framework.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

