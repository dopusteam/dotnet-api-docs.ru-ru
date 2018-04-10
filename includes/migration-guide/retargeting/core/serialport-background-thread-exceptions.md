### <a name="serialport-background-thread-exceptions"></a>SerialPort фоновый поток исключения

|   |   |
|---|---|
|Подробные сведения|Фоновые потоки, созданные с помощью <xref:System.IO.Ports.SerialPort> потоков больше не завершить процесс при возникновении исключения ОС. В приложениях, предназначенных для .NET Framework 4.7 и более ранних версий, процесс был завершен при возникновении исключения операционная система в фоновом потоке, созданных с помощью <xref:System.IO.Ports.SerialPort> потока. В приложениях, предназначенных для .NET Framework 4.7.1 или более поздней версии, фоновые потоки ожидания для событий операционной системы, связанные к последовательному порту активного и мог произойти сбой в некоторых случаях, например внезапное удаления последовательного порта.|
|Предложение|Для приложений, ориентированных на .NET Framework 4.7.1, можно отключить обработку исключений, если она нежелательна, добавив следующую команду, чтобы <code>&lt;runtime&gt;</code> части вашего <code>app.config</code> файла:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Для приложений, предназначенных для более ранних версий платформы .NET Framework, но выполняться на платформе .NET 4.7.1 или более поздней версии, можно включить, добавив следующий код для обработки исключений <code>&lt;runtime&gt;</code> части вашего <code>app.config</code> файла:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.7.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

