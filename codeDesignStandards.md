# Стандарты написания кода
## По коментариям (типы):
- "//" - после такого коментария идет описание того, что происходит
- "//*" - после такого коментария идет то, что необходимо доделать, реализовать и т.п. в будущем
----------------------------------------------------------------------------------------------------
## К самому сладкому(стандарты написания кода):
### Форматирование файлов:
1. Oбщее: 
- Выносить все String(а также цвета и стили) значения из файлов разметки в файл strings.xml(colors.xml, styles.xml).
2. Отступы:
- Отступы делаем при помощи табуляции.
3. Максимальная длина строки:
- Рекомендуется длина в 80 символов.
### Соглашение по именованию
1. Пространства имен:
- Имена пространств могут содержать только буквенно-числовые символы. Числа допустимы в именах, но не приветствуются;
- Если имя пространства состоит из более чем одного слова, то первая буква каждого слова должна быть заглавной, например, "Space\GoodStyle". Последующие заглавные буквы недопустимы.
2. Классы (и интерфейсы):
- Названия всегда начинаются с заглавной буквы;
- Содержат только буквы;
- Если название состоит из более чем одного слова, то первая буква каждого слова заглавная (CamelCase);
- Не допускается написание русских слов английской раскладкой.
3. Имена файлов:
- Для файлов разрешены буквенно-численные символы, символы нижнего подчеркивания;
- Запрещены пробелы и тире.
4. Функции и методы:
- Имена функций могут содержать буквенные символы;
- Имя всегда начинается с маленькой буквы;
- В написании имен используется CamelCase;
- Название функции, обычно, глагол. Реже - другая часть речи;
- Функции в глобальной области видимости допустимы, но не приветствуются (public).
5. Переменные:
- Переменнные, которые часто используются в классе (и те, которые используются в нескольких методах) выносятся как поле класса с разрешением private;
- Остальные переменные объявляются в том месте, где первый раз используются;
- Не static и не public поля начинаются с m (допускается нарушение этого правила):
```java
class test{
 private int mFirstVariable;
 
 }
 ```
- Имены переменных должны быть максимально говорящими;
- При написании используется CamelCase.
- Переменные в глобальной области видимости не приветствуются (public).
6. Константы:
- Имена констант пишутся в верхнем регистре;
- Между словами ставится нижнее подчеркивание;
- Пример константы:
 ```java
class test{
 public static final int SOME_CONST = 45;
 
 }
```
### Стиль кодирования
1. Классы:
- Класс должен быть логически разделен на блоки:
1.Константы;
2.Переменные;
3.Методы.
- Перед блоками методов обязательны коментарии;
- В одном java файле разрешен только один класс.
2. Функции:
- Функции всегда должны определять свою область видимости (static, private, public);
- Перед объявлением функции обязателен коментарий, кратко описывающий происходящее в функции. Если функция что-то возвращает, то в коментарии должно быть описание этой переменной (что в ней происходит);
3. Управляющие структуры (if, else, else if, catch):
- Структура if, else if и catch не должны иметь пробелы до открывающейся круглой скобки с условием. Перед фигурной - один пробел:
```java
class test{
    onCreate() {
        if(a == 2) {
        }

        switch(5) {
        }
    }
}
```
- Для выражений if, else if, else форматирование должно быть следующим:
```java
class test{
    onCreate() {
        if(a == 2) {
        }
        else if(a == 3) {
        }
        else {
        }
    }
}
```
- Открывающаяся фигурная скобка пишется на той же строке, где и конструкция "if" / "else if" / "else" / "catch". Закрывающаяся фигурная скобка пишется на отдельной строке. Все содержимое между фигурными скобками пишется с отступом в два пробела;
- Использование управляющей структуры без фигурной скобки не допускается.
4. Циклы (while, for, foreach):
- Перед открывающейся круглой скобкой условия пробела нет. Перед фигурной - один;
- Открывающаяся фигурная скобка пишется на той же строке, где и конструкция "for" / "foreach". Закрывающаяся фигурная скобка пишется на отдельной строке. Все содержимое между фигурными скобками пишется с отступом в два пробела.
- В цикле for желательно объявление счетчика внутри конструкции (или перед самим циклом):
 ```java
 class test{
    onCreate() {
        for(int a = 0; a < 10; a++) {
        }
    }
}
```
### Встроенная документация
1. Файлы, классы:
- В начале каждого файла (особенно не очень часто используемого (не layout, не класс к этому layout)) приветствуется описание файла.
