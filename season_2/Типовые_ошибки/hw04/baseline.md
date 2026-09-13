---
code: hw04.baseline
hw: hw04
title: Нет базового решения для сравнения
severity: minor
detector: rule
---
**Что не так.** Не посчитан простейший бейзлайн.

**Почему это важно.** `DummyRegressor(strategy="mean")` показывает, что даёт
предсказание средним. Если модель обгоняет его незначительно, значит она
почти ничему не научилась, каким бы ни был R².

**Как надо.**

```python
from sklearn.dummy import DummyRegressor
dummy = DummyRegressor(strategy="mean").fit(X_train, y_train)
print("baseline R2:", dummy.score(X_test, y_test))
```

**Почитать:**
- [Задание HW04](rubrics/tasks/hw04.md)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
