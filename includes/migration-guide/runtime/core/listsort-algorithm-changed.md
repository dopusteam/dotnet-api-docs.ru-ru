### <a name="listsort-algorithm-changed"></a>Изменить алгоритм List.Sort

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.5 <xref:System.Collections.Generic.List%601?displayProperty=name>алгоритм сортировки изменился (следует разумной сортировки, а не быстрой сортировки). <xref:System.Collections.Generic.List%601?displayProperty=name>не был стабильной сортировки, но это изменение может вызвать различные сценарии для сортировки работает нестабильно способами. Это просто означает, что эквивалентные элементы сортировка может выполняться в разном порядке при последующих вызовах API-интерфейса.|
|Предложение|Так как старый алгоритм сортировки также работает нестабильно (хотя различными способами), должно быть не код, зависящий от эквивалентные элементы всегда Сортировка в определенном порядке. Если имеются экземпляры кода, в зависимости от того, и выполняется Счастливое с старое поведение, этот код следует обновить для использования компаратор, который будет детерминированного сортировки элементов в требуемом порядке.|
|Область|Прозрачный|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

