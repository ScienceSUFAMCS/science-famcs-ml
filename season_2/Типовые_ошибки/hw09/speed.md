---
code: hw09.speed
hw: hw09
title: Не сравнивалась скорость обучения
severity: major
detector: rule
---
**Что не так.** Не измерено время обучения дерева и леса.

**Почему это важно.** Пункт задания. Лес из 100 деревьев учится примерно в 100
раз дольше одного — но деревья независимы, и это единственный ансамбль, который
честно распараллеливается. Отсюда и вопрос задания «можно ли добиться близкой
скорости»: ответ — `n_jobs=-1`.

**Как надо.**

```python
import time
t = time.perf_counter(); tree.fit(X_train, y_train); print("дерево", time.perf_counter()-t)
t = time.perf_counter(); rf.fit(X_train, y_train);   print("лес   ", time.perf_counter()-t)
```

**Почитать:**
- [Задание HW09](rubrics/tasks/hw09.md)
- [Ансамбли в машинном обучении](https://education.yandex.ru/handbook/ml/article/ansambli-v-mashinnom-obuchenii)
