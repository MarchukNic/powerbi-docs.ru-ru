---
title: Что можно сделать с помощью API Power BI
description: Что можно сделать с помощью API Power BI
author: rkarlin
ms.author: rkarlin
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 03/25/2019
ms.openlocfilehash: fd49c69a14d3dac6b1a045f6aba407ec7aac0deb
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61269456"
---
# <a name="what-can-developers-do-with-the-power-bi-api"></a>Какие возможности API Power BI предоставляет разработчикам?

Интерфейс REST API для Power BI позволяет создавать приложения, которые интегрируются с отчетами, панелями мониторинга и плитками Power BI.

С помощью REST API для Power BI можно управлять объектами Power BI, такими как отчеты, наборы данных и рабочие области.

Ниже перечислено несколько задач, которые можно выполнить с помощью API-интерфейсов Power BI.

| **Дополнительные сведения** | **Ссылаться на эти сведения** |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Внедрение отчетов, панелей мониторинга и плиток для пользователей Power BI и других программ. | [Как внедрять панели мониторинга, отчетов и плиток Power BI ](embedding-content.md) |
| Выполняйте задачи управления объектами Power BI. | [Справочник по REST API Power BI](https://docs.microsoft.com/rest/api/power-bi/) |
| Расширение существующего рабочего бизнес-процесса для принудительной отправки ключевых данных в панель мониторинга Power BI. | [Принудительная отправка данных в панель мониторинга ](walkthrough-push-data.md) |
| Аутентификация в Power BI. | [Аутентификация в Power BI ](get-azuread-access-token.md) |

> [!NOTE]
> В интерфейсах API Power BI рабочие области приложения по-прежнему называются группами. Если упоминаются группы, это означает, что вы работаете с рабочими областями приложения.

## <a name="api-developer-tools"></a>Инструменты API для разработчика

| Инструменты | Описание |  |  |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|---|---|
| [Средство playground](https://microsoft.github.io/PowerBI-JavaScript/demo) | Воспользуйтесь полным примером использования API-интерфейсов JavaScript в Power BI. Этот инструмент также позволит быстро познакомиться с разными примерами Power BI Embedded. |  |  |
| [Вики-сайте Power BI JavaScript](https://github.com/Microsoft/powerbi-javascript/wiki) | Дополнительные сведения об API-интерфейсах JavaScript в Power BI. |  |  |
| [Postman](https://www.getpostman.com/) | Выполнение запросов, тестирование, отладка, мониторинг, запуск автоматических тестов и многое другое. |

## <a name="push-data-into-power-bi"></a>Принудительная отправка данных в Power BI

Вы можете использовать API Power BI для [принудительной отправки данных в набор](walkthrough-push-data.md). Этот компонент позволяет добавлять строки в таблицу в наборе данных. После этого новые данные отображаются на плитках панели мониторинга и в визуальных элементах отчета.

![Принудительная отправка данных](media/what-can-you-do/powerbi-push-data.png)

## <a name="github-repositories"></a>Репозитории GitHub

* [Примеры для разработчиков Power BI](https://github.com/Microsoft/PowerBI-Developer-Samples)
* [Пакет SDK для .NET](https://github.com/Microsoft/PowerBI-CSharp)
* [JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript)

## <a name="next-steps"></a>Дальнейшие действия

* [Принудительная отправка данных в панель мониторинга Power BI](walkthrough-push-data.md)
* [Разработка пользовательского визуального элемента Power BI](custom-visual-develop-tutorial.md)
* [Справочник по REST API Power BI](rest-api-reference.md)
* [REST API в Power BI](https://docs.microsoft.com/rest/api/power-bi/)

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)
