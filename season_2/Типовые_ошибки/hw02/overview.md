---
code: hw02.overview
hw: hw02
title: Нет быстрого обзора данных
severity: major
detector: rule
---
**Что не так.** Не хватает базового блока: `head()`, `info()`, `describe()`.

**Почему это важно.** Это первое, что делают с новым датасетом: сколько строк,
какие типы, есть ли пропуски, адекватны ли диапазоны значений. Без этого любой
дальнейший анализ строится вслепую.

**Как надо.** `df.head()`, `df.tail()`, `df.shape`, `df.info()`, `df.describe()`.

**Почитать:**
- [Задание HW02 (чек-лист EDA)](rubrics/tasks/hw02.md)
- [pandas: describe](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)
