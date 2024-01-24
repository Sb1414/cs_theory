# Вопросы
+ [Общее](#общее)
+ [ООП](#ооп)
+ [Обработка исключений](#обработка-исключений)
+ [Типы данных и переменные](#типы-данных-и-переменные)
+ [Коллекции](#коллекции)
+ [Платформа .NET](#платформа-net)
+ [Потоки, ассинхронность](#потоки-ассинхронность)
+ [Алгоритмы](#алгоритмы)
+ [Базы данных](#базы-данных)
+ [Тестирование](#тестирование)
+ [Протоколы](#протоколы)

## Общее
+ [От какого класса неявно наследуются все классы в .NET ?](all.md#от-какого-класса-неявно-наследуются-все-классы-в-net-)
+ [Что такое System.Object ?](all.md#что-такое-systemobject-)
+ [Какие операции со строками вы знаете ?](all.md#какие-операции-со-строками-вы-знаете-)
+ [Что такое рекурсия ?](all.md#что-такое-рекурсия-)
+ [Что такое делегаты ?](all.md#что-такое-делегаты-)
+ [Что такое лямбда-выражение ?](all.md#что-такое-лямбда-выражение-)
+ [Что такое IIS](all.md#что-такое-iis)
+ [Что такое LINQ ?](all.md#что-такое-linq)
+ [Что такое отложенное и немедленное выполнение в LINQ ?](all.md#что-такое-отложенное-и-немедленное-выполнение-в-linq-)
+ [SOLID](all.md#solid)
+ [Что такое ref и out ?](all.md#что-такое-ref-и-out-)
+ [Что такое атрибут ?](all.md#что-такое-атрибут-)
+ [Что такое "as" и "is" ?](all.md#что-такое-as-и-is-)
+ [что такое чистая функция ? Какие у нее преимущества ?](all.md#что-такое-чистая-функция--какие-у-нее-преимущества-)
+ [контравариантные и ковариантные интерфесы](all.md#контравариантные-и-ковариантные-интерфесы)
+ [Что такое C# ?](all.md#что-такое-c-)
+ [В чем разница между public, static и void ?](all.md#в-чем-разница-между-public-static-и-void-)


## Память и компиляция
+ [Как устроена компиляция в .NET ?](memory.md#как-устроена-компиляция-в-net-)
+ [Разница между управляемым и неуправляемым кодом ?](memory.md#разница-между-управляемым-и-неуправляемым-кодом-)
+ [Что такое CLR ? Что такое IL ? Что такое CLS ?](memory.md#что-такое-clr--что-такое-il--что-такое-cls-)
+ [Что такое managed code ? управляемый код](memory.md#что-такое-managed-code-)
+ [Что такое Finalize ?](oop.md#что-такое-finalize-)
+ [В чем различие между Finalize и Dispose ?](memory.md#в-чем-различие-между-finalize-и-dispose-)
+ [unsafe, указатели](memory.md#unsafe-указатели-)
+ [Что такое сериализация ?](memory.md#что-такое-сериализация-)

## ООП
+ [Что такое ООП ?](oop.md#что-такое-ооп-)
+ [Назовите основные принципы ООП](oop.md#основные-принципы-ооп)
+ [Разница между классом и объектом](oop.md#разница-между-классом-и-объектом)
+ [Разрешено ли множественное наследование в c# ?](oop.md#разрешено-ли-множественное-наследование-в-c-)
+ [Какие модификаторы доступа есть в C# ?](oop.md#какие-модификаторы-доступа-есть-в-c-)
+ [Поддерживает ли C# множественное наследование ?](oop.md#поддерживает-ли-c-множественное-наследование-)
+ [Как запретить наследование от класса ?](oop.md#как-запретить-наследование-от-класса-)
+ [В чем разница между интерфейсом и абстрактным классом в .NET ?](oop.md#в-чем-разница-между-интерфейсом-и-абстрактным-классом-в-net-)
+ [Что такое виртуальный метод ?](oop.md#что-такое-виртуальный-метод-)
+ [конструкторы](oop.md#конструкторы)
+ [Можем ли мы использовать команду «this» в статическом методе ?](oop.md#можем-ли-мы-использовать-команду-this-в-статическом-методе-)
+ [Чем перекрытый метод отличается от перегруженного метода ?](oop.md#чем-перекрытый-метод-отличается-от-перегруженного-метода-)
+ [partial class Частичные классы и методы](oop.md#partial-class-частичные-классы-и-методы-)

## Обработка исключений
+ [Что такое Exception ?](exception.md#что-такое-exception-)
+ [Типы исключений](exception.md#типы-исключений)
+ [Для чего служат try, catch, finally?](exception.md#для-чего-служат-try-catch-finally-)
+ [Что такое call stack ?](exception.md#что-такое-call-stack-)
+ [В чём разница между throw и throw ex ?](exception.md#в-чём-разница-между-throw-и-throw-ex-)

## Типы данных и переменные
+ [Типы данных](types.md#типы-данных)
+ [Разница между readonly и const полями](types.md#разница-между-readonly-и-const-полями)
+ [Какие примитивные типы знаете ?](types.md#какие-примитивные-типы-знаете-)
+ [Что такое Nullable-тип ?](types.md#что-такое-nullable-тип-)
+ [Что такое тип значения, а что такое тип ссылки?](types.md#что-такое-тип-значения-а-что-такое-тип-ссылки-)
+ [Что из этого class, а что struct ? В каком участке памяти они хранятся ?](types.md#что-из-этого-class-а-что-struct--в-каком-участке-памяти-они-хранятся-)
+ [Чем отличаются value от reference type ? String - это reference или value ?](types.md#чем-отличаются-value-от-reference-type--string---это-reference-или-value-)
+ [Куча это](types.md#куча-это)
+ [В чем отличие между string builder и string ?](types.md#в-чем-отличие-между-string-builder-и-string-)
+ [Что такое дженерики generics ? Какие проблемы они решают ?](types.md#что-такое-дженерики--какие-проблемы-они-решают-)
+ [Что такое boxing / unboxing ?](types.md#что-такое-boxing--unboxing-)
+ [Что такое сборка мусора ?](types.md#что-такое-сборка-мусора-)
+ [Какие типы можно использовать в предложении foreach ?](types.md#какие-типы-можно-использовать-в-предложении-foreach-)
+ [В чем различие между классом и структурой ?](types.md#в-чем-различие-между-классом-и-структурой-)
+ [Что означает модификатор virtual ?](types.md#что-означает-модификатор-virtual-)
+ [Может ли класс реализовать два интерфейса, у которых объявлены одинаковые методы ? Каким образом ?](types.md#может-ли-класс-реализовать-два-интерфейса-у-которых-объявлены-одинаковые-методы--каким-образом-)
+ [Рефлексия (Reflection)](types.md#рефлексия-reflection-)


## Коллекции
+ [Какие знаете коллекции ? ](collections.md#какие-знаете-коллекции-)
+ [Что такое generics дженерики ?](collections.md#что-такое-generics-)
+ [Что такое GetHashCode ?](collections.md#что-такое-gethashcode-)
+ [Что такое Array, List, HashSet, Dictionary ? Приведите примеры использования этих структур данных. Какая сложность операций с ними (поиск, вставка, удаление) ?](collections.md#что-такое-array-list-hashset-dictionary--приведите-примеры-использования-этих-структур-данных-какая-сложность-операций-с-ними-поиск-вставка-удаление-)
+ [Разница между System.Array.CopyTo() и System.Array.Clone() ?](collections.md#разница-между-systemarraycopyto-и-systemarrayclone-)
+ [Что делает оператор yield ? ](collections.md#что-делает-оператор-yield-)
+ [Как работает Dictionary, почему он работает быстрее чем List ?](collections.md#как-работает-dictionary-почему-он-работает-быстрее-чем-list-)

## Платформа .NET
+ [Что такое ASP.NET ?](net.md#что-такое-aspnet-)
+ [Какие существуют типы Action filters ? и что это такое](net.md#какие-существуют-типы-action-filters--и-что-это-такое)
+ [Что такое Web Service ?](net.md#что-такое-web-service-)
+ [Отличается ли Delegate от Action ?](net.md#отличается-ли-delegate-от-action-)
+ [Что такое пространство имен (namespace) и зачем это нужно ?](net.md#что-такое-пространство-имен-namespace-и-зачем-это-нужно-)
+ [Что такое managed и unmanaged resources в .NET ?](net.md#что-такое-managed-и-unmanaged-resources-в-net-)

## Потоки, ассинхронность
+ [ Что такое параллельное программирование (многопоточность) и его назначение ? Какие классы используются ?](asynchrony.md#что-такое-параллельное-программирование-многопоточность-и-его-назначение--какие-классы-используются-)
+ [Что такое асинхронность и чем она отличается от многопоточности ?](asynchrony.md#что-такое-асинхронность-и-чем-она-отличается-от-многопоточности-)
+ [Что означают ключевые слова async / await ?](asynchrony.md#что-означают-ключевые-слова-async--await-)

## Алгоритмы
+ [Быстрая сортировка](algorithms.md#быстрая-сортировка)
+ [Сортировка вставками](algorithms.md#сортировка-вставками)
+ [Волновой метод](algorithms.md#волновой-метод)
+ [Линейный поиск](algorithms.md#линейный-поиск)
+ [Бинарный поиск](algorithms.md#бинарный-поиск)

## Базы данных
+ [Транзакция и ACID](db.md#транзакция-и-acid)
+ [Индексы](db.md#индексы)
+ [Недостатки и отличия различных типов объединений (join)](db.md#недостатки-и-отличия-различных-типов-объединений-join)
+ [Как подключиться к базе данных в С# ?](db.md#как-подключиться-к-базе-данных-в-с-)

## Тестирование
+ [Для чего нужны unit-тесты?](tests.md#для-чего-нужны-unit-тесты)
+ [Какие преимущества и недостатки использования unit-тестов?](tests.md#какие-преимущества-и-недостатки-использования-unit-тестов)
+ [Из каких трех логических блоков состоит unit-тест?](tests.md#какие-преимущества-и-недостатки-использования-unit-тестов)
+ [Что такое модульное тестирование и как его провести в C# ?](tests.md#что-такое-модульное-тестирование-и-как-его-провести-в-c-)

## Протоколы
+ [Что такое порт ?](protocols.md#что-такое-порт-)
+ [Что такое HTTP ?](protocols.md#что-такое-http-)
+ [HttpClient](protocols.md#httpclient)
+ [Что такое HTTPS](protocols.md#что-такое-https-)
+ [ Что такое HTML ?](protocols.md#что-такое-html-)
+ [Что такое FTP ?](protocols.md#что-такое-ftp-)
+ [Что такое SMTP ?](protocols.md#что-такое-smtp-)
+ [Что такое IMAP ?](protocols.md#что-такое-imap-)
+ [Что такое POP3 ?](protocols.md#что-такое-pop3-)
+ [Что такое javascript ?](protocols.md#что-такое-javascript-)
+ [Чем отличается метод POST от метода PUT?](protocols.md#чем-отличается-метод-post-от-метода-put-)
+ [Чем отличается метод GET от метода POST ?](protocols.md#чем-отличается-метод-get-от-метода-post-)
+ [Какие группы статус кодов вы знаете ?](protocols.md#какие-группы-статус-кодов-вы-знаете-)
+ [В каком формате передаются данные в теле запроса ?](protocols.md#в-каком-формате-передаются-данные-в-теле-запроса-)
+ [Про JSON](protocols.md#про-json)
+ [Про REST](protocols.md#про-rest)
+ [Как тестировать API ?](protocols.md#как-тестировать-api-)
+ [Какие вкладки в инструментах разработчика вы знаете ?](protocols.md#какие-вкладки-в-инструментах-разработчика-вы-знаете-)
+ [Уровни оси](protocols.md#уровни-оси)
+ [Вы набираете google.com в браузере . Расскажите как можно подробнее, что происходит в это время на HTTP-уровне ?](protocols.md#вы-набираете-googlecom-в-браузере--расскажите-как-можно-подробнее-что-происходит-в-это-время-на-http-уровне-)