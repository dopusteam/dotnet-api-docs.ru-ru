### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Коды ошибок для maxRequestLength или maxReceivedMessageSize различаются

|   |   |
|---|---|
|Подробные сведения|Сообщения в WCF веб-службы, размещенные в Internet Information Services (IIS) или ASP.NET Development Server, превышающие maxRequestLength (в ASP.NET) или maxReceivedMessageSize (в WCF) имеют различные ошибки код состояния codeThe HTTP изменился с 400 (неправильный запрос ) на 413 (слишком большой объект запроса) и сообщения, превышающие maxRequestLength или параметра maxReceivedMessageSize throw <xref:System.ServiceModel.ProtocolException?displayProperty=name> исключение. Сюда входят случаи, в которых режимом передачи является потоковым.|
|Предложение|Это изменение облегчает отладку в тех случаях, когда длина сообщения превышает ограничения, установленные ASP.NET или WCF. Необходимо изменить любой код, который выполняет обработку на основе кода состояния HTTP 400.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|

