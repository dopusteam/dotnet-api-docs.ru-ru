### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException в коде из ImageSourceConverter.ConvertFrom обработки исключений

|   |   |
|---|---|
|Подробные сведения|Ошибки в код для обработки исключений <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> причиной неправильного <xref:System.NullReferenceException?displayProperty=name> исключение вместо предполагаемого исключение (например <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), это изменение устраняет эту ошибку, чтобы метод теперь вызывает исключение вправо. По умолчанию все приложения, предназначенные для .NET Framework 4.6.2 и ниже будет продолжать вызывать <xref:System.NullReferenceException?displayProperty=name> для совместимости, разработчиков, предназначенных для .NET Framework 4.7 и более поздних версий должны увидеть правой exceptions.// замены пространство с символом «x», если применимо|
|Предложение|Разработчики, желающие вернуться в начало <xref:System.NullReferenceException?displayProperty=name> при предназначенных для .NET Framework 4.7 можно добавить или слияния следующий файл App.config для своего приложения:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.7|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

