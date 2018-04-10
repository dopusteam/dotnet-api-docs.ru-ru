### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear не удаляет дубликаты из SelectedItems

|   |   |
|---|---|
|Подробные сведения|Предположим, что селектор (с включен множественный выбор) содержит повторяющиеся значения в его <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> коллекцию — тот же элемент указан более одного раза.  Удаление этих элементов из источника данных (например, с помощью вызова Items.Clear) не удается удалить их из <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; только первый экземпляр удаляется. Кроме того последующее использование <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (например SelectedItems.Clear()) могут вызвать проблемы, такие как <xref:System.ArgumentException?displayProperty=name>, так как <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> содержит элементы, которые больше не находятся в источнике данных.|
|Предложение|По возможности обновите .NET 4.6.2.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

