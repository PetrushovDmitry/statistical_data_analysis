---
## Front matter
title: "Отчет по лабораторной работе 5"
author: "Петрушов Дмитрий, 1032212287"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Цель работы

Основная цель работы — освоить синтаксис языка Julia для построения графиков.
 
# Выполнение лабораторной работы

## Основные пакеты для работы с графиками в Julia

Julia поддерживает несколько пакетов для работы с графиками. Использование того или иного пакета 
зависит от целей, преследуемых пользователем при построении. Стандартным для Julia является пакет Plots.jl.

Рассмотрим построение графика функции f(x) = (3x2 + 6x - 9)e-0,3x разными способами (рис. [-@fig:001] - (рис. [-@fig:002]):

![График функции, построенный при помощи gr()](image/1.png){ #fig:001 width=100% height=100% }

![График функции, построенный при помощи pyplot()](image/2.png){ #fig:002 width=100% height=100% }

## Опции при построении графика

На примере графика функции sin(x) и графика разложения этой функции в ряд Тейлора рассмотрим 
дополнительные возможности пакетов для работы с графикой (рис. [-@fig:003] - рис. [-@fig:005]):

![График функции sin(x)](image/3.png){ #fig:003 width=100% height=100% }

![График функции разложения исходной функции в ряд Тейлора](image/4.png){ #fig:004 width=100% height=100% }

![Графики исходной функции и её разложения в ряд Тейлора](image/5.png){ #fig:005 width=100% height=100% }

Затем добавим различные опции для отображения на графике (рис. [-@fig:006]):

![Вид графиков после добавления опций при их построении](image/6.png){ #fig:006 width=100% height=100% }

## Точечный график

Как и при построении обычного графика для точечного графика необходимо задать массив значений x, 
посчитать или задать значения y, задать опции построения графика (рис. [-@fig:007]):

![График десяти случайных значений на плоскости (простой точечный график)](image/7.png){ #fig:007 width=100% height=100% }

Для точечного графика можно задать различные опции, например размер маркера, его тип, цвет и и т.п. (рис. [-@fig:008]):

![График пятидесяти случайных значений на плоскости с различными опциями отображения (точечный график с кодированием значения размером точки)](image/8.png){ #fig:008 width=100% height=100% }

Также можно строить и 3-мерные точечные графики (рис. [-@fig:009]):

![График пятидесяти случайных значений в пространстве с различными опциями отображения (3-мерный точечный график с кодированием значения размером точки)](image/9.png){ #fig:009 width=100% height=100% }

## Аппроксимация данных

Аппроксимация — научный метод, состоящий в замене объектов их более простыми аналогами, сходными по своим свойствам.

Для демонстрации зададим искусственно некоторую функцию, в данном случае похожую по поведению на экспоненту (рис. [-@fig:010]):

![Пример функции](image/10.png){ #fig:010 width=100% height=100% }

Аппроксимируем полученную функцию полиномом 5-й степени (рис. [-@fig:011]):

![Пример аппроксимации исходной функции полиномом 5-й степени](image/11.png){ #fig:011 width=100% height=100% }

## Две оси ординат

Иногда требуется на один график вывести несколько траекторий с существенными отличиями в значениях по оси ординат.

Пример первой траектории (рис. [-@fig:012]):

![Пример отдельно построенной траектории](image/12.png){ #fig:012 width=100% height=100% }

## Полярные координаты

Приведём пример построения графика функции в полярных координатах (рис. [-@fig:013]):

![График функции, заданной в полярных координатах](image/13.png){ #fig:013 width=100% height=100% }

## Параметрический график

Приведём пример построения графика параметрически заданной кривой на плоскости (рис. [-@fig:014]):

![Параметрический график кривой на плоскости](image/14.png){ #fig:014 width=100% height=100% }

Далее приведём пример построения графика параметрически заданной кривой в пространстве (рис. [-@fig:015]):

![Параметрический график кривой в пространстве](image/15.png){ #fig:015 width=100% height=100% }

## График поверхности

Для построения поверхности, заданной уравнением f(x, y) = x2 + y2, можно воспользоваться функцией surface() (рис. [-@fig:016]):

![График поверхности (использована функция surface())](image/16.png){ #fig:016 width=100% height=100% }

Также можно воспользоваться функцией plot() с заданными параметрами (рис. [-@fig:017]):

![График поверхности (использована функция plot())](image/17.png){ #fig:017 width=100% height=100% }

Можно задать параметры сглаживания (рис. [-@fig:018]):

![Сглаженный график поверхности](image/18.png){ #fig:018 width=100% height=100% }

Можно задать определённый угол зрения (рис. [-@fig:019]):

![График поверхности с изменённым углом зрения](image/19.png){ #fig:019 width=100% height=100% }

## Линии уровня

Линией уровня некоторой функции от двух переменных называется множество точек на координатной 
плоскости, в которых функция принимает одинаковые значения. Линий уровня бесконечно много, и 
через каждую точку области определения можно провести линию уровня.

С помощью линий уровня можно определить наибольшее и наименьшее значение исходной функции от 
двух переменных. Каждая из этих линий соответствует определённому значению высоты. 

Поверхности уровня представляют собой непересекающиеся пространственные поверхности.

Рассмотрим поверхность, заданную функцией g(x, y) = (3x + y2)| sin(x) + cos(y)| (рис. [-@fig:020]):

![График поверхности, заданной функцией g(x, y) = (3x + y2)| sin(x) + cos(y)|](image/20.png){ #fig:020 width=100% height=100% }

Линии уровня можно построить, используя проекцию значений исходной функции на плоскость (рис. [-@fig:021]):

![Линии уровня](image/21.png){ #fig:021 width=100% height=100% }

Можно дополнительно добавить заливку цветом (рис. [-@fig:022]):

![Линии уровня с заполнением](image/22.png){ #fig:022 width=100% height=100% }

## Векторные поля

Если каждой точке некоторой области пространства поставлен в соответствие вектор с началом в 
данной точке, то говорят, что в этой области задано векторное поле.

Векторные поля задают векторными функциями.

Для функции h(x, y) = x3 - 3x + y2 сначала построим её график (рис. [-@fig:023]) и линии
уровня (рис. [-@fig:024]):

![График функции h(x, y) = x3 - 3x + y2](image/23.png){ #fig:023 width=100% height=100% }

![Линии уровня для функции h(x, y) = x3 - 3x + y2](image/24.png){ #fig:024 width=100% height=100% }

Векторное поле можно охарактеризовать векторными линиями. Каждая точка векторной линии является 
началом вектора поля, который лежит на касательной в данной точке. 

Для нахождения векторной линии требуется решить дифференциальное уравнение.

## Анимация

Технически анимированное изображение представляет собой несколько наложенных изображений 
(или построенных в разных точках графиках) в одном файле.

В Julia рекомендуется использовать gif-анимацию в pyplot().

Строим поверхность (рис. [-@fig:025]):

![Статичный график поверхности](image/25.png){ #fig:025 width=100% height=100% }

Добавляем анимацию (рис. [-@fig:026]):

![Анимированный график поверхности](image/26.png){ #fig:026 width=100% height=100% }

## Гипоциклоида

Гипоциклоида — плоская кривая, образуемая точкой окружности, катящейся по внутренней стороне другой 
окружности без скольжения.

Построим большую окружность (рис. [-@fig:027]):

![Большая окружность гипоциклоиды](image/27.png){ #fig:027 width=100% height=100% }

Для частичного построения гипоциклоиды будем менять параметр t (рис. [-@fig:028]):

![Половина пути гипоциклоиды](image/28.png){ #fig:028 width=100% height=100% }

Добавляем малую окружность гипоциклоиды (рис. [-@fig:029]):

![Малая окружность гипоциклоиды](image/29.png){ #fig:029 width=100% height=100% }

Добавим радиус для малой окружности (рис. [-@fig:030]):

![Малая окружность гипоциклоиды с добавлением радиуса](image/30.png){ #fig:030 width=100% height=100% }

В конце сделаем анимацию получившегося изображения (рис. [-@fig:031]):

![Малая окружность гипоциклоиды с добавлением радиуса](image/31.png){ #fig:031 width=100% height=100% }

## Errorbars

В исследованиях часто требуется изобразить графики погрешностей измерения.

Построим график исходных значений (рис. [-@fig:032]):

![График исходных значений](image/32.png){ #fig:032 width=100% height=100% }

Построим график отклонений от исходных значений (рис. [-@fig:033]):

![График исходных значений с отклонениями](image/33.png){ #fig:033 width=100% height=100% }

Повернём график (рис. [-@fig:034]):

![Поворот графика](image/34.png){ #fig:034 width=100% height=100% }

Заполним область цветом (рис. [-@fig:035]):

![Заполнение цветом](image/35.png){ #fig:035 width=100% height=100% }

Можно построить график ошибок по двум осям (рис. [-@fig:036]):

![График ошибок по двум осям](image/36.png){ #fig:036 width=100% height=100% }

Можно построить график асимметричных ошибок по двум осям (рис. [-@fig:037]):

![График асимметричных ошибок по двум осям](image/37.png){ #fig:037 width=100% height=100% }

## Использование пакета Distributions

Строим гистограмму.


Задаём нормальное распределение и строим гистограмму.


Далее применим для построения нескольких гистограмм распределения людей по возрастам на одном 
графике plotly().  
Ничего из этого не получилось сделать.  


## Подграфики

Определим макет расположения графиков. Команда layout принимает кортеж layout = (N, M), который 
строит сетку графиков NxM. Например, если задать layout = (4,1) на графике четыре серии, 
то получим четыре ряда графиков (рис. [-@fig:038]):

![Серия из 4-х графиков в ряд](image/38.png){ #fig:038 width=100% height=100% }

Для автоматического вычисления сетки необходимо передать layout целое число (рис. [-@fig:039]):

![Серия из 4-х графиков в сетке](image/39.png){ #fig:039 width=100% height=100% }

Аргумент heights принимает в качестве входных данных массив с долями желаемых высот. Если в 
сумме дроби не составляют 1,0, то некоторые подзаголовки могут отображаться неправильно.

Можно сгенерировать отдельные графики и объединить их в один, например, в сетке 2 × 2 (рис. [-@fig:040]):

![Объединение нескольких графиков в одной сетке](image/40.png){ #fig:040 width=100% height=100% }

Обратите внимание, что атрибуты на отдельных графиках применяются к отдельным графикам, 
в то время как атрибуты в последнем вызове plot применяются ко всем графикам.

Разнообразные варианты представления данных (рис. [-@fig:041]):

![Разнообразные варианты представления данных](image/41.png){ #fig:041 width=100% height=100% }

Применение макроса @layout наиболее простой способ определения сложных макетов. Точные размеры 
могут быть заданы с помощью фигурных скобок, в противном случае пространство будет поровну 
разделено между графиками (рис. [-@fig:042]):

![Демонстрация применения сложного макета для построения графиков](image/42.png){ #fig:042 width=100% height=100% }



# Вывод

В ходе выполнения лабораторной работы был освоен синтаксис языка Julia для построения графиков.

# Список литературы{.unnumbered}

::: {#refs}
:::