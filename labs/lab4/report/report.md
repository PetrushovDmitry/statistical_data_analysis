---
## Front matter
title: "Отчет по лабораторной работе 4"
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

Основной целью работы является изучение возможностей специализированных пакетов Julia 
для выполнения и оценки эффективности операций над объектами линейной алгебры.
  

# Выполнение лабораторной работы

##  Поэлементные операции над многомерными массивами

Для матрицы 4 × 3 рассмотрим поэлементные операции сложения и произведения её элементов (рис. [-@fig:001]):

![Поэлементные операции сложения и произведения элементов матрицы](image/1.png){ #fig:001 width=100% height=100% }

Для работы со средними значениями можно воспользоваться возможностями пакета Statistics (рис. [-@fig:002]):

![Использование возможностей пакета Statistics для работы со средними значениями](image/2.png){ #fig:002 width=100% height=100% }

## Транспонирование, след, ранг, определитель и инверсия матрицы

Для выполнения таких операций над матрицами, как транспонирование, диагонализация, определение следа, ранга, определителя 
матрицы и т.п. можно воспользоваться библиотекой (пакетом) LinearAlgebra (рис. [-@fig:003] - рис. [-@fig:004]):

![Использование библиотеки LinearAlgebra для выполнения определённых операций](image/3.png){ #fig:003 width=100% height=100% }

![Использование библиотеки LinearAlgebra для выполнения определённых операций](image/4.png){ #fig:004 width=100% height=100% }

## Вычисление нормы векторов и матриц, повороты, вращения

Для вычисления нормы используется LinearAlgebra.norm(x) (рис. [-@fig:005]):

![Использование LinearAlgebra.norm(x)](image/5.png){ #fig:005 width=100% height=100% }

Вычислим нормы для двумерной матрицы (рис. [-@fig:006]):

![Вычисление нормы для двумерной матрицы](image/6.png){ #fig:006 width=100% height=100% }

## Матричное умножение, единичная матрица, скалярное произведение

Выполним примеры матричного умножения, единичной матрицы и скалярного произведения (рис. [-@fig:007]):

![Примеры матричного умножения, единичной матрицы и скалярного произведения](image/7.png){ #fig:007 width=100% height=100% }

## Факторизация. Специальные матричные структуры

Рассмотрим несколько примеров. Для работы со специальными матричными структурами потребуется 
пакет LinearAlgebra. 

Решение систем линейный алгебраических уравнений Ax = b (рис. [-@fig:008]):

![Решение систем линейный алгебраических уравнений Ax = b](image/8.png){ #fig:008 width=100% height=100% }

Julia позволяет вычислять LU-факторизацию и определяет составной тип факторизации
для его хранения (рис. [-@fig:009]):

![Пример вычисления LU-факторизации и определение составного типа факторизации для его хранения](image/9.png){ #fig:009 width=100% height=100% }

Исходная система уравнений Ax = b может быть решена или с использованием
исходной матрицы, или с использованием объекта факторизации (рис. [-@fig:010]):

![Пример решения с использованием исходной матрицы и с использованием объекта факторизации](image/10.png){ #fig:010 width=100% height=100% }

Julia позволяет вычислять QR-факторизацию и определяет составной тип факторизации для его хранения (рис. [-@fig:011]):

![Пример вычисления QR-факторизации и определение составного типа факторизации для его хранения](image/11.png){ #fig:011 width=100% height=100% }

Примеры собственной декомпозиции матрицы A (рис. [-@fig:012]):

![Примеры собственной декомпозиции матрицы A](image/12.png){ #fig:012 width=100% height=100% }

Далее рассмотрим примеры работы с матрицами большой размерности и специальной структуры (рис. [-@fig:013]):

![Примеры работы с матрицами большой размерности и специальной структуры](image/13.png){ #fig:013 width=100% height=100% }

Пример добавления шума в симметричную матрицу (матрица уже не будет симметричной) (рис. [-@fig:014]):

![Пример добавления шума в симметричную матрицу](image/14.png){ #fig:014 width=100% height=100% }

В Julia можно объявить структуру матрица явно, например, используя Diagonal, Triangular, 
Symmetric, Hermitian, Tridiagonal и SymTridiagonal (рис. [-@fig:015]):

![Пример явного объявления структуры матрицы](image/15.png){ #fig:015 width=100% height=100% }

Далее для оценки эффективности выполнения операций над матрицами большой размерности и специальной 
структуры воспользуемся пакетом BenchmarkTools (рис. [-@fig:016]):

![Использование пакета BenchmarkTools](image/16.png){ #fig:016 width=100% height=100% }

Далее рассмотрим примеры работы с разряженными матрицами большой размерности.

Использование типов Tridiagonal и SymTridiagonal для хранения трёхдиагональных матриц позволяет 
работать с потенциально очень большими трёхдиагональными матрицами (рис. [-@fig:017]):

![Примеры работы с разряженными матрицами большой размерности](image/17.png){ #fig:017 width=100% height=100% }

## Общая линейная алгебра

В примере показано, как можно решить систему линейных уравнений с рациональными элементами 
без преобразования в типы элементов с плавающей запятой (для избежания проблемы с переполнением используем BigInt) (рис. [-@fig:018]):

![Решение системы линейных уравнений с рациональными элементами без преобразования в типы элементов с плавающей запятой](image/18.png){ #fig:018 width=100% height=100% }

## Самостоятельная работа

Выполнение задания "Произведение векторов" (рис. [-@fig:019]):

![Решение задания "Произведение векторов"](image/19.png){ #fig:019 width=100% height=100% }

Выполнение задания "Системы линейных уравнений" (рис. [-@fig:020] - рис. [-@fig:021]):

![Решение задания "Системы линейных уравнений"](image/20.png){ #fig:020 width=100% height=100% }

![Решение задания "Системы линейных уравнений"](image/21.png){ #fig:021 width=100% height=100% }

![Решение задания "Системы линейных уравнений"](image/22.png){ #fig:022 width=100% height=100% }

![Решение задания "Системы линейных уравнений"](image/23.png){ #fig:023 width=100% height=100% }

Выполнение задания "Операции с матрицами" (рис. [-@fig:022] - рис. [-@fig:026]):

![Решение задания "Операции с матрицами"](image/24.png){ #fig:024 width=100% height=100% }

![Решение задания "Операции с матрицами"](image/25.png){ #fig:025 width=100% height=100% }

![Решение задания "Операции с матрицами"](image/26.png){ #fig:026 width=100% height=100% }

Выполнение задания "Линейные модели экономики" (рис. [-@fig:027]):

![Решение задания "Линейные модели экономики"](image/27.png){ #fig:027 width=100% height=100% }

# Вывод

В ходе выполнения лабораторной работы были изучены возможности специализированных пакетов Julia 
для выполнения и оценки эффективности операций над объектами линейной алгебры.


# Список литературы{.unnumbered}

::: {#refs}
:::