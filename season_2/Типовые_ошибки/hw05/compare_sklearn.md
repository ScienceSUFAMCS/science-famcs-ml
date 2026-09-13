---
code: hw05.compare_sklearn
hw: hw05
title: Нет сравнения со scikit-learn
severity: major
detector: rule
---
**Что не так.** Не обучена `LogisticRegression` из sklearn и/или нет сводной
таблицы сравнения.

**Почему это важно.** Это проверка правильности вашей реализации: если метрики
сильно расходятся, значит где-то ошибка в градиенте или в обучении. Заодно
видно, почему библиотечная версия быстрее — она использует не простой
градиентный спуск, а методы второго порядка (lbfgs, newton-cg).

**Почитать:**
- [Линейные модели](https://education.yandex.ru/handbook/ml/article/linear-models)
- [Метрики классификации и регрессии](https://education.yandex.ru/handbook/ml/article/metriki-klassifikacii-i-regressii)
