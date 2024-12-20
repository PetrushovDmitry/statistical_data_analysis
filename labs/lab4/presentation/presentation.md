---
## Front matter
lang: ru-RU
title: Лабораторная работа 4
author:
  - Петрушов Дмитрий Сергеевич 1032212287
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 2024

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

## Цель лабораторной работы

- Изучить возможности специализированных пакетов Julia 
для выполнения и оценки эффективности операций над объектами линейной алгебры.

# Выполнение лабораторной работы

##  Поэлементные операции над многомерными массивами

![Поэлементные операции сложения и произведения элементов матрицы](image/1.png){ #fig:001 width=80% height=80% }

##  Поэлементные операции над многомерными массивами

![Использование возможностей пакета Statistics для работы со средними значениями](image/2.png){ #fig:002 width=80% height=80% }

## Транспонирование, след, ранг, определитель и инверсия матрицы

![Использование библиотеки LinearAlgebra для выполнения определённых операций](image/3.png){ #fig:003 width=80% height=80% }

## Транспонирование, след, ранг, определитель и инверсия матрицы

![Использование библиотеки LinearAlgebra для выполнения определённых операций](image/4.png){ #fig:004 width=80% height=80% }

## Вычисление нормы векторов и матриц, повороты, вращения

![Использование LinearAlgebra.norm(x)](image/5.png){ #fig:005 width=80% height=80% }

## Вычисление нормы векторов и матриц, повороты, вращения

![Вычисление нормы для двумерной матрицы](image/6.png){ #fig:006 width=80% height=80% }

## Матричное умножение, единичная матрица, скалярное произведение

![Примеры матричного умножения, единичной матрицы и скалярного произведения](image/7.png){ #fig:007 width=80% height=80% }

## Факторизация. Специальные матричные структуры

![Решение систем линейный алгебраических уравнений Ax = b](image/8.png){ #fig:008 width=80% height=80% }

## Факторизация. Специальные матричные структуры

![Пример вычисления LU-факторизации и определение составного типа факторизации для его хранения](image/9.png){ #fig:009 width=80% height=80% }

## Факторизация. Специальные матричные структуры

![Пример решения с использованием исходной матрицы и с использованием объекта факторизации](image/10.png){ #fig:010 width=100% height=100% }

## Факторизация. Специальные матричные структуры

![Пример вычисления QR-факторизации и определение составного типа факторизации для его хранения](image/11.png){ #fig:011 width=80% height=80% }

## Факторизация. Специальные матричные структуры

![Примеры собственной декомпозиции матрицы A](image/12.png){ #fig:012 width=80% height=80% }

## Факторизация. Специальные матричные структуры

![Примеры работы с матрицами большой размерности и специальной структуры](image/13.png){ #fig:013 width=80% height=80% }

## Факторизация. Специальные матричные структуры

![Пример добавления шума в симметричную матрицу](image/14.png){ #fig:014 width=100% height=100% }

## Факторизация. Специальные матричные структуры

![Пример явного объявления структуры матрицы](image/15.png){ #fig:015 width=100% height=100% }

## Факторизация. Специальные матричные структуры

![Использование пакета BenchmarkTools](image/16.png){ #fig:016 width=100% height=100% }

## Факторизация. Специальные матричные структуры

![Примеры работы с разряженными матрицами большой размерности](image/17.png){ #fig:017 width=80% height=80% }

## Общая линейная алгебра

![Решение системы линейных уравнений с рациональными элементами без преобразования в типы элементов с плавающей запятой](image/18.png){ #fig:018 width=80% height=80% }

## Самостоятельная работа

![Решение задания "Произведение векторов"](image/19.png){ #fig:019 width=100% height=100% }

## Самостоятельная работа

![Решение задания "Системы линейных уравнений"](image/20.png){ #fig:020 width=80% height=80% }

## Самостоятельная работа

![Решение задания "Системы линейных уравнений"](image/21.png){ #fig:021 width=80% height=80% }

## Самостоятельная работа

![Решение задания "Системы линейных уравнений"](image/22.png){ #fig:022 width=80% height=80% }

## Самостоятельная работа

![Решение задания "Системы линейных уравнений"](image/23.png){ #fig:023 width=100% height=100% }

## Самостоятельная работа

![Решение задания "Операции с матрицами"](image/24.png){ #fig:024 width=80% height=80% }

## Самостоятельная работа

![Решение задания "Операции с матрицами"](image/25.png){ #fig:025 width=100% height=100% }

## Самостоятельная работа

![Решение задания "Операции с матрицами"](image/26.png){ #fig:026 width=80% height=80% }

## Самостоятельная работа

![Решение задания "Линейные модели экономики"](image/27.png){ #fig:027 width=80% height=80% }

# Вывод

## Вывод

- В ходе выполнения лабораторной работы были изучены возможности специализированных пакетов Julia 
для выполнения и оценки эффективности операций над объектами линейной алгебры.