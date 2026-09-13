---
code: common.fit_on_test
hw: common
title: Преобразование обучено на тестовой выборке
severity: critical
detector: rule
kind: methodology
---
**Что не так.** На тесте вызван `fit` или `fit_transform` вместо `transform`.
Типовая строка: `X_test_scaled = scaler.fit_transform(X_test)`.

**Почему это важно.** Тест перестаёт быть тестом. Признаки теста
масштабируются по его собственным среднему и дисперсии, то есть модель
получает данные в другой системе координат, чем при обучении, — и одновременно
вы используете статистику теста, которую в реальности знать не могли. Оценка
качества становится недостоверной в обе стороны.

**Как надо.** На тесте — только `transform`, объект уже обучен на train:

```python
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)     # без fit
```

**Почитать:**
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
- [sklearn: Pipeline и утечки](https://scikit-learn.org/stable/common_pitfalls.html#data-leakage)
