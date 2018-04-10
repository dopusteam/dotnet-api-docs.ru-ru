### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs перечисляются не профилировщиками

|   |   |
|---|---|
|Подробные сведения|В .NET Framework v4.5.1, API профилирования <code>RootReferences2()</code> неправильно никогда не возвращает <code>COR_PRF_GC_ROOT_HANDLE</code> (они возвращаются в виде <code>COR_PRF_GC_ROOT_OTHER</code> вместо). Эта проблема исправлена, начиная с .NET Framework 4.6.|
|Предложение|Эта проблема была устранена в платформе .NET Framework 4.6 и можно обращаться путем обновления для этой версии платформы .NET Framework.|
|Область|Дополнительный номер|
|Версия|4.5.1|
|Тип|Среда выполнения|

