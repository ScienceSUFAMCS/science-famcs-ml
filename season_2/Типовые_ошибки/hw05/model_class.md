---
code: hw05.model_class
hw: hw05
title: Модель не собрана в класс
severity: major
detector: rule
---
**Что не так.** Нет класса `MyLogisticRegressionGD`.

**Почему это важно.** Задание требовало собрать разрозненные функции в объект
с интерфейсом `fit`/`predict`/`predict_proba` — тем же, что у scikit-learn.
Это и делает модель пригодной к использованию в пайплайне.

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Оптимизация в ML](https://education.yandex.ru/handbook/ml/article/optimizaciya-v-ml)
