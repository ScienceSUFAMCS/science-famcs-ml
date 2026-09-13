---
code: hw07.prepruning
hw: hw07
title: Нет pre-pruning
severity: major
detector: rule
---
**Что не так.** Дерево обучено без ограничений глубины и размера листьев.

**Почему это важно.** Дерево без ограничений растёт до идеальной классификации
обучающей выборки: в пределе по листу на объект. Это стопроцентное
переобучение. Pre-pruning — ограничения, заданные заранее.

**Как надо.** `max_depth`, `min_samples_leaf`, `min_samples_split`, `max_leaf_nodes`.

**Почитать:**
- [Решающие деревья](https://education.yandex.ru/handbook/ml/article/reshayushchiye-derevya)
