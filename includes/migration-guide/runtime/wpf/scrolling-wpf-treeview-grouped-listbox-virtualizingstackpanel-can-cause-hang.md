### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>Прокрутка WPF TreeView или сгруппированные ListBox в VirtualizingStackPanel может привести к зависанию

|   |   |
|---|---|
|Подробные сведения|Версии платформы .NET Framework 4.5 прокрутки WPF <xref:System.Windows.Controls.TreeView?displayProperty=name> виртуализированных стека панель может привести к зависает при наличии поля в области просмотра (между элементами в <xref:System.Windows.Controls.TreeView?displayProperty=name>, например, или на элементе ItemsPresenter). Кроме того, в некоторых случаях элементы разных размеров в представлении могут привести к нестабильности даже при отсутствии полей.|
|Предложение|Этой ошибки можно избежать путем обновления до .NET Framework 4.5.1. Кроме того, можно удалить поля из просмотр коллекций (например <xref:System.Windows.Controls.TreeView?displayProperty=name>s) в виртуализированных стека панелей, если все элементы имеют одинаковый размер.|
|Область|Значительно|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

