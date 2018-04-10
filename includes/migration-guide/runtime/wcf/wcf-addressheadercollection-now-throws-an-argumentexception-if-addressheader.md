### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection теперь создает ArgumentException, если элемент addressHeader имеет значение null

|   |   |
|---|---|
|Подробные сведения|Начиная с .NET Framework 4.7.1, <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> вызывает конструктор <xref:System.ArgumentException> Если один из элементов <code>null</code>. В .NET Framework 4.7 и более ранних версий исключение не возникает.|
|Предложение|При возникновении проблем совместимости с этим изменением на платформу .NET Framework 4.7.1 или более поздней версии, вы можно отказаться от ее, добавив следующую строку, чтобы <code>&lt;runtime&gt;</code> раздел файла app.config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Область|Дополнительный номер|
|Версия|4.7.1|
|Тип|Среда выполнения|
|Затронутые API|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

