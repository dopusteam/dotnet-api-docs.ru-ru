### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Привязки WCF в режиме безопасности TransportWithMessageCredential

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6.1, привязка WCF, которая использует режим безопасности TransportWithMessageCredential можно настроить для получения сообщений с неподписанные &quot;для&quot; заголовки для асимметричных ключей безопасности. По умолчанию, без учета знака &quot;для&quot; заголовки будут отклонены в .NET 4.6.1. Они будут приниматься только в том случае, если переводит приложение в этот новый режим работы, с помощью переключателя Switch.System.ServiceModel.AllowUnsignedToHeader конфигурации. Это функция, включаемая, оно не влияет на поведение существующих приложений.|
|Предложение|Поскольку это возможность, включаемая пользователем, она не должна влиять на поведение существующих приложений. Для управления, используется ли новое поведение, используйте следующий параметр конфигурации:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Прозрачный|
|Версия|4.6.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

