---
code: hw05.gradient_step
hw: hw05
title: Не реализован шаг градиентного спуска
severity: major
detector: rule
---
**Что не так.** Нет функции `forward_backward`.

**Почему это важно.** Это ядро задания: понять, что обучение — это повторяющийся
расчёт градиента и сдвиг весов против него.

**Как надо.** Для логистической регрессии градиент выходит удивительно простым:

```python
def forward_backward(X, y, w, b):
    p = sigmoid(X @ w + b)
    dw = X.T @ (p - y) / len(y)
    db = (p - y).mean()
    return compute_log_loss(y, p), dw, db
```

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Оптимизация в ML](https://education.yandex.ru/handbook/ml/article/optimizaciya-v-ml)
