### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>ConcurrentDictionary, сериализованного в .NET 4.5 с NetDataContractSerializer не может быть десериализован в .NET 4.5.1 или 4.5.2

|   |   |
|---|---|
|Подробные сведения|Из-за внутренних изменений в тип <xref:System.Collections.Concurrent.ConcurrentDictionary%602> с .NET Framework 4.5 сериализуемых объектов с помощью <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> не может быть десериализован в .NET Framework 4.5.1 или 4.5.2.Note .NET Framework, перемещение в другие (направление сериализация с .NET Framework 4.5.x и десериализации с помощью .NET Framework 4.5) работает. Аналогичным образом все сериализации кросс Платформенная 4.x работает с 4.6.Serializing .NET Framework и десериализации с помощью одной версии платформы .NET Framework не затрагивается.|
|Предложение|Если это необходимо для сериализации и десериализации <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> между .NET Framework 4.5 и .NET Framework 4.5.1/4.5.2 альтернативный сериализатор, например <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> или <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> сериализатор следует использовать вместо <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. Кроме того так как эта проблема устранена в платформе .NET Framework 4.6, его можно решить, обновление до этой версии платформы .NET Framework.|
|Область|Дополнительный номер|
|Версия|4.5.1|
|Тип|Среда выполнения|

