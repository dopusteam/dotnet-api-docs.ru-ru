### <a name="only-tls-10-11-and-12-protocols-supported-in-systemnetservicepointmanager-and-systemnetsecuritysslstream"></a>Только протоколы Tls 1.0, 1.1 и 1.2, поддерживаемые в System.Net.ServicePointManager и System.Net.Security.SslStream

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6 <xref:System.Net.ServicePointManager> и <xref:System.Net.Security.SslStream> только классы могут использовать один из трех следующих протоколов: Tls1.0, Tls1.1 и Tls1.2. Протокол SSL 3.0 и шифрование RC4 не поддерживаются.|
|Предложение|Является рекомендуется обновить приложения на стороне сервера для использования Tls1.0, Tls1.1 и Tls1.2. Если это невозможно, или если клиентские приложения не работают, можно использовать класс <xref:System.AppContext?displayProperty=name>, чтобы отказаться от этой функции одним из двух способов.<ol><li>Программным путем совместимости переключается <xref:System.AppContext?displayProperty=name>, как описано [здесь](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>Путем добавления следующей строки <code>&lt;runtime&gt;</code> раздел файла app.config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSchUseStrongCrypto=true&quot;/&gt;</code>;</li></ol>|
|Область|Дополнительный номер|
|Версия|4.6|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Net.SecurityProtocolType.Ssl3?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl2?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl3?displayProperty=nameWithType></li></ul>|

