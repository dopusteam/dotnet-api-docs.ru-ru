### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Изменения в поведении для Task.WaitAll методы с аргументами времени ожидания

|   |   |
|---|---|
|Подробные сведения|Поведение Task.WaitAll в был выполнен более согласованной .NET 4.5.In .NET Framework 4, эти методы поведение было непоследовательным. По истечении времени ожидания, если одна или несколько задач были завершены или отменены до вызова метода, метод вызывал исключение <xref:System.AggregateException?displayProperty=name>. По истечении времени ожидания, если ни одна задача не была завершена или отменена до вызова метода, однако одна или несколько задач входили в эти состояния после вызова метода, метод возвращал значение false.<br/><br/>В .NET Framework 4.5, эти перегрузки метода теперь возвращают значение false, если все задачи по-прежнему выполняются после истечения интервала времени ожидания, и вызывают исключение <xref:System.AggregateException?displayProperty=name> только в том случае, если входная задача была отменена (независимо от того, была ли она до или после метода вызов), а не выполняются никакие другие задачи.|
|Предложение|Если <xref:System.AggregateException?displayProperty=name> перехвачено с точки зрения обнаружение задачу, которая была отменена до вызова метода Метод WaitAll вызываемого кода вместо этого делать же обнаружения через свойство IsCanceled (например:. Any(t =&gt; t.IsCanceled)) с момента .NET 4.6 только вызывает исключение в этом случае, если выполняются все ожидающей задачи до времени ожидания.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

