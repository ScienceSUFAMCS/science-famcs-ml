---
code: hw03.metrics_compare
hw: hw03
title: Не сравнивались метрики расстояния
severity: major
detector: rule
---
**Что не так.** Использована только метрика по умолчанию (евклидова).

**Почему это важно.** Задание требовало сравнить метрики. Выбор расстояния
меняет геометрию задачи: манхэттенское устойчивее к выбросам в отдельных
координатах, косинусное игнорирует длину вектора и полезно для текстов
и разреженных данных.

**Как надо.**

```python
for metric in ["euclidean", "manhattan", "chebyshev", "cosine"]:
    m = KNeighborsClassifier(n_neighbors=best_k, metric=metric)
    print(metric, cross_val_score(m, X_train_s, y_train, cv=5).mean())
```

**Почитать:**
- [Задание HW03](rubrics/tasks/hw03.md)
- [Метрические методы](https://education.yandex.ru/handbook/ml/article/metricheskiye-metody)
