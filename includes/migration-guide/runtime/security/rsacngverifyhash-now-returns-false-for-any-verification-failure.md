### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash теперь возвращает значение False для любой сбой проверки

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6.2, этот метод возвращает <strong>False</strong> Если саму подпись имеют неправильный формат. Теперь возвращает значение false для любой сбой проверки. В .NET Framework 4.6 и 4.6.1, метод создает <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> Если саму подпись имеют неправильный формат.|
|Предложение|Любой код, выполнение которого зависит от обработки <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> вместо этого следует выполнить, если проверка завершается с ошибкой, а метод возвращает <strong>False</strong>.|
|Область|Дополнительный номер|
|Версия|4.6.2|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

