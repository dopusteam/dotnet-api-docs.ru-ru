### <a name="deadlock-may-result-when-using-reentrant-services"></a>При использовании реентерабельным служб может привести к взаимоблокировки

|   |   |
|---|---|
|Подробные сведения|Взаимоблокировка может привести к повторных входящих вызовов службы, которая ограничивает экземпляров службы для одного потока выполнения одновременно. Вероятность возникновения этой проблемы службы имеют следующие <xref:System.ServiceModel.ServiceBehaviorAttribute> в своем коде:<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|Предложение|Чтобы устранить эту проблему, выполните следующие действия.<ul><li>Значение режима параллелизма службы <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> или &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;. Пример:</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>Установите последнее обновление для .NET Framework 4.6.2 или обновление до новой версии платформы .NET Framework. Это приведет к отключению поток <xref:System.Threading.ExecutionContext> в <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>. Такое поведение является настраиваемым; он эквивалентен, добавив следующий параметр приложения в файл конфигурации:</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.6.2|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

