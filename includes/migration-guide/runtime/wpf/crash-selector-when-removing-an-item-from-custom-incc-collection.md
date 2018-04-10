### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>Приводит к сбою в селекторе при удалении элемента из коллекции пользовательских INCC

|   |   |
|---|---|
|Подробные сведения|<code>T:System.InvalidOperationException</code> Может произойти в следующих сценариях:<ul><li>ItemsSource для <code>T:System.Windows.Controls.Primitives.Selector</code> является коллекцией с пользовательской реализации <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>.</li><li>Выбранный элемент будет удален из коллекции.</li><li><code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> Имеет <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> = 1 (что показывает неизвестную позицию).</li></ul>Стек вызовов исключения начинается с System.Windows.Threading.Dispatcher.VerifyAccess() на System.Windows.DependencyObject.GetValue (DependencyProperty dp) на System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject элемент) это исключение может возникнуть в .net 4.5, если приложение имеет более одного потока диспетчера. В .net 4.7 исключение также может возникнуть в приложениях с отдельным потоком, Dispatcher. Проблема устранена в .net 4.7.1.|
|Предложение|Обновление до .net 4.7.1.|
|Область|Дополнительный номер|
|Версия|4.7|
|Тип|Среда выполнения|

