# Лабораторная работа: Использование команды grep

## Предварительные требования
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
И заполните файл, например, текстом стихотворения Федора Тютчева:
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
    - Попробуйте использовать параметр -i для игнорирования регистра при поиске и параметр -n для вывода номера строки:
``` bash
grep -in "как" testfile.txt
```
После выполнения команды вы должны увидеть следующий вывод:
``` bash
2:Как тихо веет над долиной
4:Как шум от стаи журавлиной, —
7:Как море вешнее в разливе,
```
## 2. Задание
Напишите Bash-скрипт, который будет принимать слово для поиска в качестве аргумента и искать его во всех текстовых файлах в текущей директории. Результаты поиска должны записываться в файл results.txt.

## Как успешно сдать работу?
Создать свой репозиторий из шаблона этого. Как это делается - "Use this template" -> "Create a new repository" и сделайте его public. 

Находясь уже в своем репозитории - создайте новый файл формата .md и там оформляйте отчет. В отчете опишите все шаги которые вы делали, чтобы получить финальный результат работы.

Что вам нужно знать, чтобы успешно защитить работу:
- Основные принципы работы с текстом в Linux.
- Как использовать команду grep для поиска строк в файлах.
- Как применять различные параметры grep, такие как -i (игнорирование регистра), -r (рекурсивный поиск), -v (вывод строк, не содержащих шаблон).
- Как обрабатывать результаты и записывать их в файл.
- Как составлять и тестировать скрипты для автоматизации задач.
## Источники
1. [Команда grep в Linux](https://timeweb.cloud/tutorials/linux/komanda-grep-v-linux)
2. [Что такое grep](https://habr.com/ru/articles/229501/)
3. [16 полезных опций grep](https://proglib.io/p/16-opciy-grep-kotorye-pomogut-vam-v-realnom-mire-2021-03-16)
4. [grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
5. [Команда grep](https://losst.pro/gerp-poisk-vnutri-fajlov-v-linux)
