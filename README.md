# Основы Git
*Задание для курса [Яндекс Практикум](https://practicum.yandex.ru/) "Основы работы с Git".*
## Зачем нужен Git?
Git позволяет отслеживать изменения в файлах. Свою информацию Git хранит в репозитории (хранилище).
После создания репозитория можно с помощью специальных команд фиксировать состояние отслеживаемых файлов, а затем просматривать изменения. При каждой фиксации можно добавлять комментарий, а при необхоимости можно восстановить состояние файлов в одно из зафиксированных состояний.

Зафиксированное состояние называется коммитом (commit). Коммиты создаются на ветках. В репозитории всегда есть основная ветка (master или main) и могут быть дополнительные.

Git относится к классу программ version control system (VCS) и его особенно удобно использовать для отслеживания изменений в текстовых файлах, например, программном коде. При работе с текстовыми файлами Git может показывать не только какие файлы изменились, но и построчные изменения в каждом файле.
## Как создать локальный репозиторий?
Для того, чтобы начать отслеживать изменения в папке надо создать репозиторий Git. Для этого надо перейти а папку и выполнить команду
``` bash
git init
```
Для указания файлов и папок, которые надо отслеживать, надо выполнить команду
``` bash
git add <имя файла>
```
или, чтобы добавить все файлы в папке
``` bash
git add .
```
Для просмотра статуса файлов (добавлен/изменён/удалён) и статуса отслеживания используется команда
``` bash
git status
```
Для фиксации изменений используется команда
``` bash
git commit
```
Для просмотра истории фиксаций используется команда
```bash
git log
```
## Цикл работы с локальным репозиторием.
Обычный цикл работы с Git после созданя репозитория выглядит следующим образом.
1. Создание/изменение файлов
2. Просмотр изменившихся файлов
``` bash
git status
```
3. Добавление файлов в список отслеживания
``` bash
git add 
```
4. После приведения файлов в состояние, которое хотим зафиксировать
``` bash
git commit
```
## Что такое GitHub?
[GitHub](https://github.com/) - это Web2 приложение (портал), которое позволяет создавать удалённые репозитории. 
После связывания локального и удалённого репозиториев, появлеятся возможность синхронизировать содержимое репозиториев. Это позволяет разным людям работать через Интернет с одним репозиторием. 
## Как создать удалённый репозиторий?
Для создания удалённого репозитория на [GitHub](https://github.com/) необходимо выполнить следующие шаги:
1. Открыть страницу Dashboard
2. Нажать кнопку `New`
3. Указать имя репозитория в поле `Repository name`
4. Выбрать тип репозитория: публичный или приватный и установить соответствующий переключатель
5. Нажать кнопку `Create Repository`
## Как связать локальный и удалённый репозитории?
После создания репозитория в голубом блоке будет указан адрес удалённого репозитория. Адрес будет начинаться с git@github.com:

Для установления связи локального и удалённого репозиториев необходимо выполнить команды
``` bash
git remote add origin <адрес удалённого репозитория>
git push -u origin main
```
После этого закомиченные изменения отправляются в удалённый репозиторий командой 
```
git push
```

