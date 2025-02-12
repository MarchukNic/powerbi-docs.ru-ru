---
title: Сведения о потоках данных в Power BI
description: Узнайте, как работают потоки данных в Power BI
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 04/01/2019
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: 55571cda4558b5dd9ba28f757f6e11ad4b45f939
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61136388"
---
# <a name="self-service-data-prep-in-power-bi"></a>Подготовка данных самообслуживания в Power BI

По мере роста объема данных повышается и сложность преобразования этих данных в практически применимую информацию нужного формата. Нам нужны такие данные, которые пригодны для аналитики, для заполнения визуализаций, отчетов и панелей мониторинга, поэтому мы должны быстро преобразовывать весь объем данных в практически применимые аналитические сведения. Power BI предлагает функцию **самостоятельной подготовки данных** для больших данных, что позволяет получить в Power BI аналитические сведения из исходных данных всего несколькими щелчками мыши.

![Использование потоков данных в Power BI](media/service-dataflows-overview/powerbi-dataflows_01.png)

В Power BI появились **потоки данных**, которые помогают организациям объединять данные из разнородных источников и готовить их к моделированию. Аналитики смогут легко создавать потоки данных с помощью уже знакомых инструментов для самостоятельной работы. Потоки данных позволяют принимать, преобразовывать, интегрировать и дополнять большие данные, определяя соединители с источниками данных, логику извлечения, преобразования и загрузки, расписания обновления и многое другое. Кроме того, новый механизм вычислений на основе модели, который включен в потоки данных, упрощает для аналитиков и создателей отчетов контроль над процессом подготовки данных, позволяет получить более стабильные результаты с меньшими усилиями. Точно так же, как электронные таблицы выполняют повторные вычисления для всех затронутых формул, потоки данных от вашего имени управляют изменениями для сущности или элемента данных, автоматизируют обновления и устраняют монотонные и длительные проверки логики, которые необходимы даже при простейших обновлениях данных. Благодаря потокам данных задачи, которые специалисты по обработке данных ранее контролировали вручную и на которые тратили несколько часов или даже дней, теперь можно выполнить несколькими щелчками мыши. 

Данные хранятся в виде сущностей [**модели общих данных**](https://docs.microsoft.com/powerapps/common-data-model/overview) в Azure Data Lake Storage 2-го поколения. Потоки данных создаются и управляются в рабочих областях приложений с помощью службы Power BI.  
 
В **потоках данных** используется **модель общих данных** — это стандартизированная модульная расширяемая коллекция схем данных, опубликованных Майкрософт, которые призваны упростить создание, использование и анализ данных. С помощью этой модели вы можете передавать данные из источников на панели мониторинга Power BI практически без усилий.

Потоки данных поддерживают прием данных из большого постоянно растущего набора локальных и облачных источников данных, в который уже сейчас входят Dynamics 365, Salesforce, База данных SQL Azure, Excel, SharePoint и многие другие.

Вы можете сопоставлять полученные данные со стандартными сущностями в модели общих данных, а также изменять и расширять существующие сущности и создавать пользовательские сущности. Опытные пользователи могут создавать полностью настраиваемые потоки данных с помощью встроенного интерфейса самообслуживания Power Query, который предусматривает работу с малым объемом кода или вовсе без кода. Этот интерфейс похож на Power Query, который уже хорошо знаком миллионам пользователей Power BI Desktop и Excel.  

После создания потока данных с помощью Power BI Desktop и службы Power BI можно создавать наборы данных, отчеты, панели мониторинга и приложения, использующие всю мощь модели общих данных для получения ценных аналитических сведений, касающихся вашего бизнеса. 

Расписанием обновления потока данных можно управлять непосредственно из рабочей области, в которой был создан этот поток данных, так же как для наборов данных. 

## <a name="how-dataflows-work"></a>Как работают потоки данных

Ниже приведены несколько примеров применения потоков данных.

* Организации могут сопоставлять свои данные со стандартными сущностями в модели общих данных или создавать собственные настраиваемые сущности. Эти сущности далее станут строительными блоками для отчетов, панелей мониторинга и приложений, которые не требуют дополнительной настройки и без проблем предоставляются любым пользователям в пределах организации. 

* Организации могут подключать к наборам данных собственные источники данных с помощью обширного набора соединителей данных Майкрософт, сопоставлять данные с источником с помощью Power Query и передавать эти данные в Power BI. После импорта данных в поток данных (с учетом обновления с указанной частотой) настроенные сущности потока данных можно применять в приложениях Power BI Desktop для создания презентабельных отчетов и панелей мониторинга. 

## <a name="how-to-use-dataflows"></a>Как использовать потоки данных

В предыдущем разделе описаны несколько способов применения потоков данных для быстрого создания мощных аналитических средств в Power BI. В этом разделе вы найдете краткий обзор процесса, позволяющего быстро создать корпоративные аналитические данные с помощью потоков данных. Также вы узнаете, как специалисты по бизнес-аналитике могут создавать собственные потоки данных и настраивать аналитические сведения для своей организации.

> [!NOTE]
> Для работы с потоками данных требуется платная учетная запись Power BI, например учетная запись Power BI Pro или Power BI Premium. Однако отдельная плата за использование потоков не взимается. 

### <a name="extend-the-common-data-model-for-your-business-needs"></a>Расширение модели общих данных для конкретных бизнес-потребностей
Если организация желает расширить модель общих данных, потоки данных дают специалистам по бизнес-аналитике возможность настроить стандартные сущности или создать новые. Возможность самостоятельной настройки модели данных в сочетании с потоками данных позволяет создавать приложения и панели мониторинга Power BI, разработанные под конкретные нужды и задачи организации.

### <a name="define-dataflows-programmatically"></a>Определение потоков данных программным способом
Вы можете даже разработать собственные программные решения для создания потоков данных. Открытые API-интерфейсы и возможность программно создавать пользовательские файлы определений для потоков данных (model.json) позволяют создавать пользовательские решения, соответствующие уникальным характеристикам данных и потребностям в аналитике вашей организации. 

Открытые API-интерфейсы предоставляют разработчикам простой метод взаимодействия с Power BI и потоками данных.

### <a name="extend-your-capabilities-with-azure"></a>Расширение возможностей с помощью Azure
Azure Data Lake Storage 2-го поколения включается в каждую платную подписку Power BI (10 ГБ на каждого пользователя, 100 ТБ на каждый узел P1). Это позволит вам быстро начать самостоятельную подготовку данных в Azure Data Lake. 

В Power BI можно настроить хранение потока данных в корпоративной учетной записи Azure Data Lake Storage 2-го поколения. Подключив Power BI к подписке Azure, вы предоставите специалистам по разработке данных и анализу данных такие мощные средства Azure, как Машинное обучение Azure, Azure Databricks, Фабрика данных Azure и многие другие.

Power BI также может подключаться к папкам со схематизированными данными в формате модели общих данных, сохраненными в учетной записи Azure Data Lake Storage. Такие папки можно создавать во многих службах, в том числе в службах данных Azure. Подключившись к таким папкам, аналитики смогут легко применять данные из них в Power BI. 

Дополнительные сведения об Azure Data Lake Storage 2-го поколения и интеграции потоков данных, включая способы создание потоков данных в Azure Data Lake вашей организации, см. в статье [Потоки данных и интеграция Azure Data Lake (предварительная версия)](service-dataflows-azure-data-lake-integration.md).

## <a name="dataflow-capabilities-on-power-bi-premium"></a>Возможности потоков данных в Power BI Premium

Чтобы компоненты и рабочие нагрузки потока данных работали в подписке Power BI Premium, для этой емкости Premium должна быть включена рабочая нагрузка потоков данных. В следующей таблице приведены компоненты потока данных и их характеристики для учетной записи Power BI Pro, а также сравнение с подпиской Power BI Premium.


|Характеристики потока данных | Power BI Pro |   Power BI Premium |
|---------|---------|---------|
|Запланированное обновление| 8 в день|  48|
|Общий объем хранилища| 10 ГБ на пользователя  |100 ТБ на узел|
|Создание потока данных с помощью Power Query Online|    +   |+|
|Управление потоком данных в Power BI|   +|  +|
|Соединитель данных для потоков данных в Power BI Desktop|  +|  +|
|Интеграция с Azure|    +|  +|
|Вычисляемые сущности (преобразование в хранилище с помощью M) | |   +|
|Новые соединители|    +|  +|
|Добавочное обновление потока данных|  |   +|
|Выполнение в емкости Power BI Premium и параллельное выполнение преобразований|   |   +|
|Сущности, связанные с потоком данных| |        +|
|Стандартизированная схема и встроенная поддержка модели общих данных|  +|  +|

Дополнительные сведения о включении рабочих нагрузок потоков данных в емкости Premium см. в разделе [Настройка рабочих нагрузок в емкости Premium](service-admin-premium-workloads.md). Сейчас рабочие нагрузки потоков данных недоступны в емкостях с поддержкой нескольких регионов.

## <a name="summary-of-self-service-data-prep-for-big-data-in-power-bi"></a>Сводка по самостоятельной подготовке данных в Power BI для больших данных
Как упоминалось ранее в этой статье, в некоторых сценариях и примерах **потоки данных** позволяют усилить контроль над бизнес-данными и ускорить получение аналитических сведений по ним. С помощью стандартной модели данных (схемы), которая определена в модели общих данных, потоки данных могут импортировать ценные бизнес-данные и подготавливать их к моделированию и созданию бизнес-аналитики в течение очень короткого периода времени вместо нескольких месяцев, которые требовались для этого ранее. 

Размещая бизнес-данные в стандартизированном формате **модели общих данных**, специалисты по бизнес-аналитике и разработчики могут создавать приложения с быстрым, удобным и автоматизированным созданием визуализаций и отчетов. В качестве примеров можно упомянуть следующие возможности:


* сопоставление данных со стандартными сущностями модели общих данных, что позволяет объединять данные и использовать известные схемы для получения полезных сведений без дополнительной настройки;
* создание пользовательских сущностей для объединения данных по всей организации; 
* использование и обновление **внешних данных** в составе потока данных и реализация импорта этих данных для получения аналитических сведений;
* переход к разработке собственных потоков данных.


## <a name="next-steps"></a>Дальнейшие действия

В этой статье вы ознакомились с возможностями самостоятельной подготовки данных в Power BI для больших данных и узнали о различных вариантах их применения. В следующих статьях содержатся более подробные сведения о типичных сценариях применения потоков данных. 

* [Creating and using dataflows in Power BI (Preview)](service-dataflows-create-use.md) (Создание и использование потоков данных в Power BI (предварительная версия))
* [С помощью вычисляемых сущностями в Power BI Premium](service-dataflows-computed-entities-premium.md)
* [Использование потоков данных с локальными источниками данных](service-dataflows-on-premises-gateways.md)
* [Ресурсы для разработчиков для потоков данных Power BI](service-dataflows-developer-resources.md)
* [Интеграция потоки данных и Azure Data Lake](service-dataflows-azure-data-lake-integration.md)

Дополнительные сведения о Power Query и обновлении по расписанию содержатся в следующих статьях:
* [Общие сведения о запросах в Power BI Desktop](desktop-query-overview.md)
* [Настройка запланированного обновления](refresh-scheduled-refresh.md)

Дополнительные сведения о модели общих данных вы найдете в этой обзорной статье:
* [Что такое модель общих данных?](https://docs.microsoft.com/powerapps/common-data-model/overview)

