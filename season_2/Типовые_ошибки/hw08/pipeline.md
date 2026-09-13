---
code: hw08.pipeline
hw: hw08
title: Масштабирование не через Pipeline
severity: major
detector: rule
---
**Что не так.** `StandardScaler` применён руками, а не внутри `Pipeline`.

**Почему это важно.** При `GridSearchCV` масштабирование должно переобучаться
на каждом фолде. Если сделать его один раз до кросс-валидации, статистика
валидационной части протечёт в обучение, и подобранные C и gamma окажутся
завышенно оптимистичными.

**Как надо.** `make_pipeline(StandardScaler(), SVC())` и уже его в `GridSearchCV`.

**Почитать:**
- [sklearn: SVM](https://scikit-learn.org/stable/modules/svm.html)
- [Слайды лекции по SVM](materials/svm_slides.pdf)
