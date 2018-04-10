### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>WPF текстовое поле текст отображается другой цвет, когда текстовое поле неактивно.

|   |   |
|---|---|
|Подробные сведения|В .NET 4.5, если элемент управления текстовым полем WPF неактивен (в нем отсутствует фокус), выбранный текст внутри поля будут отображаться цветом, отличным от того, когда элемент управления является активным.|
|Предложение|Можно восстановить прежнее поведение (.NET 4.0), задав <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> свойства <code>false</code>.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

