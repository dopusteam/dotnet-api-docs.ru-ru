### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>Не может отобразить HtmlTextWriter `<br/>` элемент неправильно

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.6, при вызове <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> и <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> с элементом <code>&lt;BR /&gt;</code> правильно вставляется только один <code>&lt;BR /&gt;</code> (вместо двух).|
|Предложение|Если приложение зависит от дополнительного тега <code>&lt;BR /&gt;</code>, <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> следует вызвать второй раз. Обратите внимание, что это изменение в поведении влияет только на приложениях, предназначенных для .NET Framework 4.6 или более поздней версии, поэтому другой вариант — предназначенные для предыдущей версии платформы .NET Framework, чтобы получить старое поведение.|
|Область|Пограничный случай|
|Версия|4.6|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

