### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Неправильная реализация MemberDescriptor.Equals

|   |   |
|---|---|
|Подробные сведения|Исходной реализации &quot;равняется&quot; метод сравнения двух свойств другую строку из объектов в группе сравнения: имя категории, чтобы строка описания. Исправление заключается в сравнении &quot;категории&quot; первого объекта &quot;категории&quot; второго и &quot;описание&quot; для &quot;описание&quot;. Значение конфигурации MemberDescriptorEqualsReturnsFalseIfEquivalent можно задать значение true, чтобы отказаться от нового поведения при нацеливании 4.6.2, или значение false, чтобы включить это исправление, если назначение целевой версии framework меньше 4.6.2.|
|Предложение|Если приложение зависит от MemberDescriptor.Equals иногда возвращение значения false при дескрипторы эквивалентны, и для различных версий 4.6.2 версии платформы .NET Framework, существует несколько вариантов:<ol><li>Изменения в коде для сравнения &quot;категории&quot; и &quot;описание&quot; поля вручную наряду с выполнением метода Equals.</li><li>Отказаться от этого изменения, добавив следующий параметр в файл app.config:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Если ваш предназначено приложение 4.6.1 или более ранняя версия .NET Framework и это изменение включена, можно задать параметр совместимости false, добавив следующий параметр в файл app.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.6.2|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

