### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer не удается десериализовать руководство сериализации с помощью другой версии .NET.

|   |   |
|---|---|
|Подробные сведения|Разработчиками предусмотрено <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> может использоваться только в том случае, если оба концах сериализации и десериализации совместное использование тех же типов CLR. Таким образом не гарантируется, сериализованный в одной версии платформы .NET Framework может быть десериализован с помощью другой версии.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> — Это тип, известное не десериализуемые правильно при сериализации в .NET Framework 4.5 или более ранней версии и десериализован в .NET Framework 4.5.1 и более поздних версиях.|
|Предложение|Существует несколько возможных решений этой проблемы:<ul><li>Обновите компьютер сериализации для использования в .NET Framework 4.5.1, а также.</li><li>Используйте <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> вместо <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> как не ожидает те же типы среды CLR на концах и сериализации.</li><li>Используйте <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> вместо <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> , так как оно не обеспечивает этой конкретной 4.5 -&gt;прервать 4.5.1.</li></ul>|
|Область|Дополнительный номер|
|Версия|4.5.1|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

