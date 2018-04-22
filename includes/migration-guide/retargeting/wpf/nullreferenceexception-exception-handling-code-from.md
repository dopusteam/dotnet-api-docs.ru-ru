### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException в коде обработки исключений из ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Подробные сведения|Ошибка в коде обработки исключений для <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> приводила к возникновению неправильного исключения <xref:System.NullReferenceException?displayProperty=name> вместо ожидаемого исключения (например <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>). Это изменение устраняет эту ошибку, и теперь метод вызывает правильное исключение. По умолчанию все приложения, предназначенные для .NET Framework 4.6.2 и более ранних версий, будут по-прежнему вызывать исключение <xref:System.NullReferenceException?displayProperty=name> в целях совместимости. В .NET Framework 4.7 и более поздних версий будут отображаться правильные исключения.// Замените пробел символом "x" по возможности|
|Предложение|Разработчики, желающие по-прежнему получать <xref:System.NullReferenceException?displayProperty=name> при работе с .NET Framework 4.7, могут добавить следующее в файл App.config приложения:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.7|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

