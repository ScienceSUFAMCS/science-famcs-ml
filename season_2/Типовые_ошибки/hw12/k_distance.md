---
code: hw12.k_distance
hw: hw12
title: Нет подбора eps через k-distance plot
severity: major
detector: rule
---
**Что не так.** `eps` взят наугад.

**Почему это важно.** Есть стандартный приём: отсортировать для каждой точки
расстояние до k-го соседа и построить график. Резкий изгиб («колено») на нём и
подсказывает разумное значение `eps`.

**Как надо.**

```python
d, _ = NearestNeighbors(n_neighbors=min_samples).fit(X_s).kneighbors(X_s)
plt.plot(np.sort(d[:, -1]))
```

**Почитать:**
- [Кластеризация](https://education.yandex.ru/handbook/ml/article/klasterizaciya)
