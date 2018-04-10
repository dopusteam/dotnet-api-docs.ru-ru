### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>По умолчанию используется текстовое поле WPF Отменить ограничение в 100

|   |   |
|---|---|
|Подробные сведения|В .NET 4.5 ограничение отмены по умолчанию для текстового поля WPF равно 100 (в отличие от неограниченного в .NET 4.0).|
|Предложение|В случае слишком низкой отмены ограничение в 100 ограничение можно задать явным образом <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

