---
code: common.no_seed
hw: common
title: Не зафиксирован seed
severity: minor
detector: rule
kind: methodology
---
**Что не так.** Нигде не задан `random_state` или `np.random.seed`.

**Почему это важно.** Разбиение выборки, инициализация моделей и подвыборки
в ансамблях зависят от случайности. Без фиксации при следующем запуске получатся
другие числа, и вывод «модель A лучше модели B на 0.01» может развалиться.
Воспроизводимость — базовое требование к эксперименту.

**Как надо.** Задавать `random_state` везде, где он есть:

```python
RANDOM_STATE = 42
np.random.seed(RANDOM_STATE)

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=RANDOM_STATE
)
model = RandomForestRegressor(n_estimators=200, random_state=RANDOM_STATE)
```

**Почитать:**
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
