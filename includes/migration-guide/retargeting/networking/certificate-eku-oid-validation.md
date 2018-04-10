### <a name="certificate-eku-oid-validation"></a>Проверка кода Объекта EKU сертификата

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6 <xref:System.Net.Security.SslStream> или <xref:System.Net.ServicePointManager> классы выполнять проверку идентификатор (OID) расширенного использования ключа (EKU) объекта. Расширение расширенного использования ключа (EKU) — это коллекция идентификаторов объектов (OID), которые указывают приложения, использующие ключ. Проверка Объекта EKU использует обратные вызовы удаленный сертификат, чтобы обеспечить удаленный сертификат правильно OID для своей цели.|
|Предложение|Если это изменение нежелательно, можно отключить проверки кода Объекта EKU сертификата путем добавления следующих переключиться на [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) в [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) из вашей файл конфигурации приложения:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Этот параметр предоставляется для обеспечения обратной совместимости. В противном случае его использование не рекомендуется.</blockquote> |
|Область|Дополнительный номер|
|Версия|4.6|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

