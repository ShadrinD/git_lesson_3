# Инструкция для работы с Git
## Что такое Git и зачем он нужен?
Git - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов.
С помощью Git-a вы можете откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.
Репозиторием называют хранилище вашего кода и историю его изменений. Git работает локально и все ваши репозитории хранятся в определенных папках на жестком диске.

Каждая точка сохранения вашего проекта носит название commit. У каждого commit-a есть hash (уникальный id) и комментарий. Из таких commit-ов собирается ветка. Ветка - это история изменений. У каждой ветки есть свое название. Репозиторий может содержать в себе несколько веток, которые создаются из других веток или вливаются в них.

## Настройка Git

### Установка имени пользователя
*git config --global user.name "<ваше_имя>"*

### Установка email.
*git config --global user.email "<адрес_почты@email.com>"*

## Инициализация/создание репозитория

*git init*

Так Git отслеживает изменения файлов вашего проекта. Но, так как вы только создали репозиторий в нем нет вашего кода. Для этого необходимо создать commit.
## Создание commit
### Добавим все файлы проекта в нам будующий commit

*git add .* 
Или чтобы добавить все *git add --all*

### Для конкретного файла

*git add <имя_файла>*

## Добавление commit.
commit работает как сохранение наших изменений файла

*git commit -m "<комментарий>"*

## Просмотр состояния
Для того чтобы посмотреть текущее состояние ветки, например, какие файлы добавлены или не добавлены для создания commit, можно выполнить команду:

*git status*

### Переход между версиями
*git checkout master* Направляет к основной версии файла. 

*git checkout <id>* Направит к конкретной прошлой версии файла

### Список всех версий
Для просмотра списком всех версий файла до выбранной используется команда:

*git log*

Там можно найти присвоенные каждом коммиту id (hash)

### Просмотр различий между файлами
Просмотреть изменения относительно двух веток можно командой:

git diff <исходная_ветка> <целевая_ветка>

# Кратко
*git config --global user.name "<ваше_имя>"*

*git config --global user.email "<адрес_почты@email.com>"*

*git init*

*git add .* 

*git commit -m "<комментарий>"*

*git status*

*git checkout <id>*

*git log*

git diff <исходная_ветка> <целевая_ветка>

# Синтаксис

## Параграфы и разрывы строк
Чтобы поделить текст на параграфы, между ними нужно оставить пустую строку. Строка считается пустой, даже если в ней есть пробелы и табуляции. Если же строки находятся рядом, то они автоматически склеиваются в одну.

Пример:

Первый параграф

Второй параграф
Продолжение второго параграфа

## Перенос строки
Для переноса строки внутри одного параграфа есть три метода:

-поставить в конце строки два или больше пробела   
-поставить в конце строки обратную косую черту \  
-использовать HTML-тег <br>

 у каждого из методов есть свои недостатки:

*пробелы в конце строки бывает трудно заметить, и это может запутать читателя

*обратный слеш вводится в стандарте CommonMark и может поддерживаться не всеми редакторами

*HTML-теги в Markdown также поддерживаются не всеми редакторами

## Заголовки
В синтаксисе Markdown есть шесть уровней заголовков: от H1 (самого большого) до H6 (самого маленького). Для их выделения используют решётки #. Между решёткой и текстом ставится пробел.
# Заголовок первого уровня
## Заголовок второго уровня 
### Заголовок третьего уровня
#### Заголовок четвёртого уровня
##### Заголовок пятого уровня
###### Заголовок шестого уровня



## Выделение текста
Чтобы изменить начертание текста, нужно выделить его с двух сторон спецсимволами следующим образом: <спецсимвол>текст<спецсимвол>.

## Курсив
Для выделения текста курсивом нужно использовать одну звёздочку * или нижнее подчёркивание _.

*Текст курсивом*

_Текст курсивом_

## Жирный
Для выделения текста жирным нужно использовать две звёздочки ** или два нижних подчёркивания __.

**Жирный текст**

__Жирный текст__


## Жирный курсив
Для выделения текста сразу обоими стилями нужно использовать три звёздочки *** или три нижних подчёркивания ___.

***Текст жирным курсивом***

___Текст жирным курсивом___

## Зачёркнутый
Чтобы зачеркнуть текст, нужно использовать две тильды ~~. Такая опция есть только в диалекте GitHub Flavored Markdown.

~~Зачёркнутый текст~~

#Подчёркнутый
В синтаксисе Markdown нет встроенного способа подчеркнуть текст. Но если ваш редактор поддерживает HTML, то можно использовать теги:

<u>Подчёркнутый текст</u>

## Разделители
Чтобы оформить горизонтальный разделитель, нужно поставить три или больше специальных символа: звёздочки *, дефиса - или нижних подчёркивания _. Они должны находиться на отдельной строке, и между ними можно ставить любое количество пробелов и табуляций.

Если ваш редактор поддерживает HTML-теги, то для разметки можно также использовать тег <hr>.

***
---
___
*	*  **


## Цитаты
Чтобы параграф отобразился как цитата, нужно поставить перед ним закрывающую угловую скобку >.

> Оформление цитатой
последовательных строк
внутри одного параграфа


Внутрь одного блока цитаты можно поместить сразу несколько параграфов и использовать любые элементы оформления. Например, заголовки и другие цитаты. Чтобы сделать это, нужно поместить закрывающую угловую скобку перед началом каждой строки.

> # Заголовок
> Первый параграф
>
> Второй параграф
>
> > Вложенная цитата
> > > Цитата третьего уровня
>
> Продолжение основной цитаты


## Списки
В синтаксисе Markdown есть несколько видов списков. Для их оформления перед каждым пунктом нужно поставить подходящий тег и отделить его от текста пробелом.

### Нумерованные (ordered)
Для создания нумерованного списка перед пунктами нужно поставить число с точкой. При этом нумерация в разметке ленивая. Неважно, какие именно числа вы напишете: Markdown пронумерует список автоматически.

1. Первый пункт
2. Второй пункт
3. Третий пункт


1. Первый пункт
1. Второй пункт
1. Третий пункт


1. Первый пункт
73. Второй пункт
5. Третий пункт


Список можно начинать и не с единицы. Для нумерации важно только число, которое стоит перед первым пунктом.

27. Первый пункт
27. Второй пункт
27. Третий пункт


### Ненумерованные
Для создания ненумерованного списка нужно поставить перед каждым пунктом звёздочку *, дефис - или плюс +.

* Первый пункт
* Второй пункт
* Третий пункт
- Первый пункт
- Второй пункт
- Третий пункт
+ Первый пункт
+ Второй пункт
+ Третий пункт

### Чекбоксы
Чтобы сделать чекбоксы, нужно использовать маркированный список, но между маркером и текстом поставить [x] для отмеченного пункта и [] — для неотмеченного.

Чекбоксы доступны в диалекте GitHub Flavored Markdown (тот самый, который умеет зачёркивать текст) и поддерживаются не всеми редакторами Markdown. Например, нам для демонстрации примера пришлось открывать другой.

- [x] Отмеченный пункт
- [ ] Неотмеченный пункт


### Вложенные
Чтобы создать вложенный список, нужно поставить перед его пунктами табуляцию или несколько пробелов. В Markdown одна табуляция соответствует четырём пробелам.

Список одного вида можно вкладывать в любой другой.

1. Пункт
	1. Подпункт
		1. Подподпункт

- Пункт
	- Подпункт
		- Подподпункт


1. Пункт
	- Подпункт
		* Подподпункт

+ Пункт
	1. Подпункт

- Пункт
  - [x] Отмеченный подпункт
  - [ ] Неотмеченный подпункт
    1. Подподпункт

### Другие элементы внутри списков
В пункты списков можно добавлять другие элементы оформления. Например, параграфы или цитаты. Для этого нужно сделать отступ, как если бы вы добавляли вложенный список.

1. Первый пункт
	> Цитата внутри первого пункта
1. Второй пункт
 	
    Параграф внутри второго пункта
1. Третий пункт

## Ссылки
Самый лёгкий способ поместить ссылку в Markdown — заключить её в угловые скобки. 

<https://google.com/>


Чтобы оформить ссылкой часть текста, используется такой синтаксис: [текст](ссылка). Можно сделать всплывающую подсказку при наведении курсора. Для этого в круглых скобках после ссылки нужно поставить пробел и написать текст подсказки в кавычках.

[Youtube](https://youtube.com/) без подсказки

[Прокрастинация](https://youtube.com/ "Не надо") с подсказкой


Ещё один способ оформить ссылку — справочный. Он работает как сноски в книгах: [текст][имя сноски]. При таком способе организации ссылок в конце документа нужно также написать и оформить саму сноску: [имя сноски]: ссылка. При желании после ссылки можно добавить подсказку — точно так же, как в предыдущем методе.

Имя сноски может быть любым сочетанием символов: цифрами, буквами и даже знаками препинания. На одну и ту же сноску в тексте можно ссылаться сколько угодно раз.

Ссылки, оформленные справочным методом, выглядят и работают точно так же, как и в предыдущем способе. Сами сноски в отформатированном документе не отображаются.

## Картинки (images)
Изображения в Markdown оформляются по принципу, схожему с принципом оформления ссылкок, только перед квадратными скобками нужно поставить восклицательный знак: ![текст](путь к изображению). Здесь также можно сделать всплывающую подсказку.

![Изображение](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/1920px-Markdown-mark.svg.png "Логотип Markdown")

Можно использовать и справочный метод: ![текст][имя сноски]. Сноски оформляются так же, как и в ссылках: [имя сноски]: путь к изображению, — в них тоже можно добавлять подсказки.

![Изображение][1]


[1]: https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/1920px-Markdown-mark.svg.png "Логотип Markdown"
Такая разметка выведет тот же результат, что и предыдущая.

## Вставка кода
В Markdown есть несколько способов выделить исходный код:

Если надо отобразить фрагмент кода внутри строки с каким-то текстом, нужно с двух сторон выделить этот код одним или несколькими обратными апострофами (`; их ещё называют бэктиками).
Чтобы выделить фрагмент из нескольких строк, нужно с двух сторон выделить его тремя обратными апострофами.
Также перед фрагментом кода можно поставить табуляцию или четыре пробела, при этом предыдущая строка должна быть пустой.
Функция `print (x)` выводит содержимое переменной ```x```.

```
#include <stdio.h>
int main() {
   printf("Hello, World!");
   return 0;
}
```

	let x = 12;
	let y = 6;
	console.log(x + y);

Отображение результата в браузере
Скриншот: Skillbox Media
Если обрамлять код тремя обратными апострофами, то после первой тройки можно указать язык программирования — тогда Markdown правильно подсветит элементы кода.

```python
if x > 0:
	print (x)
else:
	print ('Hello, World!')
```

```c
#include <stdio.h>
int main() {
   printf("Hello, World!");
   return 0;
}
```

```javascript
let x = 12;
let y = 6;
console.log(x + y);
```

Возможность вставлять блоки кода тремя обратными апострофами появилась в спецификации CommonMark, но там не указан список псевдонимов: как правильно называть языки, чтобы Markdown понял, о чём речь.

Поэтому каждая реализация ведёт свой собственный список языков и их псевдонимов. Так как их очень много, да ещё и новые время от времени добавляются, то удобных таблиц обычно не делают. Предлагают сразу ознакомиться с конфигурационным файлом.

Вот такой список языков, например, поддерживает диалект GitHub Flavored Markdown.

## Таблицы
В уже упомянутом выше диалекте GitHub Flavored Markdown (и некоторых других тоже) есть возможность оформлять таблицы. Столбцы разделяются вертикальными линиями |, а строка с шапкой отделяется от остальных дефисами -, которых можно ставить сколько угодно.

|Столбец 1|Столбец 2|Столбец 3|
|-|--------|---|
|Длинная запись в первом столбце|Запись в столбце 2|Запись в столбце 3|
|Кртк зпс| |Слева нет записи|

Чтобы выровнять весь столбец по правому краю, в строке с дефисами сразу после дефисов можно поставить двоеточие :. Чтобы выровнять содержимое по центру, надо поставить двоеточия с обеих сторон.

|Столбец 1|Столбец 2|Столбец 3|
|:-|:-:|-:|
|Равнение по левому краю|Равнение по центру|Равнение по правому краю|
|Запись|Запись|Запись|

# Ветки версий

## Создание веток
С помощью команды git branch мы вызываем список всех веток версий в репозитории.


Чтобы создать новую ветку версий файла, используется команда git branch название_ветки.


Для перехода между ветками используется команда git checkout branch_name.
## Слияние веток

## Удаление веток

## Разница между версиями