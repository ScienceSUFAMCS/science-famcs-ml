---
code: hw01.pandas_ops
hw: hw01
title: Нет осмысленных операций pandas
severity: major
detector: rule
---
**Что не так.** Не показаны фильтрация, сортировка или группировка.

**Почему это важно.** Задание проверяет владение базовым инструментом:
без уверенного `groupby`/`query` любой EDA превращается в мучение.

**Как надо.**

```python
df[df["target"] > 0].sort_values("feature_0", ascending=False).head()
df.groupby(pd.cut(df["feature_0"], 3))["target"].mean()
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [pandas за 10 минут](https://pandas.pydata.org/docs/user_guide/10min.html)
- [ODS: первичный анализ данных с Pandas](https://habr.com/ru/companies/ods/articles/322626/)
