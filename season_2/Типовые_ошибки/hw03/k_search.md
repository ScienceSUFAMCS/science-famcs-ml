---
code: hw03.k_search
hw: hw03
title: Нет подбора числа соседей
severity: major
detector: rule
---
**Что не так.** Значение `k` взято наугад, без перебора и графика качества.

**Почему это важно.** `k` управляет компромиссом смещения и разброса: при `k=1`
модель переобучается и повторяет шум, при слишком большом `k` — сглаживает
всё до предсказания самого частого класса.

**Как надо.**

```python
scores = []
for k in range(1, 31):
    scores.append(cross_val_score(
        KNeighborsClassifier(n_neighbors=k), X_train_s, y_train, cv=5).mean())
plt.plot(range(1, 31), scores); plt.xlabel("k"); plt.ylabel("accuracy")
```

**Почитать:**
- [Задание HW03](rubrics/tasks/hw03.md)
- [Метрические методы](https://education.yandex.ru/handbook/ml/article/metricheskiye-metody)
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
