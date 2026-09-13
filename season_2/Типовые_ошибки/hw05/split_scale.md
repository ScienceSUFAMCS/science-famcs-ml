---
code: hw05.split_scale
hw: hw05
title: Не сделан шаг 1: разделение и стандартизация
severity: major
detector: rule
---
**Что не так.** Нет `train_test_split` и/или `StandardScaler`.

**Почему это важно.** Стандартизация здесь не косметика: вы обучаете модель
градиентным спуском вручную. Если признаки в разном масштабе, поверхность
функции потерь вытянута, и с общим шагом обучения спуск либо расходится, либо
ползёт бесконечно медленно.

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Оптимизация в ML](https://education.yandex.ru/handbook/ml/article/optimizaciya-v-ml)
