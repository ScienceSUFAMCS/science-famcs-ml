---
code: hw05.sigmoid
hw: hw05
title: Не реализована сигмоида
severity: major
detector: rule
---
**Что не так.** Нет функции `sigmoid`.

**Почему это важно.** Сигмоида переводит линейную комбинацию признаков в
интервал (0, 1), давая вероятность класса. Без неё модель предсказывает
произвольные числа, к которым неприменим log-loss.

**Как надо.** Устойчивая к переполнению версия:

```python
def sigmoid(z):
    return np.where(z >= 0, 1 / (1 + np.exp(-z)),
                    np.exp(z) / (1 + np.exp(z)))
```

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Оптимизация в ML](https://education.yandex.ru/handbook/ml/article/optimizaciya-v-ml)
