### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>TargetFrameworkName для домена приложения по умолчанию больше не по умолчанию имеет значение null, если не установлено

|   |   |
|---|---|
|Подробные сведения|<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> Был ранее null в домене приложения по умолчанию, если не было задано явным образом. Начиная с 4.6, <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> свойство для домена приложения по умолчанию будет иметь значение по умолчанию, производный от TargetFrameworkAttribute (при его наличии). Домены приложений не по умолчанию будет продолжать наследовать их <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> из домена приложения по умолчанию (который не будет по умолчанию NULL в 4.6) если она явно не переопределено.|
|Предложение|Следует обновить код так, чтобы он не зависел от <xref:System.AppDomainSetup.TargetFrameworkName>, принимающего п умолчанию значение NULL. Если требуется, чтобы свойство продолжало принимать значение NULL, ему можно явно присвоить это значение.|
|Область|Пограничный случай|
|Версия|4.6|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

