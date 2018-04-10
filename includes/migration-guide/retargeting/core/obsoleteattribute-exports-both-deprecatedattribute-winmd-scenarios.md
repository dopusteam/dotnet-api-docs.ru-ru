### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>Экспортирует ObsoleteAttribute, например ObsoleteAttribute и DeprecatedAttribute в сценариях WinMD

|   |   |
|---|---|
|Подробные сведения|При создании библиотеки метаданных Windows (winmd-файл), <xref:System.ObsoleteAttribute?displayProperty=name> атрибут экспортируется как <xref:System.ObsoleteAttribute?displayProperty=name> и [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Предложение|При перекомпиляции существующего исходного кода, использующего <xref:System.ObsoleteAttribute?displayProperty=name> атрибута могут выдаваться предупреждения при использовании кода из C + +/ CX или JavaScript.We не рекомендуется применять атрибуты <xref:System.ObsoleteAttribute?displayProperty=name> и [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) коду в управляемых сборок; это может привести к предупреждениям сборки.|
|Область|Пограничный случай|
|Версия|4.5.1|
|Тип|Изменение целевой платформы|

