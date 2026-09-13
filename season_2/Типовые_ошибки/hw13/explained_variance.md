---
code: hw13.explained_variance
hw: hw13
title: Нет объяснённой дисперсии
severity: major
detector: rule
---
**Что не так.** Не выведен `explained_variance_ratio_`.

**Почему это важно.** Это единственный способ понять, сколько информации осталось после сжатия и сколько компонент имеет смысл брать.

**Почитать:**
- [sklearn: PCA](https://scikit-learn.org/stable/modules/decomposition.html#pca)
- [Слайды лекции по снижению размерности](materials/pca_slides.pdf)
