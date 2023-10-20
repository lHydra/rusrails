[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/rusrails/rusrails?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
Официальный репозиторий проекта [RusRails.ru](http://rusrails.ru)
=================================================================

Проект **RusRails** является неофициальным переводом [официальных руководств по Ruby on Rails](http://guides.rubyonrails.org/)

Установка и запуск
------------------

* Скопировать и установить

    ```
    $ git clone git://github.com/rusrails/rusrails.git
    $ cd rusrails
    $ bundle install
    ```

* Создать конфиг для своих настроек бд (`config/database.yml`)

* Создать базу данных и загрузить схему базы данных

	```
	rails db:setup
	```
* Заполнить базу

    ```
    $ rails static_docs:import
    ```

* Запустить сервер и открыть в браузере

Пул-реквесты
-----------

Все пул-реквесты нужно делать в ту ветку, которая выставлена в данный момент текущей на гитхабе!

Нашли ошибку?
-------------

* Находите нужный файл в `source` (соответствие url на сайте rusrails и имени файла задается в `source/index.yml`)
* В интерфейсе есть кнопка Edit
* Вносите изменение
* Commit / Push

Нашли много ошибок?
-------------------

* Делаете форк. [Инструкция по форкам](http://help.github.com/fork-a-repo/)
* У себя в репозитории правите ошибки (желательно для каждого руководства править ошибки в отдельных ветках)
* Отправляете пул-реквест

Хотите помочь с переводами?
---------------------------

Для удобного перевода, каждое руководство привязано к определенной ревизии [rails/rails](https://github.com/rails/rails/tree/master/guides/source),
в файле [source/index.yml](https://github.com/rusrails/rusrails/blob/master/source/index.yml).
Таким образом, указывается заголовок на русском, url, имя файла, ревизия и дата коммита.

Алгоритм работы:

* Делаете форк. [Инструкция по форкам](http://help.github.com/fork-a-repo/)
* Выбираете руководство (степень актуальности всех руководств можно оценить с помощью `rails docrails:status`)
* Открываете [issue в rusrails](https://github.com/rusrails/rusrails/issues), с пометкой о руководстве которое хотите обновить/перевести (чтобы этим руководством никто параллельно не занимался)
* Смотрите, что изменилось - `rails 'docrails:diff[file_name]' > diff.diff` - в файле `diff.diff`
* В том же файле смотрите информацию по последней ревизии и ее дате, изменяете эти данные в `source/index.yml`
* Вносите в нужных местах исправления по диффу
* Отправляете пул-реквест

Хотите помочь с развитием сайта?
--------------------------------

Есть много всяких идей, до которых руки не доходят, например, правки дизайна, социализация, расширение на другие руководства, связанные с Rails, версии в PDF/kindle и т.д.

Предлагайте свои идеи, которые в состоянии реализовать. [@RusRails](http://twitter.com/rusrails)

Развертывание
-------------

[HTML версия](https://github.com/rusrails/rusrails.github.io) развертывается на Github Pages.

Предполагается, что клон репозитория `rusrails/rusrails.github.io` находится в той же директории, что и клон `rusrails/rusrails`.

Тогда `rails deploy:start` сгенерирует свежую версию и отправит на Гитхаб.
