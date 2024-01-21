# Домашнее задание к занятию «Объекты с внутренним состоянием, управление состоянием при тестировании»

## Цель задания

1. Научиться управлять начальным состоянием объектов через конструкторы.


## Задание 1 — обязательное

Проект «Умный дом» развивается, и решено улучшить часть, отвечающую за радио.

Что нужно сделать: внедрить изменения в сам класс и тесты.

Как это сделать:

* создайте в Git в том же репозитории новую ветку flexible — возьмите проект к ДЗ про радио, в который уже подключены CI и нужные плагины;
* модифицируете класс `Radio` под новые требования;
* делаете тест-дизайн новой версии класса, модифицируете или добавляете новые тесты;
* пушите всё на GitHub и делаете pull request, мёржить его не нужно;
* удостоверьтесь, что все тесты в CI запускаются на pull request и проходят;
* ссылку на pull request пришлите в качестве результата ДЗ.

Требования к работе с радиостанциями

1. Можно задавать **количество радиостанций** при создании объекта, по умолчанию — 10.
1. Номер текущей радиостанции изменяется в пределах от 0 до количества радиостанций не включительно. То есть если станций 10, то номер последней — 9.
1. Если текущая радиостанция — максимальная, и клиент нажал на кнопку next на пульте, то текущей должна стать нулевая.
1. Если текущая радиостанция — 0, и клиент нажал на кнопку prev на пульте, то текущей должна стать максимальная.
1. Всё так же должен присутствовать сеттер текущей станции.

Теперь объекты радио в своём поле будут хранить и количество станций, заданное при создании объекта радио. Для этого вам понадобится создать свой конструктор для класса `Radio` с одним параметром, принимающим желаемое количество радиостанций и сохраняющим это значение у себя в поле. Ещё один конструктор потребуется без параметров, чтобы, если пользователь нашего класса не захотел указывать количество радиостанций, мы бы выставили их количество в 10 штук, как указано в требованиях, «по умолчанию — 10».

Внимание: конструктором с параметром задаётся именно количество радиостанций, а не номер максимальной, это разные вещи — если количество станций, например, 30, то последней будет номер 29, так как нумеруем мы с нуля.

Требования к работе с уровнем громкости звука:

* клиент должен иметь возможность увеличивать и уменьшать уровень громкости звука в пределах от 0 до 100;
* если уровень громкости звука достиг максимального значения, то дальнейшее нажатие на + не должно ни к чему приводить;
* если уровень громкости звука достиг минимального значения, то дальнейшее нажатие на - не должно ни к чему приводить.

Итог: ссылку на pull request пришлите в качестве результата ДЗ.

------


## Задание 2 — необязательное

Пришла пора разобраться с [Lombok](https://projectlombok.org). В вашем личном кабинете прикреплено видео, в котором демонстрируется работа с Lombok.

Что нужно сделать
1. Из ветки `flexible`, созданной в предыдущем задании, создайте ветку `lombok`, в которой перепишите ваш класс `Radio`, используя Lombok.
1. Сделайте коммит и pull request на GitHub, удостоверьтесь, что CI успешно проводит сборку, мёржить его не нужно.

### Результат
При отправке решения в личном кабинете прикрепите ссылку на ваш публичный репозиторий GitHub.



------
