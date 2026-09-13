---
code: common.split_without_seed
hw: common
title: Разбиение выборки не зафиксировано
severity: major
detector: rule
kind: methodology
---
**Что не так.** В `train_test_split` не указан `random_state`.

**Почему это важно.** При каждом запуске выборка делится заново, и все числа в
ноутбуке меняются. Вывод «моя реализация показала 0.9912, библиотечная — 0.9825»
перестаёт что-либо значить: разница такого размера может целиком объясняться
другим разбиением, а не качеством моделей. Сравнивать модели можно только на
одном и том же разбиении.

**Как надо.**

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)
```

`stratify=y` заодно сохранит доли классов — при дисбалансе это важно.

**Почитать:**
- [Кросс-валидация](https://education.yandex.ru/handbook/ml/article/kross-validaciya)
