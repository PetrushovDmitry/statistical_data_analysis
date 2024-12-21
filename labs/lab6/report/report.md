---
## Front matter
title: "Отчет по лабораторной работе 6"
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

Основной целью работы является освоение специализированных пакетов для решения задач в 
непрерывном и дискретном времени.
 
# Выполнение лабораторной работы

## Решение обыкновенных дифференциальных уравнений

Вспомним, что обыкновенное дифференциальное уравнение (ОДУ) описывает изменение некоторой 
переменной u.

Для решения обыкновенных дифференциальных уравнений (ОДУ) в Julia можно использовать пакет 
diffrentialEquations.jl.

## Модель экспоненциального роста

Рассмотрим пример использования этого пакета для решение уравнения модели экспоненциального роста, 
описываемую уравнением, где a — коэффициент роста. 

Численное решение в Julia будет иметь следующий вид, а также график, 
соответствующий полученному решению (рис. [-@fig:001]):

![График модели экспоненциального роста](image/1.png){ #fig:001 width=100% height=100% }

При построении одного из графиков использовался вызов sol.t, чтобы захватить массив моментов 
времени. Массив решений можно получить, воспользовавшись sol.u.

Если требуется задать точность решения, то можно воспользоваться параметрами abstol 
(задаёт близость к нулю) и reltol (задаёт относительную точность). По умолчанию эти параметры 
имеют значение abstol = 1e-6 и reltol = 1e-3.

Для модели экспоненциального роста (рис. [-@fig:002]):

![График модели экспоненциального роста (задана точность решения)](image/2.png){ #fig:002 width=100% height=100% }

## Система Лоренца

Динамической системой Лоренца является нелинейная автономная система обыкновенных дифференциальных 
уравнений третьего порядка.

Система получена из системы уравнений Навье–Стокса и описывает движение воздушных потоков в 
плоском слое жидкости постоянной толщины при разложении скорости течения и температуры в 
двойные ряды Фурье с последующем усечением до первых-вторых гармоник.

Решение системы неустойчиво на аттракторе, что не позволяет применять классические численные методы на 
больших отрезках времени, требуется использовать высокоточные вычисления.

Численное решение в Julia будет иметь следующий вид (рис. [-@fig:003]):

![Аттрактор Лоренца](image/3.png){ #fig:003 width=100% height=100% }

Можно отключить интерполяцию (рис. [-@fig:004]):

![Аттрактор Лоренца (интерполяция отключена)](image/4.png){ #fig:004 width=100% height=100% }

## Модель Лотки–Вольтерры

Модель Лотки–Вольтерры описывает взаимодействие двух видов типа «хищник – жертва».

Численное решение в Julia будет иметь следующий вид (рис. [-@fig:005]):

![Модель Лотки–Вольтерры: динамика изменения численности популяций](image/5.png){ #fig:005 width=100% height=100% }

Фазовый портрет (рис. [-@fig:006]):

![Модель Лотки–Вольтерры: фазовый портрет](image/6.png){ #fig:006 width=100% height=100% }

## Самостоятельное выполнение

Выполнение задания №1 (рис. [-@fig:007]):

![Решение задания №1](image/7.png){ #fig:007 width=100% height=100% }

График №1 (рис. [-@fig:008]):

![график №1](image/8.png){ #fig:008 width=100% height=100% }

Выполнение задания №2 (рис. [-@fig:009]):

![Решение задания №2](image/9.png){ #fig:009 width=100% height=100% }

График №2 (рис. [-@fig:010]):

![График №2](image/10.png){ #fig:010 width=100% height=100% }

Выполнение задания №3 (рис. [-@fig:011]):

![Решение задания №3](image/11.png){ #fig:011 width=100% height=100% }

График №3 (рис. [-@fig:012]):

![График №3](image/12.png){ #fig:012 width=100% height=100% }

Выполнение задания №4 (рис. [-@fig:013]):

![Решение задания №4](image/13.png){ #fig:013 width=100% height=100% }

График №4 (рис. [-@fig:014]):

![График №4](image/14.png){ #fig:014 width=100% height=100% }

Выполнение задания №5 (рис. [-@fig:015]):

![Решение задания №5](image/15.png){ #fig:015 width=100% height=100% }

График №5 (рис. [-@fig:016]):

![График №5](image/16.png){ #fig:016 width=100% height=100% }

Выполнение задания №6 (рис. [-@fig:017]):

![Решение задания №6](image/17.png){ #fig:017 width=100% height=100% }

График №6 (рис. [-@fig:018]):

![График №6](image/18.png){ #fig:018 width=100% height=100% }

Выполнение задания №7 (рис. [-@fig:019]):

![Решение задания №7](image/19.png){ #fig:019 width=100% height=100% }

График №7 (рис. [-@fig:020]):

![График №7](image/20.png){ #fig:020 width=100% height=100% }

Выполнение задания №8 (рис. [-@fig:021]):

![Решение задания №8](image/21.png){ #fig:021 width=100% height=100% }

График №8 (рис. [-@fig:022]):

![График №8](image/22.png){ #fig:022 width=100% height=100% }

# Вывод

В ходе выполнения лабораторной работы были освоены специализированные пакеты для 
решения задач в непрерывном и дискретном времени.

# Список литературы{.unnumbered}

::: {#refs}
:::