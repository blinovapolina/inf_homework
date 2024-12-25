# Лабораторная работа: Использование команды grep

## Предварительные требования:
Для выполнения данной лабораторной работы потребуется доступ к системе Linux или эквивалентной среды, поддерживающей команды shell. Мы будем использовать утилиту командной строки ```grep```, которая предназначена для поиска текста в файлах.

## Введение
Grep — утилита командной строки, которая находит на вводе строки, отвечающие заданному регулярному выражению, и выводит их, если вывод не отменён специальным ключом. \
Команда grep встроена во множество дистрибутивов операционной системы Linux. Она выполняет поиск либо конкретного файла с указанным текстом, либо конкретной строки внутри файла с указанными символами. \
Синтаксис команды:
``` bash
grep [флаги] выражение [путь к директории или файлу]
```

## 1. Разминка
Перед выполнением основного задания познакомимся с примерами использований данной команды:
1. Создание тестового файла
    - Создайте текстовый файл testfile.txt, который будет содержать несколько строк текста. Выполните следующую команду в терминале:
``` bash
touch testfile.txt
```
И заполните файл, например, текстом стихотворения Федора Тютчева
```
Вечер
Как тихо веет над долиной
Далекий колокольный звон,
Как шум от стаи журавлиной, —
И в звучных листьях замер он.

Как море вешнее в разливе,
Светлея, не колыхнет день, —
И торопливей, молчаливей
Ложится по долине тень.

Тютчев Фёдор
```
2. Поиск с помощью grep
    - Используйте команду grep для поиска строк, содержащих слово "Как":
``` bash
grep "Как" testfile.txt
```
3. Ожидаемый результат
    - После выполнения команды вы должны увидеть следующий вывод:
```
Как тихо веет над долиной
Как шум от стаи журавлиной, —
Как море вешнее в разливе,
```
4. Дополнительные параметры
    - Попробуйте использовать параметр -i для игнорирования регистра при поиске:
``` bash
grep -i "Как" testfile.txt
```
