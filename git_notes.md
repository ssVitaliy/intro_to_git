# GIT NOTES

## Конфигурация GIT-а

Вывод списка переменных конфигурации:
```sh
git config --list
```

Заполнение Имени ползователя и емайл
```sh
git config --global user.name "Name"
git config --global user.email "user@email.com"
```

Флаг *--global* используется для задания конфигурации для пользователя.  
Флаг *--local* для текущего репозитория (хранится в *.git/config*)  
Флаг *--system* для всей машины.

## Инициализация репы

Для инициализации нового репозитория в каталоге с проектом выполнить:
```sh
git init
```

## Просмотр статуса

```sh
git status
```

## Добавление файлов

```sh
git add
```

## Очистить список добавленных файлов

```sh
git restore --staged File.Name
```
или

```sh
git reset
```

## Коммит

```sh
git commit -m "message"
```
Вызов команды без флага `-m` откроет текстовый редактор по умолчанию.

## Изменение комментария локального коммита

```sh
git commit --amend
```

## Просмотр истории коммитов

```sh
git log
```

## Переключение между коммитами

```sh
git checkout commit_hash
```

## Просмотр различий

```sh
git diff
```

## Удаление последних коммитов

Удалить 1 последний:
```sh
git reset --hard HEAD^
```
Для удаления 2х последних `HEAD~2`


# Ветки (Branches)

## Создание ветки

```sh
git branch <branch_name>
```

Создание ветки с переходом на неё:
```sh
git checkout -b ＜new-branch＞
```

## Переключение между ветками

```sh
git switch ＜branch_name＞ # New style
git checkout ＜branch_name＞ # Old style
```

## Удаление ветки

Безопасное удаление:
```sh
git branch -d <branch_name>
```
Жесткое удаление:
```sh
git branch -D <branch_name>
```

## Переименование ветки

```sh
git branch -m <branch>
```

## Слияние веток

Перейти в ветку **main** (в ту, **в которую необходимо** смержить), затем сделать слияние командой:
```sh
git merge <branch_name>
```

# Удаленные репозитории (remote rep's)
