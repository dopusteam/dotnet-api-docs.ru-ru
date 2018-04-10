### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>Изменение свойства IsEnabled родительского элемента управления TextBlock влияет на все дочерние элементы

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6.2, изменение <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> свойства родителя <xref:System.Windows.Controls.TextBlock?displayProperty=name> управления влияет на все дочерние элементы управления (например, гиперссылки и кнопки) <xref:System.Windows.Controls.TextBlock?displayProperty=name> элемента управления. В .NET Framework 4.6.1 и более ранних версий, элементы управления внутри <xref:System.Windows.Controls.TextBlock?displayProperty=name> была всегда отражает состояние <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> свойство <xref:System.Windows.Controls.TextBlock?displayProperty=name> родительского.|
|Предложение|Отсутствует. Это изменение соответствует ожидаемому поведению для элементов управления, содержащихся внутри элемента управления <xref:System.Windows.Controls.TextBlock?displayProperty=name>.|
|Область|Дополнительный номер|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

