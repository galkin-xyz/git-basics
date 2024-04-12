# Основы Git

## Зачем нужен Git?

## Как создать локальный репозиторий?

## Цикл работы с локальным репозиторием.

## Что такое GitHub?

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
```
git remote add origin <*адрес удалённого репозитория*>
git push -u origin main
```
После этого закомиченные изменения отправляются в удалённый репозиторий командой 
```
git push
```

