### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridViews, тогда свойство AllowCustomPaging установлено в true может инициировать событие PageIndexChanging при выходе из последней странице представления

|   |   |
|---|---|
|Подробные сведения|Вызывает ошибку в .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> иногда не срабатывание для <xref:System.Web.UI.WebControls.GridView?displayProperty=name>s, которые включены <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Предложение|Эта проблема была устранена в платформе .NET Framework 4.6 и можно обращаться путем обновления для этой версии платформы .NET Framework. Как обхода, приложение можно сделать явную BindGrid для какого-либо <code>Page_Load</code> , мог попасть этих условий ( <xref:System.Web.UI.WebControls.GridView?displayProperty=name> — на последней странице и Дата последнего<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> отличается от <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). Кроме того приложение может изменяться для постраничный просмотр (вместо пользовательское разбиение по страницам), как в этом сценарии не показывают проблемы.|
|Область|Дополнительный номер|
|Версия|4.5|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

