---
code: common.secret_in_repo
hw: common
title: В репозитории лежит ключ доступа
severity: critical
detector: rule
kind: hygiene
---
**Что не так.** В ноутбуке в открытом виде записан ключ доступа — к Kaggle,
GitHub, облаку или платному API.

**Почему это важно.** Репозиторий публичный, а история git помнит всё: даже
если удалить ключ следующим коммитом, он останется в предыдущем и его по-прежнему
можно достать. Публичный GitHub непрерывно сканируют боты, и найденные ключи
используют — чужими руками качают данные, запускают вычисления и тратят ваши
деньги.

**Что делать прямо сейчас.**

1. **Отозвать ключ.** Kaggle: Settings → API → Expire Token. GitHub: Settings →
   Developer settings → Personal access tokens → Revoke. Это первое действие;
   удаление файла без отзыва не помогает.
2. Выпустить новый ключ и хранить его вне репозитория — в `~/.kaggle/kaggle.json`
   или в переменной окружения:

```python
import os
os.environ["KAGGLE_USERNAME"] = os.getenv("KAGGLE_USERNAME")  # значение — снаружи
```

3. Добавить в `.gitignore` строки `kaggle.json`, `.env`, `*.pem`.

**Как не повторить.** Перед коммитом полезно просматривать диff: `git diff --staged`.

**Почитать:**
- [GitHub: удаление секретов из истории](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)
- [Kaggle API: настройка доступа](https://www.kaggle.com/docs/api)
