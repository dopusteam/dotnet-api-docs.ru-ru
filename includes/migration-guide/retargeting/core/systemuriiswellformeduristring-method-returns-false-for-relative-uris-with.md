### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>Метод System.Uri.IsWellFormedUriString возвращает значение false для относительных URI с char двоеточия в первом сегменте

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.5 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> будет рассматривать относительные URI с <code>:</code> в их первый сегмент как некорректное. Это отличается от <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> поведения в .NET Framework 4.0, которые были выполнены для обеспечения соответствия для RFC3986.|
|Предложение|(Как и другие изменения URI) это изменение влияет только приложений, предназначенных для .NET Framework 4.5 (или более поздней версии). Чтобы продолжить использовать старое поведение, целевые приложения для .NET Framework 4.0. Кроме того, проверки URI до вызова метода <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> поиск <code>:</code> символов, которые может потребоваться удаление в целях проверки, если желательно старое поведение.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

