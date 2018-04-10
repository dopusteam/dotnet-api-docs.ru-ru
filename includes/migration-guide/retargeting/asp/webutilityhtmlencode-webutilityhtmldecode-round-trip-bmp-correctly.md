### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode и WebUtility.HtmlDecode приема-передачи BMP правильно

|   |   |
|---|---|
|Подробные сведения|Для приложений, предназначенных для .NET Framework 4.5, символы, которые находятся за пределами цикла обработки базовый многоязыковый набор кодировок (BMP) правильно, когда они передаются <xref:System.Net.WebUtility.HtmlDecode(System.String)> методы.|
|Предложение|Это изменение должно не оказывают влияния на текущие приложения, но для восстановления исходного поведения задайте <code>targetFramework</code> атрибут <code>&lt;httpRuntime&gt;</code> строку, отличных от &quot;4.5&quot;. Также можно задать атрибуты <code>unicodeEncodingConformance</code> и <code>unicodeDecodingConformance</code> элемента конфигурации <code>&lt;webUtility&gt;</code>, чтобы контролировать это поведение вне зависимости от целевой версии .NET Framework.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

