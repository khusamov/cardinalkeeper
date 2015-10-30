
Cardinal Keeper 2015
====================

Небольшая программа управления собственным предприятием.

Версии программы:

http://semver.org/lang/ru/

Учитывая номер версии МАЖОРНАЯ.МИНОРНАЯ.ПАТЧ, следует увеличивать:

МАЖОРНУЮ версию, когда сделаны обратно несовместимые изменения API.
МИНОРНУЮ версию, когда вы добавляете новый функционал, не нарушая обратной совместимости.
ПАТЧ-версию, когда вы делаете обратно совместимые исправления.
Дополнительные обозначения для предрелизных и билд-метаданных возможны как дополнения к МАЖОРНАЯ.МИНОРНАЯ.ПАТЧ формату.

Инсталяция:
===========

## Первый этап:

Установка Node.js:

```
nvm ls-remote
nvm install v4.1.2
nvm use v4.1.2
nvm alias default v4.1.2
```

Установка пакетов:

```
npm install cardinalkeeper --save
bower install khusamov-extjs --save
bower install pace#~1.0.2 --save
bower cache clean
```

Вариант:

> `bower install ./node_modules/cardinalkeeper/ --save`

пока не катит, так как копирует и всю серверную часть в `bower_components`, 
чего и следовало ожидать судя по документации на команду 
`bower install <папка>`.

## Второй этап:

После установки пакетов нужно создать следующие файлы:

###.gitignore

```
npm-debug.log  
node_modules  
bower_components  
temp
```

###<название вашего проекта>.ini

###<название вашего проекта>.js


Глоссарий:
==========

Приложение

Экземпляр приложения может быть только один

Модуль приложения - на основе модуля Node.js

Модулей в приложении может быть сколько угодно

Ресурс модуля

Ресурсов в модуле можно быть сколько угодно

Роль приложения в базе данных одна

public схема приложения в базе данных

Имя модуля = схеме модуля в базе данных

На один модуль выделяется одна схема в базе данных

В главном меню для каждого модуля выделяется одно корневое меню

В конфиге для каждого модуля выделяется один раздел

В конфиге для приложения выделяется раздел application

Права доступа создаются в СУБД, дополнительные права - в приложении

