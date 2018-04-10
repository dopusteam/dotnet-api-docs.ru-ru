### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap успешно преобразует значки с кадрами PNG в объекты растрового изображения

|   |   |
|---|---|
|Подробные сведения|Начиная с приложений, предназначенных для .NET Framework 4.6 <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> метода успешно преобразует значки с кадрами PNG в объекты растрового изображения. В приложениях, предназначенных для .NET Framework 4.5.2 и более ранних версиях <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> вызывает исключение <xref:System.ArgumentOutOfRangeException> исключение, если объект значка содержит кадры PNG. Это изменение затрагивает приложения, которые компилируются повторно для платформы .NET Framework 4.6 и в которых реализуется специальная обработка <xref:System.ArgumentOutOfRangeException> , возникает, когда объект значок содержит кадры PNG. При выполнении в .NET Framework 4.6 преобразование проходит успешно, исключение <xref:System.ArgumentOutOfRangeException> больше не создается, и поэтому обработчик исключений больше не вызывается.|
|Предложение|Если такое поведение нежелательно, можно сохранить прежнее поведение, добавив следующий элемент <code>&lt;runtime&gt;</code> раздел файла app.config:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Если файл app.config уже содержит <code>AppContextSwitchOverrides</code> элемента, новое значение должны быть объединены со значением атрибута следующим образом:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.6|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

