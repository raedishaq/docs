---
title: Состояния фиксаций
intro: 'API состояния фиксации позволяет внешним службам присваивать фиксациям определенные состояния, которые отображаются во всех запросах на вытягивание, затрагивающих эти фиксации.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - API
miniTocMaxHeadingLevel: 3
allowTitleToDifferFromFilename: true
ms.openlocfilehash: 4c75b4817ecddad0e91460d7d12eddabc634d588
ms.sourcegitcommit: 5f9527483381cfb1e41f2322f67c80554750a47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2022
ms.locfileid: '147882298'
---
## Сведения об API состояний фиксации

API состояния фиксации позволяет внешним службам помечать фиксации состоянием `error`, `failure`, `pending` или `success`, которое затем отражается в запросах на вытягивание с использованием этих фиксаций. Состояния также могут включать дополнительные параметры `description` и `target_url`, поэтому мы настоятельно рекомендуем их указывать — с ними состояния будут еще более полезными в пользовательском интерфейсе GitHub.

Например, службы непрерывной интеграции с помощью состояний показывают передачу фиксаций или сбои сборки.  Параметр `target_url` — это полный URL-адрес выходных данных сборки, а `description` — краткая сводка того, что произошло со сборкой.

Состояния могут содержать `context`, который показывает, какая служба предоставляет это состояние. Например, ваша служба непрерывной интеграции может передавать состояния с контекстом `ci`, а средство аудита безопасности — с контекстом `security`.  Чтобы узнать, как получить полное состояние фиксации, см. [Получение объединенного состояния для определенной ссылки](/rest/reference/commits#get-the-combined-status-for-a-specific-reference).

Обратите внимание на то, что `repo:status` [область OAuth](/developers/apps/scopes-for-oauth-apps) предоставляет целевой доступ к состояниям **без** доступа к коду репозитория, а область `repo` — и к коду, и к состояниям.

Если вы разрабатываете приложение GitHub и хотите предоставить более подробные сведения о внешней службе, используйте [API проверки](/rest/reference/checks).