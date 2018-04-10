### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load не удаляет символ свойства

|   |   |
|---|---|
|Подробные сведения|При разработке для .NET Framework 4.5 в конструкторе рабочих процессов и загрузке повторного размещения рабочего процесса версии 3.5 с <xref:System.Activities.Presentation.WorkflowDesigner.Load> метода <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> возникает при сохранении рабочего процесса.|
|Предложение|Эта ошибка манифесты только при разработке для .NET Framework 4.5 в конструкторе рабочих процессов, поэтому ее можно обойти, установив <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> для версии 4.0 Framework.Alternatively .NET, проблему можно избежать с помощью <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> метод для загрузки рабочего процесса вместо <xref:System.Activities.Presentation.WorkflowDesigner.Load>.|
|Область|Значительно|
|Версия|4.5|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

