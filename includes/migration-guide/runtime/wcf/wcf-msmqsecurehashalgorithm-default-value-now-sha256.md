### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>Значение по умолчанию WCF MsmqSecureHashAlgorithm теперь — SHA256

|   |   |
|---|---|
|Подробные сведения|Начиная с платформы .NET Framework 4.7.1, алгоритм в WCF для сообщения Msmq подписи сообщения по умолчанию — SHA256. В .NET Framework 4.7 и более ранних версий алгоритм подписи сообщения по умолчанию-SHA1.|
|Предложение|Если возникнут проблемы совместимости с этим изменением на платформе .NET Framework 4.7.1 или более поздней версии, то можно выключить изменения, добавив следующую строку, чтобы <code>&lt;runtime&gt;</code>раздел файла app.config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.7.1|
|Тип|Среда выполнения|

