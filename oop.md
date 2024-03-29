[Вопросы](README.md)

# ООП

+ [Что такое _ООП_?](#что-такое-ооп-)
+ [Основные принципы ООП](#основные-принципы-ооп)
+ [Разница между классом и объектом](#разница-между-классом-и-объектом)
+ [Разрешено ли множественное наследование в c#?](#разрешено-ли-множественное-наследование-в-c-)
+ [Какие модификаторы доступа есть в C# ?](#какие-модификаторы-доступа-есть-в-c-)
+ [Поддерживает ли C# множественное наследование ?](#поддерживает-ли-c-множественное-наследование-)
+ [Как запретить наследование от класса ?](#как-запретить-наследование-от-класса-)
+ [В чем разница между интерфейсом и абстрактным классом в .NET ?](#в-чем-разница-между-интерфейсом-и-абстрактным-классом-в-net-)
+ [Что такое виртуальный метод ?](#что-такое-виртуальный-метод-)
+ [конструкторы](#конструкторы)
+ [Можем ли мы использовать команду «this» в статическом методе ?](#можем-ли-мы-использовать-команду-this-в-статическом-методе-)
+ [partial class Частичные классы и методы](#partial-class-частичные-классы-и-методы)

## Что такое ООП ?
__Объектно-ориентированное программирование (ООП)__ — методология программирования, основанная на представлении программы в виде совокупности объектов, каждый из которых является экземпляром определенного класса, а классы образуют иерархию наследования. 

+ объектно-ориентированное программирование использует в качестве основных логических конструктивных элементов объекты, а не алгоритмы;
+ каждый объект является экземпляром определенного класса 
+ классы образуют иерархии. 

Программа считается объектно-ориентированной, только если выполнены все три указанных требования. В частности, программирование, не использующее наследование, называется не объектно-ориентированным, а программированием с помощью абстрактных типов данных.

Согласно парадигме ООП программа состоит из объектов, обменивающихся сообщениями. Объекты могут обладать состоянием, единственный способ изменить состояние объекта - послать ему сообщение, в ответ на которое, объект может изменить собственное состояние. 

## Основные принципы ООП
C# — это объектно-ориентированный язык программирования. Четыре основных принципа объектно-ориентированного программирования следующие.

+ Инкапсуляция. Скрытие внутреннего состояния и функций объекта и предоставление доступа только через открытый набор функций. Инкапсуляция в программировании является объединением данных и кода, работающего с этими данными, в большинстве случае это сводится к тому, чтобы не давать доступа к важным данным напрямую.

+ Наследование. Возможность создания новых абстракций на основе существующих. Пример: Игры и дополнения, Версии смартфона

+ Полиморфизм. Возможность реализации наследуемых свойств или методов отличающимися способами в рамках множества абстракций. Полиморфизм немного напоминает универсальный пульт дистанционного управления, который может адаптироваться для управления различными устройствами. В программировании это означает, что один интерфейс может использоваться для управления разными методами, давая разные результаты в зависимости от контекста. Пример: Музыкальный плеер (может воспроизводить разные аудиоформаты, такие как mp3, wav и flac. Для каждого формата требуется свой метод воспроизведения, однако, вместо создания методов Play, PlayMp3, PlayWav, PlayFlac, правильнее будет использовать общий метод Play)
```
public class MusicPlayer
{
    public virtual void Play()
    {
        Console.WriteLine("Воспроизводим аудио в стандартном формате...");
    }
}

public class Mp3Player : MusicPlayer
{
    public override void Play()
    {
        Console.WriteLine("Воспроизводим mp3...");
    }
}

public class WavPlayer : MusicPlayer
{
    public override void Play()
    {
        Console.WriteLine("Воспроизводим wav...");
    }
}

public class FlacPlayer : MusicPlayer
{
    public override void Play()
    {
        Console.WriteLine("Воспроизводим flac...");
    }
}
```


+ Абстракция. Набор общих характеристик. Абстракция похожа на использование умного устройства, не зная его сложной схемы. Например, чтобы переключить канал на телевизоре, мы просто нажимаем на кнопку на пульте, как кодируется пультом нажатие на кнопку, передается на телевизор и декодируется нам не важно. Важно чтобы канал переключился, а не тонкости радиотехники. Вот и в программировании абстракция означает предоставление основных функций без погружения в детали.
Пример: Погода (чтобы узнать прогноз погоды мы просто открываем приложение на телефоне и оно показывает нам погоду. Как оно собирает для этого данные, как их обрабатывает, все это скрыто от нас.)
```
public abstract class WeatherApp
{
    public void DisplayForecast()
    {
        Console.WriteLine("Показываем текущий прогноз погоды...");
    }

    // Абстрактный метод получения данных, различающийся для текущего способа связи
    public abstract void GetWeatherData();
}

public class WifiWeatherApp : WeatherApp
{
    public override void GetWeatherData()
    {
        Console.WriteLine("Запрашиваем данные по WiFi...");
    }
}

public class MobileWeatherApp : WeatherApp
{
    public override void GetWeatherData()
    {
        Console.WriteLine("Запрашиваем данные по мобильной сети...");
    }
}
```

## Разница между классом и объектом
**Класс** – это определение объекта, а **объект** – это экземпляр класса.

класс он описывает все свойства, методы, состояния и поведение, которыми будет обладать реализующий объект. 

На основе одного класса может существовать несколько экземпляров объектов, каждый из которых обладает различными свойствами.


## [Какие модификаторы доступа есть в C# ?](https://dev-station.ru/categories/csharp/cheatsheet/csharp-base-cheatsheet#3399)
Все типы и члены типов имеют уровень доступности. Он определяет возможность их использования из другого кода в вашей или в других сборках. Сборка — это .dll или .exe, созданные путем компиляции одного или нескольких CS-файлов в одной компиляции. Следующие модификаторы доступа позволяют указать доступность типа или члена при объявлении:

- **public**: доступ к типу или члену возможен из любого другого кода в той же сборке или другой сборке, ссылающейся на него. Уровень доступности общедоступных элементов типа определяется уровнем доступности самого типа.

- **private**: доступ к типу или члену возможен только из кода в том же объекте class или struct.

- **protected**: доступ к типу или члену возможен только из кода в том же объекте class, либо в class, производном от этого class.

- **internal**: доступ к типу или члену возможен из любого кода в той же сборке, но не из другой сборки. Другими словами, internal доступ к типам или членам можно получить из кода, который является частью той же компиляции.

- **protected internal**: доступ к типу или члену возможен из любого кода в той сборке, где он был объявлен, или из производного class в другой сборке.

- **private protected**: доступ к типу или элементу возможен из типов, производных от объекта class и объявляемых в сборке, содержащей этот объект.

## [Поддерживает ли C# множественное наследование ?](https://dev-station.ru/categories/csharp/cheatsheet/csharp-base-cheatsheet#3398)
С# поддерживает множественное наследование в виде наследования от класса и нескольких интерфейсов, или просто от нескольких интерфейсов.

Но не поддерживает наследование от нескольких классов.

## [Как запретить наследование от класса ?](https://dev-station.ru/categories/csharp/cheatsheet/csharp-base-cheatsheet#3402)
Для этого служит ключевое слово *sealed*.

Еще чтобы разрешить наследование класса, но запретить перекрытие метода: указываем класс как public, а метод как sealed.

## Разрешено ли множественное наследование в c# ?
В C# не разрешено множественное наследование классов, то есть класс не может явно наследовать более одного класса. Это было решено для упрощения языка и уменьшения сложности внутренней реализации и поддержки. Однако C# поддерживает множественное наследование интерфейсов.

Множественное наследование интерфейсов позволяет классу реализовывать несколько интерфейсов, что предоставляет гибкость в определении функциональности. Таким образом, хотя множественное наследование классов не разрешено в C#, множественное наследование интерфейсов остается возможным.

пример множественного наследования интерфейсов в C#:
```
Message hello = new Message("Hello World");
hello.Print();  // Hello World
 
interface IMessage
{
    string Text { get; set; }
}
interface IPrintable
{
    void Print();
}
class Message : IMessage, IPrintable
{
    public string Text { get; set; }
    public Message(string text) => Text = text;
    public void Print()=> Console.WriteLine(Text);
}
```
В данном случае определены два интерфейса. Интерфейс IMessage определяет свойство Text, которое представляет текст сообщения. А интерфейс IPrintable определяет метод Print.

Класс Message реализует оба интерфейса и затем применяется в программе.

## [В чем разница между интерфейсом и абстрактным классом в .NET ?](https://dev-station.ru/categories/csharp/cheatsheet/csharp-base-cheatsheet#3384)
**Абстрактный класс** – это класс, содержащий один или несколько абстрактных методов. Нельзя создать объект данного класса, тк абстрактный метод, как правило, не имеет реализации. Ключевое слово `abstract`. Абстрактные классы обычно используются для определения базового класса в иерархии классов.

**Интерфейс** – это абстрактный ссылочный тип, который может содержать некоторое количество методов, свойств, событий и индексаторов. Начиная с версии C# 8.0 ещё и статические поля и константы. Так же, как и с абстрактным классом, нельзя создать объект данного типа, но мы можем объявить, например, сигнатуры нужных нам методов.

## [Что такое виртуальный метод ?](https://dev-station.ru/categories/csharp/cheatsheet/csharp-base-cheatsheet#3388)
При наследовании нередко возникает необходимость изменить в классе-наследнике функционал метода, который был унаследован от базового класса. В этом случае класс-наследник может переопределять методы и свойства базового класса.

Те методы и свойства, которые мы хотим сделать доступными для переопределения, в базовом классе помечаются модификатором virtual. Такие методы и свойства называют виртуальными.

А чтобы переопределить метод в классе-наследнике, этот метод определяется с модификатором override. Переопределенный метод в классе-наследнике должен иметь тот же набор параметров, что и виртуальный метод в базовом классе.

## partial class Частичные классы и методы
Классы могут быть частичными. То есть мы можем иметь несколько файлов с определением одного и того же класса, и при компиляции все эти определения будут скомпилированы в одно.

нужен чтобы разделить автоматически генерируемый код и код, который пишется руками.
