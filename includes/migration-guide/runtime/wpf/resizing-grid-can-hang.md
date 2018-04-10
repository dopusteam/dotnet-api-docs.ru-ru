### <a name="resizing-a-grid-can-hang"></a>Изменение размеров в сетке может зависнуть

|   |   |
|---|---|
|Подробные сведения|Бесконечный цикл может возникнуть во время макет <code>T:System.Windows.Controls.Grid</code> при следующих обстоятельствах:<ul><li>Определения строк содержат два *-строки, оба объявления MinHeight и MaxHeight.</li><li>Содержимое *-строки не превышает соответствующий MaxHeight</li><li>Доступной высоте сетки являются более поздними первый MinHeight (и любых других основных или Auto строк)</li><li>Приложение, предназначенное для .net 4.7, или будет означать согласие на алгоритм выделения 4,7, задав <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>Цикл также может произойти с более двух строк или в случае аналогом для столбцов. Проблема устранена в .net 4.7.1.|
|Предложение|Обновление до .net 4.7.1.  Кроме того Если вам не требуется алгоритм 4,7 выделения можно использовать следующий параметр конфигурации:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Область|Пограничный случай|
|Версия|4.7|
|Тип|Среда выполнения|

