# Контрольная работа в первой четверти

## Задача:

Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше
либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения
алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно
массивами.

*Примеры:*

`["hello", "2", "world", ":-)"]` -> `["2", ":-)"]`

`["Russia", "Kazan", "Denmark"]` -> `[]`

## Решение:

Задаем массив *`startArray`* на старте выполнения алгоритма.

Требуется создать новый текстовый массив *`finalArray`* с элементами, длина которых 3 и менее символа. Чтобы инициализировать его, нужно определиться с количеством элементов нового массива. Следовательно на первом этапе выясним количество требуемых элементов в исходном массиве *`startArray`*.

### Первый этап:
* Объявляем переменную *`countSymbol`* как равную нулю. 
* Организуем цикл по перебору всех элементов исходного массива. 
Каждый раз беря очередной  элемент, проверяем количество символов в его значении. 
* Если оно соответствует нашему условию (3 символа и менее), увеличиваем переменную *`countSymbol`* на единицу. 
* Если нет, переходим к следующему элементу исходного массива. 
* По окончании цикла в переменной *`countSymbol`* будет хранится количество удовлетворяющих условию элементов.

### Второй этап:
* Инициализируем новый массив *`finalArray`* длинной в *`countSymbol`* элементов.
* Объявляем новую переменную счетчика *`j`*, для указания индекса в новом массиве.
* Организуем очередной цикл по перебору исходного массива *`startArray`*, в поисках элементов, соответствующих условию.
* Каждый раз, при обнаружении "подходящего" элемента в исходном массиве *`startArray`*, присваиваем его значение элементу с индексом *`j`* нового массива *`finalArray`*. После чего увеличиваем индекс *`j`* на единицу.
* По окончании цикла в массиве *`finalArray`* будут хранится требуемые по условию задачи элементы.