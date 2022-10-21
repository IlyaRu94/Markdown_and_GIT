## Просмотр изменений до коммита
---

Можно просматривать список изменений, внесённых в репозиторий, используя параметр `diff`. <i>По умолчанию отображаются только изменения, не подготовленные для фиксации.</i>

```bash-
git diff
```

Для просмотра подготовленных изменений необходимо добавить флаг `--staged`.

```bash-
git diff --staged
```

Также можно указать имя файла как параметр и просмотреть изменения, внесённые только в этот файл.

```bash-
git diff Your_file.md
```
[<center>На главную страницу</center>](../readme.md)