### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Больше не может установить EnableViewStateMac значение false

|   |   |
|---|---|
|Подробные сведения|ASP.NET теперь не позволяет разработчикам указывать <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> или <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. Код проверки подлинности сообщения (MAC) состояния просмотра теперь принудительно применяется для всех запросов со встроенным состоянием просмотра. Только приложений, которые явным образом присвойте свойству EnableViewStateMac <code>false</code> затрагиваются.|
|Предложение|EnableViewStateMac должно присваиваться значение true, и список ошибок MAC должны быть устранены (как описано в [в этом руководстве](https://support.microsoft.com/kb/2915218), который содержит несколько разрешений, в зависимости от причины ошибки MAC).|
|Область|Значительно|
|Версия|4.5.2|
|Тип|Среда выполнения|

