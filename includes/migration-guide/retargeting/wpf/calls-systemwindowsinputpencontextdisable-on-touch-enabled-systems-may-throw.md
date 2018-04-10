### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Вызовы System.Windows.Input.PenContext.Disable в системах с поддержкой сенсорного ввода может вызвать исключение ArgumentException

|   |   |
|---|---|
|Подробные сведения|В некоторых случаях вызовы внутренней <strong>System.Windows.Intput.PenContext.Disable</strong> метод в системах с поддержкой сенсорного ввода может генерировать необработанное <code>T:System.ArgumentException</code> из-за повторного входа.|
|Предложение|Эта проблема будет устранена в 4.7 .NET Framework. Чтобы избежать возникновения исключения, обновление до версии платформы .NET Framework, начиная с .NET Framework 4.7.|
|Область|Пограничный случай|
|Версия|4.6.1|
|Тип|Изменение целевой платформы|

