---
title: Использование вычисляемых сущностей в Power BI Premium
description: Сведения об использовании вычисляемых сущностей в Power BI Premium
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 11/06/2018
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: 8131722d0e035f28fcb88827b1a68c2da97959cb
ms.sourcegitcommit: b23fdcc0ceff5acd2e4d52b15b310068236cf8c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51268934"
---
# <a name="using-computed-entities-on-power-bi-premium-preview"></a>Использование вычисляемых сущностей в Power BI Premium (предварительная версия)

Вы можете выполнять **вычисления в хранилище** при использовании **потоков данных** в подписке Power BI Premium. Это позволяет выполнять вычисления для существующих потоков данных и возвращать результаты, чтобы сосредоточиться на создании отчетов и аналитики. 

![Вычисляемые сущности в Power BI Premium](media/service-dataflows-computed-entities-premium/computed-entities-premium_00.png)

Чтобы выполнять **вычисления в хранилище**, сначала необходимо создать поток данных и перенести данные в хранилище этого потока данных в Power BI. Создав поток данных и наполнив его данными, вы можете создать **вычисляемые сущности**, т. е. сущности, которые производят вычисления в хранилище. 

Данные из потока можно подключить к Power BI двумя способами:

* [с помощью самостоятельного создания потоков данных](service-dataflows-create-use.md);
* с помощью внешнего поток данных.

Следующие разделы описывают создание вычисляемых сущностей на основе данным из потока данных.

> [!NOTE]
> Функции потоков данных предоставляются в предварительной версии и могут быть изменены до выпуска общедоступной версии.


## <a name="how-to-create-computed-entities"></a>Создание вычисляемых сущностей 

Создав поток данных со списком сущностей, вы можете выполнять по этих сущностям вычисления.

В средстве разработки потоков данных службы Power BI выберите действие **Изменение сущностей**, затем щелкните правой кнопкой мыши ту сущность, на основе которой вы намерены создать вычисляемую сущность, т. е. по которой будете выполнять вычисления. В контекстном меню выберите **Ссылка**.

Чтобы сущность можно было назначить вычисляемой сущностью, должен быть установлен флажок **Включить загрузку**, как показано на следующем рисунке. Щелкните сущность правой кнопкой мыши, чтобы отобразить контекстное меню.

![Установка флажка "Включить загрузку" в меню, которое открывается правой кнопкой мыши](media/service-dataflows-computed-entities-premium/computed-entities-premium_01.png)

Установив флажок **Включить загрузку**, вы создаете новую сущность, источником для которой будет исходная сущность. Значок сменится на значок **вычисляемой** сущности, как показано на следующем рисунке.

![Вычисляемые сущности в Power BI Premium](media/service-dataflows-computed-entities-premium/computed-entities-premium_00.png)

Любое преобразование, которое вы выполните для новой сущности, будет использовать те данные, которые уже находятся в хранилище потока данных Power BI. Это значит, что запрос будет выполняться не к внешнему источнику данных, из которого были импортированы данные (например, к базе данных SQL, из которой извлекались данные), а к тем данным, которые уже находятся в хранилище потока данных.

### <a name="example-use-cases"></a>Примеры вариантов использования
Какого рода преобразования можно выполнять для вычисляемых сущностей? Для вычислений в хранилище поддерживаются любые преобразования, которое обычно задаются с помощью пользовательского интерфейса преобразований в Power BI или редакторе M. 

Рассмотрим следующий пример: у вас есть сущность *Account* (Учетная запись), которая содержит необработанные данные для всех клиентов из подписки Dynamics 365. Также у вас есть необработанные данные *ServiceCalls* из центра поддержки по всем обращениям в службу поддержки, которые выполнялись для другой учетной записи за каждый день года.

Предположим, вы хотите дополнить сущность *Account* данными из *ServiceCalls*. 

Сначала вам следует агрегировать данные из ServiceCalls, чтобы вычислить число обращений в службу поддержки, которые выполнялись для каждой учетной записи в течение последнего года. 

![Пример вычисляемой сущности в Power BI Premium](media/service-dataflows-computed-entities-premium/computed-entities-premium_02.png)

После этого следует объединить сущность *Account* с сущностью *ServiceCallsAggregated*, чтобы вычислить дополненную таблицу **Account**.

![Пример вычисляемой сущности в Power BI Premium](media/service-dataflows-computed-entities-premium/computed-entities-premium_03.png)

После этого вы увидите результаты, представленные на следующем рисунке как *EnrichedAccount*.

![Результаты для вычисляемый сущности в Power BI Premium](media/service-dataflows-computed-entities-premium/computed-entities-premium_04.png)

Вот и все — преобразование выполняется по данным в потоке данных, которые хранятся в подписке Power BI Premium, а не по исходным данным.

## <a name="considerations-and-limitations"></a>Рекомендации и ограничения

Важно отметить, что в случае удаления рабочей области из емкости Power BI Premium связанный поток данных больше обновляться не будет. 


## <a name="next-steps"></a>Дальнейшие действия

В этой статье описываются вычисляемые сущности и потоки данных, доступные в службе Power BI. Вот еще несколько статьей, которые могут быть полезны:


* [Self-service data prep in Power BI (Preview)](service-dataflows-overview.md) (Самостоятельная подготовка данных в Power BI (предварительная версия))
* [Creating and using dataflows in Power BI (Preview)](service-dataflows-create-use.md) (Создание и использование потоков данных в Power BI (предварительная версия))
* [Использование потоков данных с локальными источниками данных (предварительная версия)](service-dataflows-on-premises-gateways.md)
* [Ресурсы для разработчиков потоков данных Power BI (предварительная версия)](service-dataflows-developer-resources.md)

Дополнительные сведения о Power Query и обновлении по расписанию содержатся в следующих статьях:
* [Общие сведения о запросах в Power BI Desktop](desktop-query-overview.md)
* [Настройка запланированного обновления](refresh-scheduled-refresh.md)

Дополнительные сведения о модели общих данных вы найдете в этой обзорной статье:
* [Что такое модель общих данных?](https://docs.microsoft.com/powerapps/common-data-model/overview)
