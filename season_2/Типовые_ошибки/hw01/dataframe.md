---
code: hw01.dataframe
hw: hw01
title: Нет DataFrame с базовым обзором
severity: major
detector: rule
---
**Что не так.** Матрица не завёрнута в `DataFrame` с осмысленными названиями
колонок, либо не показаны `head()`, `shape`, `describe()` и проверка пропусков.

**Почему это важно.** Это минимальный набор действий, с которого начинается
работа с любыми табличными данными.

**Как надо.**

```python
df = pd.DataFrame(X, columns=[f"feature_{i}" for i in range(X.shape[1])])
df["target"] = y
df.head(); df.shape; df.describe(); df.isnull().sum()
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [pandas: describe](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)
