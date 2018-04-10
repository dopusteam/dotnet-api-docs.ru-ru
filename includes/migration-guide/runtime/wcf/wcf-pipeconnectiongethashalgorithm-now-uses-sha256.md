### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>Теперь используется SHA256, WCF PipeConnection.GetHashAlgorithm

|   |   |
|---|---|
|Подробные сведения|Начиная с платформы .NET Framework 4.7.1, Windows Communication Foundation использует хэш SHA256 для формирования случайных имен для именованных каналов. В .NET Framework 4.7 и более ранних версий он используется хэш SHA1.|
|Предложение|Если возникнут проблемы совместимости с этим изменением на платформе .NET Framework 4.7.1 или более поздней версии, то можно отказаться от участия его, добавив следующую строку в <code>&lt;runtime&gt;</code> раздел файла app.config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.7.1|
|Тип|Среда выполнения|

