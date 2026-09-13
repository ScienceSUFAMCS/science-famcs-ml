---
code: hw02.plot_kinds
hw: hw02
title: Не хватает обязательных типов графиков
severity: major
detector: rule
---
**Что не так.** Нет одного или нескольких обязательных графиков: гистограммы,
scatter, boxplot, bar/count, heatmap корреляций.

**Почему это важно.** Каждый отвечает на свой вопрос: гистограмма — про форму
распределения, scatter — про связь двух чисел, boxplot — про выбросы,
countplot — про баланс категорий, heatmap — про мультиколлинеарность.
Пропустив тип графика, вы пропускаете вопрос.

**Как надо.** Построить все пять и под каждым написать, что он показал.

**Почитать:**
- [Задание HW02 (чек-лист EDA)](rubrics/tasks/hw02.md)
- [ODS: визуализация данных в Python](https://habr.com/ru/companies/ods/articles/323210/)
- [seaborn: распределения](https://seaborn.pydata.org/tutorial/distributions.html)
