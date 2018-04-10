### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>Изменено с MD5 на SHA1 контрольные суммы рабочего процесса

|   |   |
|---|---|
|Подробные сведения|Для поддержки отладки в Visual Studio, среда выполнения рабочего процесса приводит к возникновению ошибки контрольной суммы для экземпляра рабочего процесса, используя алгоритм хэширования. В .NET Framework 4.6.2 и более ранних версий хэширование контрольной суммы рабочего процесса используется алгоритм MD5, вызвавшее проблемы в системах с поддержкой стандарта FIPS. Начиная с .NET Framework 4.7, алгоритм — SHA1. Если код имеет постоянное эти контрольные суммы, они будут несовместимы.|
|Предложение|Если код не удалось загрузить экземпляры рабочих процессов из-за ошибки контрольной суммы, включите параметр <code>AppContext</code> переключения &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; значение true. В коде:<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>Или в файле конфигурации:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.7|
|Тип|Изменение целевой платформы|

