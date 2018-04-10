### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>Заблокированы управляемого браузера размещения элементов управления .NET Framework 1.1 и 2.0

|   |   |
|---|---|
|Подробные сведения|Размещение этих элементов управления в Internet Explorer блокируется.|
|Предложение|Internet Explorer не сможет запустить приложение, в котором используются управляемые элементы управления, размещенные в браузере. Можно восстановить прежнее поведение, параметру enableiehosting подраздела реестра <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> для <code>1</code> для x86 систем и для 32-разрядных процессов в x64 систем и задав <code>EnableIEHosting</code> значение раздела реестра, <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>для <code>1</code> для 64-разрядных процессов в x64 систем.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|

