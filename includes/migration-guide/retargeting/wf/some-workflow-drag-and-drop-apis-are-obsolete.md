### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Некоторые интерфейсы API и перетащите рабочего процесса, являются устаревшими

|   |   |
|---|---|
|Подробные сведения|Этот API и перетащите рабочего процесса является устаревшим и будут отображаться предупреждения компилятора, если приложение перестраивается в 4.5.|
|Предложение|Новый <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> следует использовать API-интерфейсы, поддерживающие операции с нескольких объектов. Кроме того, можно подавить предупреждения сборки или избежать их вывода с помощью более старой версией компилятора. Интерфейсы API по-прежнему поддерживаются.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

