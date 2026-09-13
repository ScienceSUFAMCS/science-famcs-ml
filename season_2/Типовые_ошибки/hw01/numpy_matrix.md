---
code: hw01.numpy_matrix
hw: hw01
title: Нет случайной матрицы и статистик по осям
severity: major
detector: rule
---
**Что не так.** Не создана случайная матрица 100×5 или не посчитаны статистики
по столбцам через `axis=0`.

**Почему это важно.** Задание проверяет понимание того, что в NumPy операции
идут вдоль осей. Путаница между `axis=0` (по столбцам) и `axis=1` (по строкам) —
источник огромного числа ошибок в дальнейшем.

**Как надо.**

```python
X = np.random.default_rng(42).random((100, 5))
print(X.mean(), X.std())              # по всей матрице
print(X.mean(axis=0), X.std(axis=0))  # по каждому столбцу -> 5 чисел
```

**Почитать:**
- [Задание HW01](rubrics/tasks/hw01.md)
- [NumPy: векторизация и broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html)
