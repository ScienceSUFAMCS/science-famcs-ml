---
code: hw01.vectorization
hw: hw01
title: Нет векторизованного умножения
severity: major
detector: rule
---
**Что не так.** Не показано умножение матрицы на вектор (`y = X @ w`).

**Почему это важно.** Векторизация — основной способ писать быстрый numpy-код.
Цикл по строкам матрицы работает в десятки раз медленнее и хуже читается.

**Как надо.**

```python
w = np.array([1.0, -2.0, 0.5, 3.0, 0.0])
y = X @ w          # вместо [sum(x*w) for x in X]
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [NumPy: векторизация и broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html)
