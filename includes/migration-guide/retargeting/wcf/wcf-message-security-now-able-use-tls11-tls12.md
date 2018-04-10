### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>Безопасность сообщений WCF теперь могут использовать TLS1.1 и TLS1.2

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.7, клиенты могут настроить TLS1.1 и TLS1.2 в безопасность сообщений WCF помимо SSL3.0 и TLS1.0 через параметры конфигурации приложения.|
|Предложение|В .NET Framework 4.7 Поддержка TLS1.1 и TLS1.2 в безопасность сообщений WCF отключена по умолчанию. Его можно включить, добавив следующую строку, чтобы <code>&lt;runtime&gt;</code> раздел файла app.config или web.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.7|
|Тип|Изменение целевой платформы|

