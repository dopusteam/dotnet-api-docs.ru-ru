### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF сериализует Expressions.Literal&lt;T&gt; даты по-разному теперь (разбивает пользовательские средства синтаксического анализа XAML)

|   |   |
|---|---|
|Подробные сведения|Связанный <xref:System.Windows.Markup.ValueSerializer> преобразует объект <xref:System.DateTime?displayProperty=name> или <xref:System.DateTimeOffset?displayProperty=name> во-вторых, объекта и <xref:System.DateTime.Millisecond?displayProperty=name> компоненты не равны нулю и (для <xref:System.DateTime?displayProperty=name> значение) которого <xref:System.DateTime.Kind> свойство не может быть указан для свойства элемента синтаксис вместо строки. Это изменение позволяет передавать значения <xref:System.DateTime?displayProperty=name> и <xref:System.DateTimeOffset?displayProperty=name> в оба конца. Пользовательские средства синтаксического анализа XAML, в которых предполагается, что входные данные XAML имеют синтаксис атрибутов, не будут работать правильно.|
|Предложение|Это изменение позволяет передавать значения <xref:System.DateTime?displayProperty=name> и <xref:System.DateTimeOffset?displayProperty=name> в оба конца. Пользовательские средства синтаксического анализа XAML, в которых предполагается, что входные данные XAML имеют синтаксис атрибутов, не будут работать правильно.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|

