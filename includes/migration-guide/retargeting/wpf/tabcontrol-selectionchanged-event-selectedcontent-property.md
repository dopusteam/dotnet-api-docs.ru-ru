### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>Элемент управления TabControl SelectionChanged события и свойства SelectedContent

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.7.1, <xref:System.Windows.Controls.TabControl> обновляет значение его <xref:System.Windows.Controls.TabControl.SelectedContent> свойство перед порождением <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> событие при изменении его выбора. В .NET Framework 4.7 и более ранних версий обновление SelectedContent произошло после события.|
|Предложение|Приложений, ориентированных на .NET Framework 4.7.1 или более поздней версии можно отключить это изменение и использование устаревшее поведение, добавив следующую команду, чтобы <code>&lt;runtime&gt;</code> раздел файла конфигурации приложения:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Приложений, предназначенных для .NET Framework 4.7 или более ранних но выполняются на платформе .NET Framework 4.7.1 или более поздней версии можно включить новое поведение, добавив следующую строку, чтобы <code>&lt;runtime&gt;</code> раздел файла .configuration приложения:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.7.1|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

