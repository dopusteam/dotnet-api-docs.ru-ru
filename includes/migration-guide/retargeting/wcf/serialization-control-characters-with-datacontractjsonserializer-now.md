### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>Сериализация управляющие символы с помощью DataContractJsonSerializer теперь совместима с версии ECMAScript 6 и V8

|   |   |
|---|---|
|Подробные сведения|В .NET framework 4.6.2 и более ранних версиях <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> не удалось сериализовать некоторые специальные управляющие символы, например \b "," \f "и" \t, в результате которого совместимо со стандартом ECMAScript версии 6 и V8. Начиная с .NET Framework 4.7 сериализации из этих символов управления совместим с версии ECMAScript 6 и V8.|
|Предложение|Для приложений, предназначенных для .NET Framework 4.7 Эта функция включена по умолчанию. Если оно нежелательно, данную функцию можно отключить, добавив следующую строку в раздел <code>&lt;runtime&gt;</code> файла app.config или web.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.7|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

