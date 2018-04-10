### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Вызов CreateDefaultAuthorizationContext с аргументом null был изменен

|   |   |
|---|---|
|Подробные сведения|Реализация <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> возвращается путем вызова <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> с null authorizationPolicies аргумент изменена в .NET Framework 4.6.|
|Предложение|В редких случаях в приложениях WCF, которые используют настраиваемую проверку подлинности, могут возникать различия в поведении. В таких случаях прежнее поведение можно восстановить двумя способами.<ol><li>Перекомпилируйте приложение для ориентации на версию .NET Framework, предшествующую 4.6. Для служб, размещенных в IIS, используйте &lt;httpRuntime targetFramework =&quot;x.x&quot;  / &gt; элемент на более раннюю версию платформы .NET Framework.</li><li>Добавьте следующую строку в раздел <code>&lt;appSettings&gt;</code> файла app.config: <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code>.</li></ol>|
|Область|Дополнительный номер|
|Версия|4.6|
|Тип|Изменение целевой платформы|
|Затронутые API|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

