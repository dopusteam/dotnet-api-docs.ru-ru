С помощью символьных индексирование с <xref:System.Text.StringBuilder.Chars%2A> свойство может быть резко снизит скорость обработки при следующих условиях:

- <xref:System.Text.StringBuilder> Экземпляр велико (например, он состоит из нескольких десятков тысяч символов).
- <xref:System.Text.StringBuilder> — «Фрагментированных». То есть, таких как повторные вызовы методов <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> которых автоматически увеличен объекта <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> свойства и выделенный новые блоки памяти, к нему.

Поскольку каждый символ доступа проходит весь связанный список блоков данных, чтобы найти правильные буфера индекса в серьезно влияет на производительность.

> [!NOTE]
>  Даже для большого «фрагментированных» <xref:System.Text.StringBuilder> объекту с помощью <xref:System.Text.StringBuilder.Chars%2A> свойство для доступа на основе индекса для одного или небольшое число символов может повлиять на производительность незначительно; как правило, это **0(n)** операции. Значительно снижает производительность происходит во время итерации символов в <xref:System.Text.StringBuilder> объекта, имеющего **O(n^2)** операции. 

Если возникли проблемы с производительностью при использовании символьного индексирование с <xref:System.Text.StringBuilder> объектов, которые можно использовать любой из следующих действий:

- Преобразовать <xref:System.Text.StringBuilder> экземпляр <xref:System.String> путем вызова <xref:System.Text.StringBuilder.ToString%2A> метод, затем получить доступ к символов в строке.

- Скопируйте содержимое существующего <xref:System.Text.StringBuilder> новый выделенный размер <xref:System.Text.StringBuilder> объекта. Повышает производительность, так как новый <xref:System.Text.StringBuilder> объект не фрагментированных. Пример:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Установить начальную вместимость из <xref:System.Text.StringBuilder> в значение, равное примерно до ожидаемого размера путем вызова <xref:System.Text.StringBuilder.%23ctor(System.Int32)> конструктор. Обратите внимание, что это выделяет весь блок памяти, даже если <xref:System.Text.StringBuilder> редко достигает своего максимального размера.
