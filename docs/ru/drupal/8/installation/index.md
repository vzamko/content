---
title: Руководство по установке
slug: wiki/8/installation
core: 8
category:
  area: Первое знакомство
  order: 1
  title: Установка
search-keywords:
  - Как устанавливать установить Drupal
metatags:
  title: 'Drupal 8: Руководство по установке'
  description: 'Обзор этапов установки Drupal 8.'
---

**Установка Drupal** — процесс, в результате которого производится базовая конфигурация сайта и его настройка, создание необходимых структур в базе данных, настройка часовых поясов, административного аккаунта, а также первоначальный перевод сайта.

Для того чтобы установить Drupal 8, вам потребуется веб-сервер Apache или Nginx, PHP, а также, желательно, база данных, например MySQL. Для более детальной информации обращайтесь к системным требованиям.

После того как вы подготовили необходимое окружение, вам необходимо скачать Drupal и разместить его файлы в корневой папке вашего будущего сайта. Это можно сделать, [скачав Drupal в виде архива](https://www.drupal.org/download), либо, используя [Composer](../../../composer/index.md), вы можете использовать [Drupal Recommended Project](../../../composer/drupal/recommended-project/index.md).

> [!TIP]
> Настоятельно рекомендуется использовать установку Drupal при помощи [Drupal Recommended Project](../../../composer/drupal/recommended-project/index.md). Это может показаться более сложным и комплексным на старте, но в дальнейшем, вы избежите множества проблем.
>
> Это **официально** рекомендуемый способ установки Drupal 8.

После этого, открыв страницу сервера, для которой вы подготовили окружение и произвели все необходимые настройки, перед вами откроется установка Drupal. Процесс установки не отличается от выбранного способа установки Drupal, это касается лишь структуры файловой системы сайта и конфигурации веб-сервера.

## Этапы установки

### Выбор языка

![Выбор языка](https://i.imgur.com/TFwnfFf.png)

Первым делом Drupal предложит выбрать язык сайта. Это основной язык, который будет использоваться по умолчанию после установки. Вы сможете добавить другие языки после завершения установки при помощи [административного интерфейса](../admin/index.md) и выбрать другой язык по умолчанию, и удалить не используемые. 

Данный выбор также влияет на то, на каком языке будет интерфейс установки. Для всех языков, отличных от английского, в процессе установки сайта будут загружены и установлены переводы данного языка. Если в момент установки отсутствует подключение к интернету, переводы не будут выполнены и установка продолжится и закончится на выбранном языке, но с английским интерфейсом. Вы сможете в дальнейшем обновить переводы для нужного языка.

> [!NOTE]
> Язык сайта можно менять и настраивать в процессе работы с сайтом. Данный выбор не является финальным.

### Выбор установочного профиля

![Выбор профиля](https://i.imgur.com/tSfij2z.png)

Установочные профили — это [дистрибутивы](../distributions/index.md). На данном этапе, вы выбираете, какой профиль установки будет использован для дальнейших этапов.

Выбор профиля может повлиять не только на результат установки, но и на сам процесс. Могут появиться дополнительные шаги, настройки и т.д.

По умолчанию предлагается установить "Стандартный" профиль установки.

Коротко о профилях поставляемых ядром:

- [**Стандарт**](../distributions/standard/index.md). Данный профиль выбран по умолчанию для всех установок. Он устанавливает всё самое необходимое для того, чтобы начать делать сайт. Он включает достаточное количество стандартных модулей, настраивает несколько типов содержимого для примера и расположение блоков, тему оформления и другие мелкие нюансы. Если вы не уверены какой профиль выбрать — данный профиль самый надёжный способ начать знакомство и попробовать что-то сделать на Drupal.
- [**Минимальный**](../distributions/minimal/index.md). Профиль для тех, кто хочет настраивать всё сам, и уже имеет понимание что такое Drupal и какой-то опыт работы с ним. С данным профилем установятся только самые необходимые для функционирования системы модули. Всё остальное необходимо настраивать самостоятельно. Данный профиль стоит рассматривать как установку "чистого" ядра.
- [**Demo: Umami Food Magazine**](../distributions/demo-umami/index.md). Данный профиль появился начиная с Drupal 8.6.0. Это демонстрационный профиль, который создаёт сайт "журнала" о кулинарии и еде. Он имеет собственную тему оформления, настроенные типы содержимого, поля, страницы, поиск, а также демо-контент. Это отличный выбор если вы хотите посмотреть на какой-то реальный сайт, а не голую систему где нужно всё настраивать самому. Не используйте данный профиль для создания реальных сайтов.

> [!TIP]
> Если вы впервые устанавливаете Drupal, попробуйте демонстрационный профиль **Umami Food Magazine**.

> [!NOTE]
> Вы можете создавать свои собственные профили для установки и делиться ими с сообществом. За более подробной информацией перейдите на страницу [дистрибутивов](../distributions/index.md).

### Проверка соответствия требованиям

Данный этап будет пропущен если всё настроено корректно.

Если вы попали на данный этап — значит что-то не так. Вам будут написаны причины и проблемы, которые вам необходимо устранить. Пока вы их не устраните, вы не сможете продолжить установку.

Чаще всего, проблемы касаются серверной части. Очень распространённая проблема — некорректные настройки прав доступа.

Зачастую информацию об ошибках и как её исправлять, можно легко найти в поиске, если же вы по каким-то причинам не можете решить данные проблемы, то лучше всего обратиться к [сообществу](../../community/resources/index.md) за помощью.

### Установка баз данных

![Установка баз данных](https://i.imgur.com/Dl2T7pn.png)

На данном этапе вы должны выбрать какой тип баз данных будет использоваться для сайта и указать настройки подключения к БД.

Если вы не уверены какой тип базы данных выбрать, берите самый распространённый — MySQL, MariaDB. Они есть на каждом хостинге, это самый распространённый тип баз данных для сайтов, с ним вы будете в полной безопасности.

> [!IMPORTANT]
> Разные типы БД имеют разный функционал и возможности, свои плюсы и минусы. Данный выбор может повлиять на то, как будет работать Drupal.

> [!NOTE]
> Drupal позволяет писать [модули](../modules/index.md), которые добавляют новые драйверы баз данных. Например, вы можете использовать [базы данных Oracle](https://www.drupal.org/project/oracle) после установки соответствующего модуля.

### Установка сайта

![Установка сайта](https://i.imgur.com/ienPkI9.png)

На этапе установки сайта, от вас не требуется никаких действий. В зависимости от выбранного профиля установки, будут произведены соответствующие настройки сайта. Вам лишь следует дождаться окончания.

Данный процесс может занять несколько минут, особенно, если вы устанавливаете профиль с уже множеством готовых настроек, структуры, содержимого и т.д.

### Установка переводов

![Установка переводов](https://i.imgur.com/mo3xUIc.png)

После того как произведена основная установка сайта, всё что было установлено, будет проверено на наличие переводов, они будут загружены и применены.

На этом этапе никаких действий от пользователя не требуется. Импорт переводов может занять длительное время.

> [!TIP]
> Если вы выбрали английский язык для установки, данный этап будет пропущен.

### Настройка сайта

![Настройка сайта](https://i.imgur.com/AiyvHQO.png)

Настройка сайта позволяет установить значения по умолчанию самым необходимым настройкам сайта:

- **Информация о сайте**: Базовые настройки сайта.
  - **Название сайта**: Название будущего сайта, будет использоваться на главной странице и в заголовках страниц.
  - **Адрес электронной почты сайта**: Данный адрес электронной почты будет использоваться в качестве почты сайта. По умолчанию, все письма отправляемые сайтом, будут отправлены с данной почты. Данное значение используется многими модулями, требующих настройку почтового адреса, как значение по умолчанию.
- **Учетная запись обслуживания сайта**: Настройки доступа самого главного пользователя на сайте (<abbr title="User Identifier — Идентификатор пользователя">UID</abbr>: 1). Воспринимайте данного пользователя как superuser или root-пользователь. Данный пользователь больше чем просто администратор, он имеет исключительные права, особенное поведение, например, как пропуск любой проверки прав доступа. Таких пользователей в системе больше быть не может, поэтому позаботьтесь чтобы он был защищен.
- **Региональные настройки**.
  - **Страна по умолчанию**: Данная страна будет автоматически указываться, где это требуется. Ядро Drupal использует данное значение для работы с форматами дат и чисел. Например, выбрав Россию, по умолчанию будут использоваться наш формат записи даты дд.мм.гггг, время будет в 24-часовом формате и т.д.
  - **Часовой пояс по умолчанию**: Данная настройка влияет на то, в каком поясе будут отображаться даты на сайте. В дальнейшем, можно настроить чтобы пользователи могли выбирать свой часовой пояс, и все даты будут показываться в их персональном часовом поясе.
- **Оповещения об обновлениях**: Позволяет настроить поведение при обновлениях. Можно полностью отключить проверку обновлений системы и модулей (крайне не рекомендуется),  а также отправку уведомлений на почту указанную в "Адрес электронной почты сайта", что для сайта доступны обновления.

> [!NOTE]
> Данная форма может отличаться или вовсе отсутствовать если вы используете профиль отличный от "стандартного".

### Завершение переводов

На этом этапе проводятся финальные доработки переводов и действий от пользователя не требуется.

### Ваш готовый сайт

![Ваш сайт на Drupal](https://i.imgur.com/Os2YpKn.png)

После всех прошедших этапов, вас перенаправит на главную страницу вашего нового сайта на Drupal. Вы будете автоматически авторизованы под административным пользователем и сможете приступать к работе.

> [!NOTE]
> В зависимости от выбранного профиля установки, результат установки будет разный. На скриншоте выше представлен результат установки "стандартного" установочного профиля. Например, выбрав umami, вас встретит уже журнал со статьями, рецептами и совершенно другой темой оформления.

## Смотрите также

- [Административный интерфейс](../admin/index.md)
- [Модули — позволяют расширять возможности Drupal](../modules/index.md)
- [Темы оформления — влияют на внешний вид сайта](../themes/index.md)
