---
code: hw12.silhouette
hw: hw12
title: Нет силуэта
severity: major
detector: rule
---
**Что не так.** Не посчитан `silhouette_score`.

**Почему это важно.** Нужна численная мера, чтобы сравнить разбиения. Для DBSCAN силуэт обычно считают без шумовых точек, иначе метка -1 портит оценку.

**Почитать:**
- [Кластеризация](https://education.yandex.ru/handbook/ml/article/klasterizaciya)
