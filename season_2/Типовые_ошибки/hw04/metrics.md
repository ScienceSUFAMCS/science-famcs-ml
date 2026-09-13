---
code: hw04.metrics
hw: hw04
title: Не хватает метрик регрессии
severity: major
detector: rule
---
**Что не так.** Посчитана одна метрика или ни одной.

**Почему это важно.** R² говорит, какую долю дисперсии объяснила модель,
но не даёт представления о величине ошибки в единицах таргета. RMSE даёт
ошибку в тех же единицах и сильнее штрафует крупные промахи, MAE устойчивее
к выбросам. Задание требовало обосновать выбор.

**Как надо.**

```python
print("R2  ", r2_score(y_test, pred))
print("RMSE", mean_squared_error(y_test, pred) ** 0.5)
print("MAE ", mean_absolute_error(y_test, pred))
```

**Почитать:**
- [Задание HW04](rubrics/tasks/hw04.md)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
