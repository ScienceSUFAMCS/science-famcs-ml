---
code: hw02.describe_object
hw: hw02
title: Нет describe для строковых колонок
severity: major
detector: rule
---
**Что не так.** Вызван только `df.describe()`, который по умолчанию берёт
исключительно числовые колонки.

**Почему это важно.** Категориальные признаки при этом остаются невидимыми:
не видно ни числа уникальных значений, ни самого частого. А именно там обычно
прячутся опечатки, дубли категорий («Petrol» и «petrol») и признаки с сотнями
уникальных значений, которые нельзя кодировать one-hot в лоб.

**Как надо.**

```python
df.describe(include="object")   # count, unique, top, freq
df.describe(include="all")      # всё сразу
```

**Почитать:**
- [Задание HW02 (чек-лист EDA)](rubrics/tasks/hw02.md)
- [pandas: describe](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)
