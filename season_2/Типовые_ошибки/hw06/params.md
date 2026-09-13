---
code: hw06.params
hw: hw06
title: Не оценены параметры распределений по классам
severity: major
detector: rule
---
**Что не так.** Нет функции `fit_gaussian_params`.

**Почему это важно.** Гауссовский наивный Байес описывает каждый признак внутри
каждого класса нормальным распределением. Обучение модели и есть подсчёт
среднего и дисперсии по каждому признаку в каждом классе.

**Почитать:**
- [Генеративный подход к классификации](https://education.yandex.ru/handbook/ml/article/generativnyj-podhod-k-klassifikacii)
- [Как оценивать вероятности](https://education.yandex.ru/handbook/ml/article/kak-ocenivat-veroyatnosti)
