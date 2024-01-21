[Вопросы](README.md)

# Потоки, ассинхронность

+ [Что такое параллельное программирование (многопоточность) и его назначение ? Какие классы используются ?](#что-такое-параллельное-программирование-многопоточность-и-его-назначение--какие-классы-используются-)
+ [Что такое асинхронность и чем она отличается от многопоточности ?](#что-такое-асинхронность-и-чем-она-отличается-от-многопоточности-)
+ [Что означают ключевые слова async / await ?](#что-означают-ключевые-слова-async--await-)

## Что такое параллельное программирование (многопоточность) и его назначение ? Какие классы используются ?
Во фреймворк .NET была добавлена библиотека параллельных задач TPL (Task Parallel Library), основной функционал которой располагается в пространстве имен **System.Threading.Tasks**. Данная библиотека упрощает работу с многопроцессорными, многоядерными системами. Кроме того, она упрощает работу по созданию новых потоков. Поэтому обычно рекомендуется использовать именно TPL и ее классы для создания многопоточных приложений, хотя стандартные средства и класс Thread по-прежнему находят широкое применение.

В библиотеке классов .NET задача представлена специальным классом - классом **Task**, который находится в пространстве имен **System.Threading.Tasks**. Данный класс описывает отдельную задачу, которая запускается асинхронно в одном из потоков из пула потоков. Хотя ее также можно запускать синхронно в текущем потоке.

Для определения и запуска задачи можно использовать различные способы.

- Первый способ создание объекта Task и вызов у него метода Start:
```
Task task = new Task(() => Console.WriteLine("Hello Task!"));
task.Start();
```
В качестве параметра объект Task принимает делегат Action, то есть мы можем передать любое действие, которое соответствует данному делегату, например, лямбда-выражение, как в данном случае, или ссылку на какой-либо метод. То есть в данном случае при выполнении задачи на консоль будет выводиться строка "Hello Task!".

А метод Start() собственно запускает задачу.

- Второй способ заключается в использовании статического метода **Task.Factory.StartNew()**. Этот метод также в качестве параметра принимает делегат Action, который указывает, какое действие будет выполняться. При этом этот метод сразу же запускает задачу:
```
Task task = Task.Factory.StartNew(() => Console.WriteLine("Hello Task!"));
```
В качестве результата метод возвращает запущенную задачу.

- Третий способ определения и запуска задач представляет использование статического метода **Task.Run()**:
```
Task task = Task.Run(() => Console.WriteLine("Hello Task!"));
```
Метод Task.Run() также в качестве параметра может принимать делегат Action - выполняемое действие и возвращает объект Task.


## Что такое асинхронность и чем она отличается от многопоточности ?
**Асинхронность** - способность выполнять задачи независимо друг от друга, не блокируя основной поток выполнения. В C#, асинхронные операции обычно реализуются с использованием ключевых слов *async* и *await*. Асинхронные методы позволяют освободить основной поток выполнения, в то время как определенные части кода выполняются асинхронно.

> Преимущества: улучшение отзывчивости приложения, эффективное использование ресурсов и возможность обработки большого числа запросов одновременно, не блокируя потоки.

**Многопоточность** - выполнение нескольких потоков в одном процессе. Каждый поток выполняется независимо друг от друга, и многопоточные приложения могут выполнять несколько задач параллельно. Используются классы из пространства имен System.Threading или, начиная с .NET Framework 4.0, System.Threading.Tasks.

> Преимущества: повышение параллелизма, улучшение производительности, и возможность эффективного использования многозадачности на многоядерных системах.

**Отличия между асинхронностью и многопоточностью в C#:**
1. Способ использования ресурсов: Асинхронность использует неблокирующий подход, который позволяет использовать ресурсы более эффективно, не блокируя потоки. В случае многопоточности, потоки часто блокируются, что может привести к проблемам с производительностью.

2. Синтаксис: Асинхронность в C# обычно реализуется с использованием ключевых слов async и await, что делает код более читаемым и удобным для понимания. Многопоточные приложения требуют явного управления потоками с использованием Thread или Task.

3. Сложность программирования: Асинхронность может быть более удобной для программирования в некоторых случаях, таких как обработка асинхронных событий, ввод-вывод и сетевые операции. Многопоточность может быть сложнее для управления, особенно в случае синхронизации и предотвращения состояния гонки.

4. Цель использования: Асинхронность обычно используется для обработки ввода-вывода и сетевых операций, в то время как многопоточность подходит для выполнения вычислительно сложных задач параллельно.

Оба подхода имеют свои места и сценарии использования, и выбор между асинхронностью и многопоточностью зависит от конкретных требований вашего приложения.

## Что означают ключевые слова async / await ?
1. **async** (Асинхронность):
- Описание: Ключевое слово async используется для определения асинхронных методов. Метод, помеченный async, может содержать операторы await и выполняться асинхронно.
- Пример:
    ```
    async Task<string> MyAsyncMethod()
    {
        // Асинхронные операции могут содержаться здесь
        return "Completed";
    }
    ```
2. **await** (Ожидание):
- Описание: Ключевое слово await используется внутри асинхронных методов для ожидания завершения асинхронных операций. Оно позволяет программе продолжать выполнение других задач, не блокируя поток выполнения.
- Пример:
```
async Task<string> MyAsyncMethod()
{
    // Асинхронная операция с использованием await
    string result = await SomeAsyncOperation();
    return result;
}
```
Когда метод, помеченный *async*, вызывает метод с *await*, выполнение метода приостанавливается до завершения асинхронной операции. В это время основной поток выполняет другие задачи. Когда асинхронная операция завершается, выполнение метода с *async* продолжается, и результат асинхронной операции возвращается.

Преимущества использования *async* / *await* включают более читаемый и лаконичный код при работе с асинхронными операциями, удобство отладки и обработку ошибок. Они обеспечивают удобный способ написания асинхронного кода без явного использования многопоточных конструкций.