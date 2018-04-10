### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant или Contract.Requires<TException> не учитывает String.IsNullOrEmpty как чистая

|   |   |
|---|---|
|Подробные сведения|Для приложений, ориентированных на .NET Framework 4.6.1, в том случае, если инвариантный контракт для <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> или контракт предусловия для <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> вызовы <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> метода, метод переопределения выдает предупреждение CC1036: &quot;обнаружен вызов метода " System.String.IsNullOrWhteSpace(System.String) "без [чистый] в методе.&quot; Это предупреждение, а не ошибку компилятора компилятора.|
|Предложение|Проблема была устранена в [билете 339 на сайте GitHub](https://github.com/Microsoft/CodeContracts/issues/339). Чтобы устранить это предупреждение, можно загрузить и скомпилировать обновленную версию исходного кода для средства контрактов для кода из [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md). Сведения о скачивании находятся в нижней части страницы.|
|Область|Дополнительный номер|
|Версия|4.6.1|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

