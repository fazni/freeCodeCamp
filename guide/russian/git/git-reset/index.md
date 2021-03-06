---
title: Git Reset
localeTitle: Git Reset
---
## Git Reset

Команда `git reset` позволяет перевести текущую головку в указанное состояние. Вы можете сбросить состояние определенных файлов, а также всю ветвь.

### Сбросить файл или набор файлов

Следующая команда позволяет выборочно выбирать фрагменты контента и возвращать или не выполнять его.

```shell
git reset (--patch | -p) [tree-ish] [--] [paths] 
```

### Выровнять файл

Если вы переместили файл в промежуточную область с `git add` , но больше не хотите, чтобы он был частью коммита, вы можете использовать `git reset` для того, чтобы отключить этот файл:

```shell
git reset HEAD FILE-TO-UNSTAGE 
```

Изменения, которые вы внесли, по-прежнему будут в файле, эта команда просто удаляет этот файл из вашей промежуточной области.

### Сбросьте ветвь на предыдущую фиксацию

Следующая команда сбрасывает HEAD вашего текущего филиала в данный `COMMIT` и обновляет индекс. Он в основном перематывает состояние вашего филиала, а затем все фиксируют, что вы делаете переписку над всем, что появилось после точки сброса. Если вы опустите `MODE` , по умолчанию используется `--mixed` :

```shell
git reset MODE COMMIT 
```

Опции `MODE` :

*   `--soft` : не сбрасывает индексный файл или рабочее дерево, но сбрасывает HEAD для `commit` . Изменяет все файлы на «Изменения, которые необходимо совершить»
*   `--mixed` : сбрасывает индекс, но не рабочее дерево, и сообщает, что не обновлялось
*   `--hard` : сбрасывает индекс и рабочее дерево. Любые изменения в отслеживаемых файлах в рабочем дереве с момента `commit` отбрасываются
*   `--merge` : сбрасывает индекс и обновляет файлы в рабочем дереве, которые отличаются между `commit` и HEAD, но сохраняет те, которые отличаются между индексом и рабочим деревом
*   `--keep` : сбрасывает записи индекса и файлы обновлений в рабочем дереве, которые отличаются между `commit` и HEAD. Если файл, который отличается от `commit` и HEAD, имеет локальные изменения, сброс отменяется

### Дополнительная информация:

*   [Сброс документации Git](https://git-scm.com/docs/git-reset)