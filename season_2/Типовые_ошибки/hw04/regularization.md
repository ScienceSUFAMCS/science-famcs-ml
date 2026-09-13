---
code: hw04.regularization
hw: hw04
title: Нет регуляризации
severity: major
detector: rule
---
**Что не так.** Обучена только обычная линейная регрессия, Ridge/Lasso не
пробовали.

**Почему это важно.** Задание разбирало проблему мультиколлинеарности: когда
признаки линейно зависимы, матрица `XᵀX` вырождена, коэффициенты МНК
разлетаются до огромных значений и становятся неустойчивыми. Ridge добавляет
`α‖w‖²` и лечит именно это; Lasso вдобавок зануляет часть коэффициентов
и работает как отбор признаков.

**Как надо.**

```python
for alpha in [0.01, 0.1, 1, 10, 100]:
    m = make_pipeline(StandardScaler(), Ridge(alpha=alpha))
    print(alpha, cross_val_score(m, X_train, y_train, cv=5, scoring="r2").mean())
```

**Почитать:**
- [Задание HW04](rubrics/tasks/hw04.md)
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
