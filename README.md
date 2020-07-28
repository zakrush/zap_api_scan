# PYTHON

Для автоматизации тестирования пишутся скрипты на python обращения к API.

Используемая версия: `python > 3.8`

**ВНИМАНИЕ!:** если zap поднимается на удаленном сервере, то чтобы достучаться до API
необходимо к API обращаться через **hostname zap**. Обращение по ip адресу не работает,
Поэтому на хосте с которого будут работать python скрипты **необходимо** прописать в `/etc/hosts` запись о хосте `zap` на котором работает API.

## Зависимости

Используются следующие библиотеки:
* `time`
* `datetime`
* `pprint`
* `zapv2`

Установка возможна через команду:
    `pip3 install -r requirements.txt`

## Скрипты и назначения

`zap_regression_api_script.py`

Используется для автоматизации тестирования после сканирования через регрессию.

##### Особенности скрипта zap_regression:

* создает новый контекст по маске `.*timebook.ru/.*`
* не использует пауков тестирует только по ссылкам регрессии.