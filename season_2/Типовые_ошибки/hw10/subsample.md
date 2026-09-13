---
code: hw10.subsample
hw: hw10
title: Не добавлен параметр subsample
severity: major
detector: rule
---
**Что не так.** В свою реализацию не добавлен `subsample`.

**Почему это важно.** Обучение каждого дерева на случайной доле объектов
(стохастический градиентный бустинг) вносит разнообразие: деревья становятся
менее скоррелированными, дисперсия ансамбля падает, переобучение снижается.

**Как надо.**

```python
idx = rng.choice(len(X), size=int(self.subsample * len(X)), replace=False)
tree.fit(X[idx], antigrad[idx])
```

**Почитать:**
- [Задание HW10](rubrics/tasks/hw10.md)
- [Градиентный бустинг](https://education.yandex.ru/handbook/ml/article/gradientnyj-busting)
