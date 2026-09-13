---
code: hw08.boundary
hw: hw08
title: Не построена граница решений
severity: major
detector: rule
---
**Что не так.** Нет визуализации разделяющей поверхности на двух признаках.

**Почему это важно.** Это то, ради чего SVM изучают: увидеть, как ядро меняет
форму границы. Линейное ядро даёт прямую, RBF — произвольно изогнутую
поверхность.

**Почитать:**
- [sklearn: SVM](https://scikit-learn.org/stable/modules/svm.html)
- [Слайды лекции по SVM](materials/svm_slides.pdf)
