---
code: common.fit_before_split
hw: common
title: Преобразование обучено до разделения выборки
severity: major
detector: rule
kind: methodology
---
**Что не так.** Скейлер, импьютер, PCA или target encoding обучены на всём
датасете, и только потом данные разделены на train и test.

**Почему это важно.** Это утечка данных. `StandardScaler` запоминает среднее и
дисперсию, `SimpleImputer` — медиану, `TargetEncoder` — средние значения
таргета. Посчитанные по всей выборке, они содержат информацию о тесте, и модель
на тесте выглядит лучше, чем будет в реальности. На проде такой модели неоткуда
взять «среднее по будущим данным», и качество проседает. Ошибка коварна тем,
что ничего не ломает: метрики просто тихо завышаются.

**Как надо.** Сначала делим, потом учим преобразование только на train:

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=42)

scaler = StandardScaler()
X_train_s = scaler.fit_transform(X_train)   # fit только на train
X_test_s = scaler.transform(X_test)         # на тесте — только transform
```

Надёжнее собрать всё в `Pipeline`: тогда при кросс-валидации преобразование
переобучается на каждом фолде правильно и забыть об этом невозможно.

```python
pipe = make_pipeline(StandardScaler(), LogisticRegression())
cross_val_score(pipe, X, y, cv=5)
```

**Почитать:**
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
- [sklearn: Pipeline и утечки](https://scikit-learn.org/stable/common_pitfalls.html#data-leakage)
