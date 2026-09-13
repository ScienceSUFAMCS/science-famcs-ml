---
code: hw05.log_loss
hw: hw05
title: Не реализован log-loss
severity: major
detector: rule
---
**Что не так.** Нет функции `compute_log_loss`.

**Почему это важно.** Это то, что модель минимизирует. MSE для классификации
не годится: с сигмоидой он даёт невыпуклую задачу и слабые градиенты при
уверенно неверных ответах, тогда как log-loss штрафует их резко.

**Как надо.** Обязательно с клиппингом, иначе `log(0)` даст `-inf`:

```python
def compute_log_loss(y_true, p):
    p = np.clip(p, 1e-15, 1 - 1e-15)
    return -np.mean(y_true * np.log(p) + (1 - y_true) * np.log(1 - p))
```

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Оптимизация в ML](https://education.yandex.ru/handbook/ml/article/optimizaciya-v-ml)
