### <a name="winforms-checkforoverflowunderflow-property-is-now-true-for-systemdrawing"></a>Свойство CheckForOverflowUnderflow WinForm больше не относится к System.Drawing

|   |   |
|---|---|
|Подробные сведения|CheckForOverflowUnderflow для сборки System.Drawing.dll свойству значение true.|
|Предложение|Раньше при переполнениях результат усекался без уведомления. Теперь создается исключение <xref:System.OverflowException?displayProperty=name>,|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|

