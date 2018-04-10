### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>Рассматривает все claimTypes X509CertificateClaimSet.FindClaims

|   |   |
|---|---|
|Подробные сведения|В приложениях, предназначенных для .NET Framework 4.6.1, если X509 набор утверждений инициализируется из сертификата, имеющего несколько DNS-записей в поле SAN <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> метод пытается сопоставить аргумент claimType со всеми записями DNS. Для приложений, предназначенных для предыдущих версий платформы .NET Framework <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> метод пытается сопоставить аргумент claimType только с последней записью DNS.|
|Предложение|Это изменение затрагивает только приложения, предназначенные для .NET Framework 4.6.1. Это изменение может быть отключено (или включено, если используются версии, предшествующие 4.6.1) с помощью параметра совместимости [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation).|
|Область|Дополнительный номер|
|Версия|4.6.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

