---
title: Планирование и отслеживание работы для команды или проекта
intro: 'Основные сведения об использовании средств планирования и отслеживания {% data variables.product.prodname_dotcom %} для управления работой c командой или проектом.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: overview
topics:
  - Project management
  - Projects
ms.openlocfilehash: 782351c80164c90d479120996edf25329d20078c
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/05/2022
ms.locfileid: '147423615'
---
## Введение
Репозитории, проблемы, доски проектов и другие инструменты {% data variables.product.prodname_dotcom %} можно использовать для планирования и отслеживания работы, будь то работа над отдельным проектом или в междисциплинарной команде.

Из этого руководства вы узнаете, как создать и настроить репозиторий для совместной работы с группой людей, создавать шаблоны{% ifversion fpt or ghec %} и формы проблем{% endif %}, открывать проблемы и использовать списки задач для деления работ на фрагменты, а также как создать доску проекта для организации и отслеживания проблем.

## Создание репозитория
При запуске нового проекта, инициативы или компонента в первую очередь создается репозиторий. Репозитории содержат все файлы проекта и служат местом для совместной работы с другими пользователями и управления работой. Дополнительные сведения см. в разделе [Создание репозитория](/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/creating-a-new-repository).

Репозитории можно настраивать для разных целей в зависимости от ваших потребностей. Вот несколько основных способов применения:

- **Репозитории продуктов**: крупные организации, которые отслеживают свою работу и цели по отдельным продуктам, могут иметь один или несколько репозиториев, содержащих код и другие файлы. Такие репозитории также можно использовать для документации, отчетов о работоспособности продукта или планов по его развитию. 
- **Репозитории проектов**: репозитории можно создавать как для личных проектов, так и для проектов, над которым вы работаете вместе с другими пользователями. Организации, которая отслеживает работу по краткосрочным инициативам или проектам, например консалтинговой компании, необходимо получать отчеты о работоспособности проекта и перераспределять людей между разными проектами с учетом навыков и потребностей. Код проекта часто содержится в одном репозитории.
- **Репозитории команд**: в организации, где над проектами работают команды, такие как команда средств разработки, код может быть распределен между несколькими репозиториями, созданными для разных работ, которые им нужно отслеживать. В этом случае может быть удобнее создать для каждой команды отдельный репозиторий как единое место для отслеживания всех работ, в которых она участвует.
- **Личные репозитории**: личный репозиторий позволяет отслеживать все работы в одном месте, планировать будущие задачи и даже добавлять заметки или информацию, которую вы хотите сохранить. Сюда можно добавлять участников совместной работы, чтобы предоставить доступ к информации другим пользователям. 

Если вам необходимы разные разрешения на доступ к исходному коду или вы хотите отслеживать проблемы и обсуждения, можно создать несколько отдельных репозиториев. Дополнительные сведения см. в разделе [Создание репозитория только для проблем](/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/creating-an-issues-only-repository).

В следующих примерах в этом руководстве мы будем использовать пример репозитория под названием Project Octocat.
## Передача данных о репозитории
Для репозитория можно создать файл README.md, чтобы рассказать о своей команде или проекте или сообщить важные сведения о репозитории. Зачастую README — первое, что видит посетитель репозитория, поэтому здесь же можно указать, каким образом пользователи или участники могут приступить к работе над проектом и как связаться с командой. Дополнительные сведения см. в статье [О файлах README](/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-readmes).

Кроме того, можно создать файл CONTRIBUTING.md и добавить в него инструкции по участию в работе и взаимодействию с командой или проектом, например, информацию о том, как подать запрос на устранение ошибки или на доработку. Дополнительные сведения см. в разделе [Настройка инструкций для участников репозитория](/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors).
### Пример файла README
Создадим файл README.md с информацией о нашем новом проекте — Project Octocat. 

![Создание примера файла README](/assets/images/help/issues/quickstart-creating-readme.png)
## Создание шаблонов проблем

Проблемы можно использовать для отслеживания различных типов работ вашей междисциплинарной команды или проекта, а также для сбора соответствующей информации за пределами проектами. Приведем несколько распространенных вариантов использования проблем.

- Отслеживание выпусков: проблему можно использовать для отслеживания хода выполнения выпуска или этапов запуска.
- Крупные инициативы: проблему можно использовать для отслеживания хода выполнения крупной инициативы или проекта, которые затем сопоставляются с проблемами поменьше.
- Запросы компонентов: ваша команда или пользователи могут создавать проблемы для запроса доработки того или иного продукта или проекта.
- Ошибки: ваша команда или пользователи могут создавать проблемы для сообщения об ошибке. 

В зависимости от типа репозитория и проекта, над которым вы работаете, одним типам проблем можно присваивать более высокий приоритет, чем другим. Определив наиболее распространенные типы проблем для вашей команды, вы можете создать шаблоны {% ifversion fpt or ghec %}и формы проблем{% endif %} для репозитория. Шаблоны {% ifversion fpt or ghec %}и формы проблем{% endif %} позволяют создавать стандартизированный список шаблонов, которые участник сможет выбирать, открывая проблему в репозитории. Дополнительные сведения см. в разделе [Настройка шаблонов проблем для репозитория](/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository).

### Пример шаблона проблем
Ниже мы создадим шаблон проблемы для сообщения об ошибке в Project Octocat.

![Создание примера шаблона проблемы](/assets/images/help/issues/quickstart-creating-issue-template.png)

Теперь, когда мы создали шаблон проблемы с сообщением об ошибке, его можно будет выбрать при создании новой проблемы в Project Octocat.

![Выбор примера шаблона проблемы](/assets/images/help/issues/quickstart-issue-creation-menu-with-template.png)

## Открытие проблем и использование списков задач для отслеживания работы
Для организации и отслеживания работы можно создавать проблемы. Дополнительные сведения см. в статье "[Создание проблемы](/issues/tracking-your-work-with-issues/creating-issues/creating-an-issue)".
### Пример проблемы
Приведем пример проблемы, созданной для крупной иницбиативы (внешний интерфейс) в Project Octocat.

![Пример создания проблемы для крупной инициативы](/assets/images/help/issues/quickstart-create-large-initiative-issue.png)
### Пример списка задач

Списки задач можно использовать для деления больших проблем на небольшие задачи и отслеживания проблем в рамках более крупной цели. {% ifversion fpt or ghec %} При добавлении в текст проблемы у списков задач появляются дополнительные функциональные возможности. В верхней части проблемы отображается количество завершенных задач, а если кто-то закрывает проблему, входящую в список задач, автоматически устанавливается флажок завершения.{% endif %} Дополнительные сведения см. в статье [Сведения о списках задач](/issues/tracking-your-work-with-issues/creating-issues/about-task-lists).

Ниже мы добавили список задач в проблему Project Octocat, разделив ее на проблемы поменьше.

![Пример добавления списка задач в проблему](/assets/images/help/issues/quickstart-add-task-list-to-issue.png)

## Принятие решений в команде
Проблемы и обсуждения можно использовать для взаимодействия и командного принятия решений по плановым доработкам или приоритетам в рамках проекта. Проблемы полезно создавать для обсуждения определенных деталей, таких как отчеты об ошибках или производительности, планы на следующий квартал или разработка новой инициативы. Обсуждения полезны для открытого мозгового штурма или обратной связи за пределами базы кода и в репозиториях. Дополнительные сведения см. в статье [Какой инструмент обсуждения лучше использовать](/github/getting-started-with-github/quickstart/communicating-on-github#which-discussion-tool-should-i-use).

Кроме того, в рамках команды с помощью проблем можно сообщать об изменениях в повседневных задачах, чтобы все были в курсе состояния работы. Например, можно создать проблему для большого компонента, над которым работают несколько человек, что позволит каждому участнику группы добавлять обновления с указанием состояния и открывать вопросы в этой проблеме.
### Пример проблемы с участниками проектами
Приведем пример того, как участники одного проекта сообщают об изменении состояния работы в проблеме Project Octocat.

![Пример совместной работы в проблеме](/assets/images/help/issues/quickstart-collaborating-on-issue.png)
## Использование меток для выделения целей и состояния проекта
Для репозитория можно создавать метки, позволяющие классифицировать проблемы, запросы на вытягивание и обсуждения. Кроме того, в {% data variables.product.prodname_dotcom %} предусмотрены метки по умолчанию для каждого нового репозитория, которые можно изменять или удалять. Метки помогают отслеживать цели проектов, ошибки, типы работ и состояния проблемы.

Дополнительные сведения см. в разделе [Создание метки](/issues/using-labels-and-milestones-to-track-work/managing-labels#creating-a-label).

Метку, созданную в репозитории, можно впоследствии применять к любой проблеме, запросу на вытягивание или обсуждению в этом репозитории. Фильтрация проблем и запросов на вытягивание по меткам позволит найти все соответствующие работы. Например, чтобы найти в проекте все ошибки внешнего интерфейса, отфильтруйте проблемы с метками `front-end` и `bug`. Дополнительные сведения см. в статье [Фильтрация и поиск проблем и запросов на вытягивание](/issues/tracking-your-work-with-issues/filtering-and-searching-issues-and-pull-requests).
### Пример метки
Ниже приведен пример метки `front-end`, которую мы создали и добавили в проблему.

![Пример добавления метки в проблему](/assets/images/help/issues/quickstart-add-label-to-issue.png)

## Добавление проблем на доску проекта

{% ifversion projects-v2 %}

Вы можете использовать {% data variables.projects.projects_v2 %} на {% data variables.product.prodname_dotcom %} для планирования и отслеживания работы для вашей команды. Проект — это настраиваемая электронная таблица, которая интегрируется с вашими проблемами и запросами на вытягивание в {% data variables.product.prodname_dotcom %} и автоматически обновляет сведения в {% data variables.product.prodname_dotcom %}. Макет можно настраивать, фильтруя, сортируя и группируя проблемы и запросы на вытягивание. Сведения о начале работы с проектами см. в [кратком руководстве по проектам](/issues/planning-and-tracking-with-projects/learning-about-projects/quickstart-for-projects).
### Пример проекта
Ниже показан табличный макет из примера проекта, заполненный созданными нами проблемами Project Octocat.

![Пример табличного макета для проектов](/assets/images/help/issues/quickstart-projects-table-view.png)

Этот же проект можно открыть как доску.

![Пример макета-доски для проектов](/assets/images/help/issues/quickstart-projects-board-view.png)

{% endif %} {% ifversion projects-v1 %}

Вы можете {% ifversion projects-v2 %}также использовать существующие {% else %}использовать{% endif %} {% data variables.product.prodname_projects_v1 %} на {% data variables.product.prodname_dotcom %} для планирования и отслеживания своей работы и работы вашей команды. Доски проектов состоят из проблем, запросов на вытягивание и заметок, распределенных в виде карточек между столбцами по вашему выбору. Доски проектов можно создавать для работы компонентов, для дорожных карт высокого уровня и даже для контрольных списков выпусков. Дополнительные сведения см. в разделе [О панелях проектов](/issues/organizing-your-work-with-project-boards/managing-project-boards/about-project-boards).
### Пример доски проекта
Ниже показана доска проекта для репозитория Project Octocat из нашего примера с созданной нами проблемой, и добавлены проблемы поменьше, на которые мы ее разделили.

![Пример доски проекта](/assets/images/help/issues/quickstart-project-board.png)

{% endif %}

## Дальнейшие действия

Вы узнали о предлагаемых инструментах {% data variables.product.prodname_dotcom %} для планирования и отслеживания работы, а также о том, как настраивать репозиторий для междисциплинарной команды или проекта. Вот несколько полезных ресурсов по дальнейшей настройке репозитория и организации вашей работы.

- [Сведения о репозиториях](/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-repositories) — дополнительные сведения о создании репозиториев.
- [Отслеживание работы с использованием проблема](/issues/tracking-your-work-with-issues) — дополнительные сведения о различных способах создания проблем и управления ими.
- [Сведения о шаблонах проблем и запросов на вытягивание](/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates) — дополнительные сведения о шаблонах проблем.
- [Управление метками](/issues/using-labels-and-milestones-to-track-work/managing-labels) — дополнительные сведения о создании, редактировании и удалении меток.
- [Сведения о списках задач](/issues/tracking-your-work-with-issues/creating-issues/about-task-lists) — дополнительные сведения о списках задач {% ifversion projects-v2 %} - [Сведения о проектах](/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) — дополнительные сведения о проектах
- [Настройка представления](/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-a-view) — дополнительные сведения о том, как настраивать представления для проектов{% endif %} {% ifversion projects-v1 %}- [Сведения о {% data variables.product.prodname_projects_v1 %}](/issues/organizing-your-work-with-project-boards/managing-project-boards/about-project-boards) — дополнительные сведения об управлении досками проектов{% endif %}