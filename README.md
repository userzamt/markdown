# Markdown
**Markdown** (произносится маркдаун) — облегчённый язык разметки, созданный с целью обозначения форматирования в простом тексте, с максимальным сохранением его читаемости человеком, и пригодный для машинного преобразования в языки для продвинутых публикаций (HTML, Rich Text и других).



## Диалекты и редакторы
Базовым синтаксисом Markdown уже мало кто пользуется. Зато у него существуют спецификации и диалекты, которые добавляют в язык новые функции: встраивание HTML-тегов, создание таблиц и чекбоксов, зачёркивание текста, разные варианты переноса строки.

Разные редакторы Markdown могут поддерживать или не поддерживать часть новых функций — учтите это при выборе платформы, на которой будете работать.

Самый распространённый Markdown — диалект [GitHub Flavored Markdown](https://github.github.com/gfm/), основанный на [спецификации CommonMark](https://commonmark.org/). 



## Заголовки
В синтаксисе Markdown есть шесть уровней заголовков: от `H1` (самого большого) до `H6` (самого маленького). Для их выделения используют решётки `#`, при этом есть несколько тонкостей:
    
+ количество решёток соответствует уровню заголовка: одна для первого уровня, две для второго и так далее;
+ между решёткой и текстом ставится пробел.

```
# A first-level heading
## A second-level heading
### A third-level heading
```

![Уровни заголовков](https://docs.github.com/assets/cb-11407/mw-1440/images/help/writing/headings-rendered.webp)

У заголовков первого и второго уровня есть альтернативный способ выделения: на следующей строке после них нужно поставить знаки равенства `=` или дефисы `-`. Вот несколько правил:

+ знак `=` применяется для заголовков `H1`;
+ дефис применяется для заголовков `H2`;
+ если в одной строке поставить оба знака, то работать ничего не будет;
+ можно ставить любое количество знаков, и на тип заголовка это не повлияет;
+ между заголовком и знаками не должно быть пустых строк.

```
Заголовок первого уровня
=
Заголовок первого уровня
=========
Заголовок второго уровня
-
Заголовок второго уровня
----------
```



## Текст
Чтобы изменить начертание текста, нужно выделить его с двух сторон спецсимволами 

```
*Этот текст будет наклонным (курсив)*
_Этот текст будет наклонным (курсив)_

**Этот текст будет жирным**
__Этот текст будет жирным__

_Можно **вставлять** один тип в другой_
```

*Этот текст будет наклонным (курсив)*
_Этот текст будет наклонным (курсив)_

**Этот текст будет жирным**
__Этот текст будет жирным__

_Можно **вставлять** один тип в другой_

> [!IMPORTANT]
> Обратите внимание, что если вы хотите выделить фрагмент внутри слова, то это корректно сработает только при использовании звёздочек.

```
Кор*рек*тно, кор**рек**тно, кор***рек***тно

Некор_рек_тно, некор__рек__тно, некор___рек___тно
```

Кор*рек*тно, кор**рек**тно, кор***рек***тно

Некор_рек_тно, некор__рек__тно, некор___рек___тно



## Зачёркнутый текст
В GitHub Flavored Markdown добавлено зачеркивание текста. Если необходимо зачеркнуть текст, то можно поставить по две тильды (`~~`) в начале и в конце фрагмента.

```
~~Привет, студени!~~\
Здравствуйте, студенты!
```
~~Привет, студени!~~\
Здравствуйте, студенты!



## Горизонтальная линия (horizontal rules)
Чтобы оформить горизонтальный разделитель, нужно поставить три или больше специальных символа: звёздочки `*`, дефиса `-` или нижних подчёркивания `_`. Они должны находиться на отдельной строке, и между ними можно ставить любое количество пробелов и табуляций.

```
***
**   ** *
---
-- -
___
_ _ _
```

***
**   ** *
---
-- -
___
_ _ _



## Цитаты (blockquotes)
Чтобы параграф отобразился как цитата, нужно поставить перед ним закрывающую угловую скобку `>`.

```
> Дома новы, но предрассудки стары.
> 
> *Александр Грибоедов, "Горе от ума"*
```

> Дома новы, но предрассудки стары.
> 
> *Александр Грибоедов, "Горе от ума"*



## Абзацы
**Абзац**(параграф) — это одна или несколько подряд идущих строчек текста, отделённых одной или несколькими пустыми строчками. Если строка содержит только пробелы или табы, то она всё равно считается пустой.

Для создания абзацев используйте пустую строку для разделения одной или нескольких строк текста.

Чтобы создать разрыв строки или новую строку (`<br>`), завершите строку двумя или более пробелами, а затем введите `Enter`. Либо добавить обратную косую черту в конце строки `\`.



## Исходный код
Markdown позволяет специальным образом размечать исходный код. Все символы внутри будут автоматически экранированы.

```
Функция `alert()`
вызывает диалоговое окно.

Сумму двух переменных
можно вывести так:
``const a = 1;
const b = 2;
alert(a + b);``
```

Функция `alert()`
вызывает диалоговое окно.

Сумму двух переменных
можно вывести так:
``const a = 1;
const b = 2;
alert(a + b);``

---
Если обрамлять код тремя обратными апострофами, то после первой тройки можно указать язык программирования — тогда Markdown правильно подсветит элементы кода. Для примера ниже, указана язык `javascript`

```javascript
const a = 1;
const b = 2;
alert(a + b);
```

Возможность вставлять блоки кода тремя обратными апострофами появилась в спецификации CommonMark, но там не указан список псевдонимов: как правильно называть языки, чтобы Markdown понял, о чём речь.

Поэтому **каждая реализация ведёт свой собственный список языков** и их псевдонимов. Так как их очень много, да ещё и новые время от времени добавляются, то удобных таблиц обычно не делают. Предлагают сразу ознакомиться с конфигурационным файлом.

Вот такой [список языков](https://github.com/github-linguist/linguist/blob/main/lib/linguist/languages.yml), например, поддерживает диалект GitHub Flavored Markdown.



## Списки
В синтаксисе Markdown есть несколько видов списков. Для их оформления перед каждым пунктом нужно поставить подходящий тег и отделить его от текста пробелом.

Для разметки неупорядоченных списков можно использовать или `*`, или `-`, или `+`:

```
* Пункт
- Ещё один пункт
+ Ещё Ещё один пункт
```

* Пункт
- Ещё один пункт
+ Ещё Ещё один пункт

> [!IMPORTANT]
> В примере выше, на самом деле не один единый список, а три разных

Если в качестве маркеров использовать цифры c точкой на конце (1., 2. и т. д.), то мы получим упорядоченный (нумерованный) список.

```
1. Хлеб
2. Молоко
3. Помидоры
```

1. Хлеб
2. Молоко
3. Помидоры

Номера пунктов в итоговой разметке будут идти по порядку (1, 2, 3), даже если в Markdown будут стоять `1.`,` 4.`, `9.`. Такая особенность позволяет нам использовать *«ленивую нумерацию»*, когда перед каждым пунктом ставится одно и то же число.

```
1. Хлеб
1. Молоко
1. Помидоры
```

1. Хлеб
1. Молоко
1. Помидоры

Число перед первым пунктом показывает с чего нужно начинать нумеровать элементы списка, поэтому если в Markdown поставить `99.`, `1.`, `2.`, то в итоговой разметки пункты будут стоять под номерами `99`, `100`, `101`.

```
99. Хлеб
1. Молоко
1. Помидоры
```

99. Хлеб
1. Молоко
1. Помидоры

> [!NOTE] 
> Любые списки можно вкладывать друг в друга, для этого перед маркером нужно поставить таб или несколько пробелов

```
+ Хлеб
+ Молочные продукты
  1. Кефир
  2. Ряженка

1. Молоко
2. Хлебобулочные изделия
    + Бублик
    + Ватрушка
```

+ Хлеб
+ Молочные продукты
  1. Кефир
  2. Ряженка

1. Молоко
2. Хлебобулочные изделия
    + Бублик
    + Ватрушка



## Чекбокс
Чтобы сделать чекбоксы, нужно использовать маркированный список, но между маркером и текстом поставить [x] для отмеченного пункта и [] — для неотмеченного.

Чекбоксы доступны в диалекте **GitHub Flavored Markdown** и поддерживаются не всеми редакторами Markdown. 

```
- [x] Отмеченный пункт
- [ ] Неотмеченный пункт
```

- [x] Отмеченный пункт
- [ ] Неотмеченный пункт

В диалекте **GitHub Flavored Markdown** чекбоксы называются [списоком задач](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-task-lists) и созданы немного для другого.



## Таблицы
В уже упомянутом выше диалекте **GitHub Flavored Markdown** (и некоторых других тоже) есть возможность оформлять таблицы. Столбцы разделяются вертикальными линиями `|`, а строка с шапкой отделяется от остальных дефисами `-`, которых можно ставить сколько угодно.

```
| Место | Участник | Рейтинг |
|-------|----------|---------|
| 1     | Саша     | 118     |
| 2     | Юля      | 92      |
| 3     | Даниил   | 36      |


|Место|Участник|Рейтинг|
|-------|----------|---------|
|1|Саша|11|
|2|Юля|92|
|3|Даниил|36|
```

|Место|Участник|Рейтинг|
|-------|----------|---------|
|1|Саша|11|
|2|Юля|92|
|3|Даниил|36|

Чтобы выровнять весь столбец по правому краю, в строке с дефисами сразу после дефисов можно поставить двоеточие `:`. Чтобы выровнять содержимое по центру, надо поставить двоеточия с обеих сторон.

```
|Столбец 1|Столбец 2|Столбец 3|
|:-|:-:|-:|
|Равнение по левому краю|Равнение по центру|Равнение по правому краю|
|Запись|Запись|Запись|
```

|Столбец 1|Столбец 2|Столбец 3|
|:-|:-:|-:|
|Равнение по левому краю|Равнение по центру|Равнение по правому краю|
|Запись|Запись|Запись|



## Ссылки
[Ссылка на фото Alert](https://docs.github.com/assets/cb-24696/mw-1440/images/help/writing/alerts-rendered.webp)



## Изображения




## Emoji
[Существует множество эмодзи, которые вы можете использовать](https://gist.github.com/rxaviers/7360908)



## Alert
**alert** - это расширение Markdown на основе синтаксиса *blockquote*, который можно использовать для выделения критически важных сведений. На GitHub они отображаются с отличительными цветами и значками, чтобы указать важность содержимого.

```
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```

![сообщения](https://docs.github.com/assets/cb-24696/mw-1440/images/help/writing/alerts-rendered.webp)



## Экранирование (escaping characters)
Многие символы в **Markdown** выполняют роль служебных. Если они встречаются в вашем тексте сами по себе, то для корректного отображения их стоит экранировать (иначе они просто не только не отобразятся сами, но и добавят вашему тексту какое-нибудь ненужное форматирование). Для этого перед ними ставится обратная косая черта `\`.

Вот список символов, которые нужно экранировать: ```\`*_{}[]<>()#+-.!|```. Делать это постоянно необязательно — достаточно ставить экран только в тех случаях, когда Markdown может воспринять эти символы как служебные. Например, если строка начинается с символа `#`, то экранировать её надо — потому что программа может решить, что вы хотите сделать заголовок. А вот если решётка находится где-то в центре строки, то экранировать ничего не надо — редактор поймёт, что тут она просто часть текста.





