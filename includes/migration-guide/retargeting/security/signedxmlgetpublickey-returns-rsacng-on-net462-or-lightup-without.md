### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey возвращает RSACng net462 (или lightup) без изменения целевой платформы

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6.2, конкретным типом объекта, возвращаемого <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> метод изменен (без особенность) от реализации CryptoServiceProvider на реализацию Cng. Это из-за изменения реализации с помощью <code>certificate.PublicKey.Key</code> с помощью внутреннего <code>certificate.GetAnyPublicKey</code> которого пересылает <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.|
|Предложение|Начиная с приложений, выполняющихся в .NET Framework 4.7.1, можно использовать CryptoServiceProvider реализацию, используемую по умолчанию в платформе .NET Framework 4.6.1 и переключитесь в более ранних версиях, добавив следующую конфигурацию [среды выполнения](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)раздел файла конфигурации приложения:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.6.2|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

