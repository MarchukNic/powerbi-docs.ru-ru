---
title: Динамические данные служб SQL Server Analysis в Power BI
description: Динамические данные служб SQL Server Analysis в Power BI. Реализуются через источник данных, настроенный для корпоративного шлюза.
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
author: Minewiskan
ms.author: owend
manager: kfile
ms.reviewer: ''
ms.custom: ''
ms.date: 08/10/2017
LocalizationGroup: Data from databases
ms.openlocfilehash: 51efec6c78dbb29b9c3dc760284c7bb3c8711bdc
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "64769933"
---
# <a name="sql-server-analysis-services-live-data-in-power-bi"></a>Динамические данные служб SQL Server Analysis в Power BI

В Power BI существует два способа подключения к серверу динамических данных SQL Server Analysis Services. Вы можете подключиться к серверу SQL Server Analysis Services на вкладке **Получение данных** или подключиться к [файлу Power BI Desktop](service-desktop-files.md) или [книге Excel](service-excel-workbook-files.md), которые уже подключены к серверу служб Analysis Services. Как правило, корпорация Майкрософт настоятельно рекомендует использовать Power BI Desktop, так как это приложение располагает полным набором инструментов и возможностью хранения резервной копии файла Power BI Desktop на локальном компьютере.

>[!IMPORTANT]
> * Для динамического подключения к серверу Analysis Services администратор должен установить и настроить локальный шлюз данных. Дополнительную информацию см. в разделе [Локальный шлюз данных](service-gateway-onprem.md).
> * При использовании шлюза данные размещены локально.  Отчеты, созданные на их основе, сохраняются в службе Power BI. 
> * [Вопросы и ответы на естественном языке](service-q-and-a-direct-query.md) — предварительная версия функции для интерактивных подключений к Analysis Services.

## <a name="to-connect-to-a-model-from-get-data"></a>Подключение к модели на вкладке "Получение данных"

1. В разделе **Моя рабочая область** щелкните **Получить данные**. Можно также перейти в рабочую область группы, если она доступна.

   ![Подключитесь, чтобы кнопки "данные"](media/sql-server-analysis-services-tabular-data/connecttoas_getdatabutton.png)

2. Щелкните **Базы данных и другое**.

   ![Подключение для получения данных 1](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_1.png)

3. Выберите **Службы SQL Server Analysis Services** > **Подключение**.

   ![Подключение для получения данных 2](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_2.png)

4. Выберите сервер. Если в списке нет указанных здесь серверов, это означает, что не настроен шлюз и источник данных или учетная запись отсутствует на вкладке **Пользователи** источника данных в шлюзе. Обратитесь к администратору.

5. Выберите модель для подключения. Это может быть многомерная или табличная модель.

После подключения к модели она появится на вашем сайте Power BI в разделе **Моя рабочая область/Наборы данных**. Если вы перешли в рабочую область группы, набор данных будет отображаться в группе.

![Подключитесь к набору данных](media/sql-server-analysis-services-tabular-data/connecttoas_dataset_5.png)

## <a name="dashboard-tiles"></a>Плитки панели мониторинга

Если закрепить визуальные элементы из отчета на панели мониторинга, закрепленные плитки будут автоматически обновляться каждые 10 минут. При обновлении данных на локальном сервере данных Analysis Services плитки автоматически обновляются через 10 минут.

## <a name="common-issues"></a>Распространенные проблемы

* Ошибка "Не удалось загрузить схему модели". Эта ошибка происходит, когда пользователь, подключающийся к службам SQL Server Analysis Services, не имеет доступа к базе данных, кубу и модели SQL Server Analysis Services.

## <a name="next-steps"></a>Дальнейшие действия

* [On-premises data gateway (Локальный шлюз данных)](service-gateway-onprem.md)  
* [Управление источниками данных служб Analysis Services](service-gateway-enterprise-manage-ssas.md)  
* [Устранение неполадок локального шлюза данных](service-gateway-onprem-tshoot.md)  

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)