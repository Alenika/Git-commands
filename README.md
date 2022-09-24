# Git-commands
Шпаргалка по основным командам

## Первоначальная настройка

**$ git config --global user.name "[имя]"** - устанавливает имя, которое будет отображаться в поле автора у выполняемых вами коммитов

**$ git config --global user.email "[адрес электронной почты]"** - устанавливает адрес электронной почты, который будет отображаться в информации о выполняемых вами коммитах

## Создание репозитория

**$ git init [название проекта]** - cоздаёт новый локальный репозиторий с заданным именем

**$ git clone [url-адрес]** - cкачивает репозиторий вместе со всей его историей изменений

## Внесение изменений

**$ git status** - перечисляет все новые или изменённые файлы, которые нуждаются в фиксации

**$ git add [файл]** - индексирует указанный файл для последующего коммита

**$ git reset [файл]** -отменяет индексацию указанного файла, при этом сохраняет его содержимое

**$ git commit -m "[сообщение с описанием]"** - фиксирует проиндексированные изменения и сохраняет их в историю версий

## Коллективная работа

**$ git branch** - cписок именованных веток коммитов с указанием выбранной ветки

**$ git branch [имя ветки]** - cоздаёт новую ветку

**$ git switch -c [имя ветки]** - переключается на выбранную ветку и обновляет рабочую директорию до её состояния

**$ git merge [имя ветки]** - вносит изменения указанной ветки в текущую ветку

**$ git branch -d [имя ветки]** - уаляет выбранную ветку

## Просмотр истории

**$ git log** - история коммитов для текущей ветки

**$ git log --follow [файл]** - история изменений конкретного файла, включая его переименование

## Откат коммитов

**$ git reset [коммит]** - отменяет все коммиты после заданного, оставляя все изменения в рабочей директории

**$ git reset --hard [коммит]** - сбрасывает всю историю вместе с состоянием рабочей директории до указанного коммита

## Синхронизация с удалённым репозиторием

**$ git fetch [удалённый репозиторий]** - cкачивает всю историю из удалённого репозитория

**$ git merge [удалённый репозиторий]/[ветка]** - вносит изменения из ветки удалённого репозитория в текущую ветку локального репозитория

**$ git push [удалённый репозиторий] [ветка]** - загружает все изменения локальной ветки в удалённый репозиторий

**$ git pull** - загружает историю из удалённого репозитория и объединяет её с локальной. pull = fetch + merge

## Контроль отображения записей

**git log --pretty=oneline --max-count=2**

**git log --pretty=oneline --since='5 minutes ago'**

**git log --pretty=oneline --until='5 minutes ago'**

**git log --pretty=oneline --author=<your name>**

**git log --pretty=oneline --all**

## Создание тегов версий

**git tag <tag name>** - создать тег

**git tag** - увидеть, какие теги доступны

**git checkout "tag name"** - переключаться между отмеченными версиями

**git hist master --all** - посмотреть теги в логе
