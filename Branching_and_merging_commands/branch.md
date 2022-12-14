## Работа с ветками
---

* ___<h3>Просмотр списка веток</h3>___

Можно просматривать полный список веток, используя параметр `branch`. Команда отобразит все ветки, отметит текущую звёздочкой (*) и выделит её цветом.

```bash-
git branch
```

Также можно вывести список удалённых веток с помощью флага `-a`.

```bash-
git branch -a
```

---
* ___<h3>Создание новой ветки и переход в неё</h3>___


Создать новую ветку можно с помощью параметра `branch`, указав имя ветки.

```bash-
git branch new_branch_name
```

**Но Git не переключится на неё автоматически.** Для автоматического перехода нужно добавить флаг `-b` и параметр `checkout`.

```bash-
git checkout -b new_branch_name
```

---
* ___<h3>Удаление ветки</h3>___


Удалить ветку можно параметром `branch` с добавлением флага `-d` и указанием имени ветки. Если вы завершили работу над веткой и объединили её с основной, можно её удалить без потери истории. Однако, если выполнить команду удаления до слияния — *в результате появится сообщение об ошибке*. Этот защитный механизм предотвращает потерю доступа к файлам.

```bash-
git branch -d existing_branch_name
```

Для принудительного удаления ветки используется флаг `-D` с заглавной буквой. **В этом случае ветка будет удалена независимо от текущего статуса, без предупреждений.**

```bash-
git branch -D existing_branch_name
```

_Вышеуказанные команды удаляют только локальную копию ветки. В удалённом репозитории она может сохраниться. Если хотите стереть удалённую ветку, выполните следующую команду:_
```bash-
git push origin --delete existing_branch_name
```
[Подробнее о команде push](../collaboration_and_updates_commands/push.md) 

[<-На главную страницу](../readme.md)