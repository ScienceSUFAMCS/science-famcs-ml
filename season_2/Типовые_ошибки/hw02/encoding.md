---
code: hw02.encoding
hw: hw02
title: Нет кодирования категориальных признаков
severity: major
detector: rule
---
**Что не так.** Не применён ни `pd.get_dummies`, ни `OneHotEncoder` — при том
что это обязательный пункт задания.

**Почему это важно.** Модели работают с числами. Категории надо превратить в
числа так, чтобы не появился ложный порядок: если закодировать `Petrol=0,
Diesel=1, CNG=2`, линейная модель решит, что CNG «больше» Petrol в два раза.
One-hot этой проблемы лишён.

**Как надо.**

```python
df_enc = pd.get_dummies(df, columns=["FuelType"], drop_first=True)
# или, если нужен объект для переиспользования на тесте:
enc = OneHotEncoder(handle_unknown="ignore", sparse_output=False)
```

**Почитать:**
- [Задание HW02 (чек-лист EDA)](rubrics/tasks/hw02.md)
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
