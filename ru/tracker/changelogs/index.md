# История изменений в {{ tracker-full-name }} в мае 2023

* [Обновления](#top-news)
* [Исправления и улучшения](#fixes)

## Обновления {#top-news}

### Перенос досок на новые технологии {#old-to-new}

Старые доски теперь можно [перенести](../manager/boards-convertor.md) на [новые технологии](../manager/agile-new.md). При миграции у доски сохранятся:
* идентификатор;
* название;
* добавленные задачи;
* распределение статусов по колонкам;
* фильтры **Я автор** и **Я исполнитель**;
* фильтр для добавления задач.

При необходимости после миграции вы сможете вернуть доску к старой версии. Для этого на верхней панели доски нажмите ![](../../_assets/tracker/svg/actions.svg) → **Миграция в старую версию** и дождитесь завершения миграции.

### Группировка задач по любому полю {#grouping}

Добавлена группировка задач по любому полю. Эта возможность доступна для [списка задач проекта](../manager/project-list.md), диаграммы Ганта проекта, а также на [новых досках](../manager/agile-new.md).

Чтобы сгруппировать задачи, нажмите кнопку ![](../../_assets/tracker/svg/group.svg) и выберите поле.

### Настройка цвета задач для диаграммы Ганта по очереди и фильтру {#gantt-colours-filter}

На [диаграмме Ганта](../gantt/project.md) по очереди и фильтру можно назначать цвет задачам в зависимости от выбранного параметра (очередь, статус, и др.). Для этого на странице с диаграммой Ганта нажмите **Настройки диаграммы** и в разделе **Цвет задач** выберите **по параметрам задачи**.

### Кнопки **Свернуть** и **Развернуть** {#new-buttons}

На странице [проекта](../manager/project-new.md) на вкладках **Список задач** и **Диаграмма Ганта** появились кнопки **Свернуть** и **Развернуть**. Они позволяют развернуть и свернуть:
* все подзадачи в древовидном списке;
* все группы в режиме групировки.

### Навигация по стрелкам {#arrow-buttons}

В списках задач теперь можно перемещаться с помощью клавиатуры:

* клавиши-стрелки — для навигации в меню;
* **Enter** или пробел — для перехода по ссылке.


### Отключение организации {#no-orgs}

Теперь для работы в {{ tracker-name }}, {{ wiki-name }} и {{ forms-name }} можно выбрать одну [организацию](../cloud-vs-360.md) и отключить вторую, если она не нужна. Чтобы отключить организацию, перейдите на страницу ![](../../_assets/tracker/svg/admin.svg) **Администрирование** → ![](../../_assets/tracker/svg/organizations.svg) [**Организации**]({{ link-tracker }}admin/orgs). Нажмите ![](../../_assets/tracker/dots.png) и выберите **Отключить**.

При этом она будет отключена от сервисов {{ tracker-name }}, {{ wiki-name }} и {{ forms-name }}. Данные сохранятся, но пользователи этой организации будут помечены как уволенные, группы будут удалены, а права доступа отозваны. Настроенные почтовые алиасы на домене в очередях будут удалены.


### Кнопки перехода к комментарию {#comment-up-down}

Добавлены кнопки перехода к первому или последнему комментарию в задачах. Чтобы перейти к описанию задачи, нажмите кнопку ![](../../_assets/tracker/to-first-comment.png =12x12)  два раза.
Также для навигации можно использовать клавиши:

* **Windows**: **Home** или **End**;
* **Mac OS**: **⌘** + **↑** или **⌘** + **↓**.

### Обязательные комментарии на экране перехода {#flow-comments}

В [новом редакторе воркфлоу](../manager/workflow.md) появилась возможность сделать обязательным заполнение комментария при смене статуса задачи. Чтобы сделать поле **Комментарий** обязательным, перейдите в редактор воркфлоу и в разделе **Экран перехода** выберите опцию&nbsp;**Обязательное**.

## Исправления и улучшения {#fixes}

### Отображение завершенных спринтов {#scroll-fixed}

* Исправлена ошибка, при которой список завершенных спринтов отображался лишь частично.
* Завершенные спринты сортируются по дате завершения: недавно завершенные спринты располагаются в списке выше.
* Появилась кнопка перехода на список задач спринта на странице фильтра.
