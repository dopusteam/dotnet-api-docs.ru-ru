### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>Алгоритм хэширования по умолчанию для WPF PackageDigitalSignatureManager теперь является SHA256

|   |   |
|---|---|
|Подробные сведения|<code>System.IO.Packaging.PackageDigitalSignatureManager</code> Предоставляет функциональные возможности для цифровых подписей относительно пакеты WPF.  В .NET Framework 4.7 и более ранних версий, алгоритм по умолчанию (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) используется для подписи частей пакета была SHA1.  Из-за последние обеспечения безопасности с помощью SHA1, это значение по умолчанию было изменено на SHA256 начиная с .NET Framework 4.7.1.  Это изменение затрагивает все Подписание пакета, включая XPS-документы.|
|Предложение|Разработчик, желающий использовать это изменение во время целевая версия ниже .NET 4.7.1 framework или если разработчику требуется прежние функции при ориентировании на .NET 4.7.1 или выше, может правильно настроить следующий флаг параметров AppContext.  Значение true приведет к SHA1, используемого в качестве алгоритма по умолчанию; Возвращает значение false SHA256.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.7.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

