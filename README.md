# Инструкция по работе с GIT

## Общая информация

---

**Git** — распределённая система управления версиями. Проект был создан Линусом Торвальдсом для управления разработкой ядра Linux, первая версия выпущена 7 апреля 2005 года.

Git применяется для управления версиями в рамках колоссального количества проектов по разработке ПО, как коммерческих, так и с открытым исходным кодом. Система используется множеством профессиональных разработчиков программного обеспечения.

---

## Начальная настройка

---
Перед началом работы нужно выполнить некоторые настройки, представиться GIT. Для этого нужно указать свое имя и электронную почту с помощью следующих команд:

__git config --global user.name "Your_Name"__ # указать имя, которым будут подписаны коммиты

__git config --global user.email "your_email@example"__  # указать электропочту, которая будет в описании коммитера

**git init** - создать репозиторий в текущей папке

**git init folder-name** - создать репозиторий в указанной папке

---

## Общие команды

---

__git status__ - посмотреть статус репозитория

__git add [file]__ - сделать указанный файл готовым к сохранению

__git add .__ - подготовить все файлы в папке для сохранения

__git commit -m "Message"__ - зафиксировать внесенные в файл изменения и добавить комментарий к этому сохранению

__git commit -am "Message"__ - зафиксировать внесенные изменения для всех файлов в папке

---

## Просмотр изменений

---

__git diff__  - сравнить рабочую директорию и индекс (неотслеживаемые файлы ИГНОРИРУЮТСЯ)

__git diff --color-words__  - сравнить рабочую директорию и индекс, показать отличия в словах

__git diff master feature__ - посмотреть что сделано в ветке feature по сравнению с веткой master

**git reset** - убрать из индекса все добавленные в него изменения

**git log** - показать коммиты в текущей ветке

**git log master** - показать коммиты в указанной ветке

**git log -2** - показать последние 2 коммита в активной ветке

**git log --graph -10** - показать последние 10 коммитов с ASCII-представлением ветвления

**git log --since=2.weeks** - показать коммиты за последние 2 недели

**git log --after '2018-06-30'** - показать коммиты, сделанные после указанной даты

**git log index.html** - показать историю изменений файла index.html (только коммиты)

**git checkout b9533** - переключиться на коммит с указанным хешем (переместить HEAD на указанный коммит, рабочую директорию вернуть к состоянию, на момент этого коммита)

**git checkout master**  - переключиться на коммит, на который указывает master, рабочую директорию вернуть к состоянию на момент этого коммита

---

## Работа с ветками

---

__git branch new_branch__ - создать новую ветку с указанным именем на текущем коммите

**git checkout name_branch** - перейти в указанную ветку

**git checkout -b new_branch** - создать новую ветку с указанным именем и перейти в неё

__git branch__ - показать список веток

__git merge hotfix__ - влить в ветку, в которой находимся, данные из ветки hotfix

__git merge hotfix -m "My commentary"__ - влить в ветку, в которой находимся, данные из ветки hotfix с указанием сообщения коммита слияния

__git branch -d hotfix__ - удалить ветку hotfix (используется, если её изменения уже влиты в главную ветку)

__git branch --merged__ - показать ветки, уже слитые с активной

__git branch --no-merged__ - показать ветки, не слитые с активной

__git branch -a__ - показать все имеющиеся ветки (в т.ч. на удаленных репозиториях)

**git branch -m old_branch_name new_branch_name** - переименовать локально ветку old_branch_name в new_branch_name

**git branch -m new_branch_name** - переименовать локально ТЕКУЩУЮ ветку в new_branch_name
