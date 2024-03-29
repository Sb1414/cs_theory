[Вопросы](README.md)

# Платформа .NET
+ [Что такое ASP.NET ?](#что-такое-aspnet-)
+ [Какие существуют типы Action filters ? и что это такое](#какие-существуют-типы-action-filters--и-что-это-такое)
+ [Что такое Web Service ?](#что-такое-web-service-)
+ [Отличается ли Delegate от Action ?](#отличается-ли-delegate-от-action-)
+ [Что такое пространство имен (namespace) и зачем это нужно ?](#что-такое-пространство-имен-namespace-и-зачем-это-нужно-)
+ [Что такое managed и unmanaged resources в .NET ?](#что-такое-managed-и-unmanaged-resources-в-net-)

## Что такое ASP.NET ?
**ASP.NET** (Active Server Pages .NET) - это открытая серверная веб-платформа, разработанная корпорацией Microsoft для создания динамических веб-приложений и веб-сервисов. ASP.NET является частью .NET Framework и предоставляет средства для создания мощных и масштабируемых веб-приложений с использованием различных технологий.

Основные компоненты и возможности ASP.NET включают:
- ASP.NET Web Forms: Модель программирования, ориентированная на события, которая упрощает создание веб-приложений с использованием элементов управления, подобных тем, которые используются в Windows Forms.
- ASP.NET MVC (Model-View-Controller): Архитектурный шаблон, предоставляющий разделение приложения на модель (данные), представление (отображение) и контроллер (логика). Это предоставляет более гибкую архитектуру для веб-приложений.
- ASP.NET Web API: Фреймворк для создания и обслуживания HTTP-служб, использующих стандарты веба, такие как REST.
- ASP.NET Core: Версия ASP.NET, оптимизированная для кроссплатформенной разработки и более высокой производительности. ASP.NET Core также предоставляет поддержку для облака и контейнеров.

## Какие существуют типы Action filters ? и что это такое
Action Filter в ASP.NET MVC и ASP.NET Core представляет собой специальный тип фильтра, который позволяет встраиваться в жизненный цикл обработки запросов и ответов веб-приложения. Action Filter предоставляет возможность выполнить дополнительную логику до или после выполнения действия контроллера или результата.

## Что такое Web Service ?
**Web-сервис** (Web Service) - это программное обеспечение, предоставляющее функциональность для обмена данными и выполнения операций через интернет. Web-сервисы используют стандартные протоколы и форматы данных для обеспечения взаимодействия между различными программными системами, независимо от их языка программирования и платформы.

## Отличается ли Delegate от Action ?
Да, Delegate и Action представляют различные концепции в C#, хотя оба могут использоваться для передачи и вызова методов.

1. **Delegate**:
- это тип данных, который представляет собой ссылку на метод с определенной сигнатурой (типом возвращаемого значения и параметрами). Он может использоваться для создания переменной, которая может содержать ссылку на метод и вызывать этот метод.
    ```
    delegate void MyDelegate(string message);

    void DisplayMessage(string message)
    {
        Console.WriteLine(message);
    }

    MyDelegate myDelegate = new MyDelegate(DisplayMessage);
    myDelegate("Hello, Delegate!");
    ```
2. **Action**:
- это обобщенный делегат, предоставленный в стандартной библиотеке C#. Он представляет собой делегат без возвращаемого значения (аналогично delegate void), но с возможностью принимать от 0 до 16 параметров.
    ```
    Action<string> myAction = DisplayMessage;
    myAction("Hello, Action!");
    ```
*Преимущества использования Action:*
- Он более короткий и не требует явного определения собственного типа делегата.
- Поддерживает обобщенные типы параметров.

Использование между **Delegate** и **Action** будет зависеть от требований проекта. В большинстве случаев Action предпочтительнее из-за его краткости и удобства.

## Что такое пространство имен (namespace) и зачем это нужно ?
**Пространство имен (namespace)** - механизм для группировки и организации классов, интерфейсов, делегатов и других типов данных *в логически связанные блоки*. Пространства имен предназначены для избежания конфликтов имен между различными частями кода и обеспечивают структурирование кода для повышения читаемости, управляемости и возможности повторного использования.

Основные принципы пространств имен:
1. Изоляция имен: изоляция имен типов, переменных и других элементов в коде. Это предотвращает конфликты имен, когда различные части кода могут использовать одинаковые имена, не пересекаясь между собой.
2. Организация кода: организация кода, делая его более структурированным и понятным. Это улучшает читаемость кода и облегчает его поддержку.
3. Повторное использование кода: группировка и организация кода, который предназначен для повторного использования. При создании библиотек или фреймворков разработчики могут поместить их в специальные пространства имен, что делает более легким их интегрирование в проекты.
4. Управление зависимостями между различными частями программы. Используя пространства имен, можно контролировать, какие части кода имеют доступ к другим частям.

## Что такое managed и unmanaged resources в .NET ?
- Managed ресурсы – это ресурсы для очистки которых используется Garbage collector.
- Unmanaged ресурсы – ресурсы которые не очищаются сборщиком мусора и их нужно явно очищать после выполнения кода, который их использовал, например: работа с файлом, работа с бд и тд.

Использование IDisposable  и конструкции using для очистки unmanaged ресурсов, как основной подход для работы с такими ресурсами.
