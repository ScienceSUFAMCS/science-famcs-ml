---
code: hw02.three_libs
hw: hw02
title: Использованы не все три библиотеки визуализации
severity: major
detector: rule
---
**Что не так.** Задание требовало осмысленно применить matplotlib, seaborn и
plotly. Использованы не все.

**Почему это важно.** У каждой своя ниша: matplotlib даёт полный контроль,
seaborn коротко строит статистические графики, plotly — интерактив с
подсказками при наведении, что удобно для поиска конкретных выбросов.

**Как надо.**

```python
df["Price"].plot(kind="hist", bins=40)                    # matplotlib
sns.boxplot(data=df, x="FuelType", y="Price")             # seaborn
px.scatter(df, x="KM", y="Price", color="FuelType",
           hover_data=["Age"])                            # plotly
```

**Почитать:**
- [Задание HW02 (чек-лист EDA)](rubrics/tasks/hw02.md)
- [ODS: визуализация данных в Python](https://habr.com/ru/companies/ods/articles/323210/)
- [plotly express](https://plotly.com/python/plotly-express/)
