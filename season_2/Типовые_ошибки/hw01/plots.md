---
code: hw01.plots
hw: hw01
title: Нет гистограммы или тепловой карты корреляций
severity: major
detector: rule
---
**Что не так.** Отсутствует гистограмма признака либо heatmap корреляций.

**Почему это важно.** Распределение и связи между признаками — то, с чего
начинается понимание данных, и то, что определяет выбор модели.

**Как надо.**

```python
df["target"].hist(bins=30)
sns.heatmap(df.corr(numeric_only=True), annot=True, cmap="coolwarm")
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [ODS: визуализация данных в Python](https://habr.com/ru/companies/ods/articles/323210/)
- [matplotlib: быстрый старт](https://matplotlib.org/stable/users/explain/quick_start.html)
