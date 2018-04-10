### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt; всегда возвращает кэшированное экземпляра

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET 4.5 <xref:System.Linq.Enumerable.Empty%60%601> всегда возвращает кэшированный внутренний экземпляр <xref:System.Collections.Generic.IEnumerable%601>. Ранее <xref:System.Linq.Enumerable.Empty%60%601> будет кэшировать пустой <xref:System.Collections.Generic.IEnumerable%601> на момент вызова API-интерфейса, это значит, что в некоторых условиях, в котором <xref:System.Linq.Enumerable.Empty%60%601> был вызван быстро и параллельно, разные экземпляры типа, которые могут возвращаться для различных вызовов API-ИНТЕРФЕЙС.|
|Предложение|Так как прежнее поведение было недетерминированным, код вряд ли зависит от него. Однако в том маловероятном случае, когда выполняется сравнение пустых перечислений и ожидается, что они будут неравными, следует создать явные пустые массивы (<code>new T[0]</code>) и не использовать <xref:System.Linq.Enumerable.Empty%60%601>.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

