[Вопросы](README.md)

# Алгоритмы
+ [Быстрая сортировка](#быстрая-сортировка)
+ [Сортировка вставками](#сортировка-вставками)
+ [Волновой метод](#волновой-метод)
+ [Линейный поиск](#линейный-поиск)
+ [Бинарный поиск](#бинарный-поиск)

## Быстрая сортировка
Быстрая сортировка (Quicksort) — это эффективный алгоритм сортировки, который использует стратегию "разделяй и властвуй". Разработан Тони Хоаром в 1960 году. 

шаги алгоритма быстрой сортировки:
1. Выбор опорного элемента (Pivot):

    Этот элемент будет использоваться для разделения массива на две подгруппы - элементы, меньшие опорного, и элементы, большие опорного.

2. Разделение (Partitioning):

    Перераспределяем элементы массива так, чтобы элементы, меньшие опорного, находились слева от опорного, а элементы, большие опорного, находились справа. В это время опорный элемент занимает свое окончательное место в массиве. Этот процесс называется разделением.

3. Рекурсивная сортировка подмассивов:

    Рекурсивно применить алгоритм быстрой сортировки к двум подмассивам, одному слева от опорного элемента и другому справа от опорного элемента. Каждый из этих подмассивов будет сортироваться независимо.

4. Остановка рекурсии:

    Процесс рекурсии продолжается до тех пор, пока подмассивы не станут достаточно маленькими, чтобы быть отсортированными непосредственно. Когда размер подмассива становится равным 1 или 0, он считается отсортированным.

5. Объединение:

    Когда все подмассивы сортированы, алгоритм завершает свою работу, и массив считается отсортированным.

## Сортировка вставками
**Сортировка вставками** (Insertion Sort) - сортирует массив путем пошагового строительства отсортированной части массива. Он начинает с пустой (или почти пустой) отсортированной части массива и последовательно вставляет элементы из оставшейся части массива в отсортированную часть.

шаги алгоритма сортировки вставками:
1. Инициализация: 

    Первый элемент массива считается отсортированным. Начиная со второго элемента, алгоритм считает, что массив разделен на отсортированную и неотсортированную части.

2. Перебор элементов:

    Перебираем элементы из неотсортированной части массива, начиная со второго элемента.

3. Вставка:

    Каждый элемент вставляется в отсортированную часть массива на свое место. Элементы в отсортированной части, которые больше текущего элемента, сдвигаются вправо, чтобы освободить место для вставки.

4. Повторение:

    Шаги 2-3 повторяются до тех пор, пока не пройдены все элементы.

5. Завершение:

    После завершения процесса вставки, весь массив считается отсортированным.

## Волновой метод
**Волновой метод** (Wavefront Algorithm) - это алгоритм поиска кратчайшего пути в сетке (или лабиринте) от начальной точки к конечной.

*Описание алгоритма:*
1. Инициализация:

    Создайте сетку (массив) размером MxN, где каждая ячейка представляет собой точку в пространстве. Обозначьте начальную точку и конечную точку.

2. Установка точек:

    Установите начальную точку в сетке. Пометьте ее значением 0 (или другим обозначением). Это значение будет представлять "волну", которая распространяется по сетке.

3. Распространение волны:

    Начиная с начальной точки, распространяйте "волну" по сетке. Увеличивайте значения волновой "сети" на единицу при распространении волны.

4. Поиск пути:

    Начинайте с конечной точки и двигайтесь к начальной точке, выбирая соседнюю ячейку с меньшим значением волновой "сети". Этот путь будет кратчайшим, так как "волна" распространяется от начальной точки.

5. Повторение:

    Продолжайте распространение волны и поиск пути до тех пор, пока не достигнете начальной точки.

## Линейный поиск
Линейный поиск подходит для ***неотсортированных*** массивов. Этот метод проходит по массиву последовательно, начиная с первого элемента, и сравнивает искомый элемент с каждым элементом массива до тех пор, пока не найдет совпадение или не достигнет конца массива.

1. Задайте целевой элемент, который вы ищете.
2. Начните с первого элемента массива.
3. Последовательно сравнивайте каждый элемент с целевым.
4. Если элемент найден, верните его индекс.
5. Если дошли до конца массива и не нашли элемент, верните -1 (или другое значение, указывающее на отсутствие).

## Бинарный поиск
Бинарный поиск применяется к отсортированным массивам. Этот метод разделяет массив пополам и сравнивает целевой элемент с элементом в середине. Если элемент найден, поиск продолжается в половине, в которой он находится. Процесс повторяется до тех пор, пока не будет найден элемент или не останется один элемент.

1. Задайте целевой элемент, который вы ищете.
2. Установите левую и правую границы массива (начало и конец).
3. Пока левая граница меньше или равна правой границе:
   a. Вычислите индекс среднего элемента.
   b. Сравните целевой элемент с элементом в середине.
   c. Если целевой элемент равен элементу в середине, верните индекс.
   d. Если целевой элемент меньше элемента в середине, обновите правую границу на индекс среднего элемента - 1.
   e. Если целевой элемент больше элемента в середине, обновите левую границу на индекс среднего элемента + 1.
4. Если элемент не найден, верните -1 (или другое значение, указывающее на отсутствие).


