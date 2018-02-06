---
title: "Подключение к Application Insights с помощью Power BI"
description: "Application Insights для Power BI"
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 0ec1ca9bccabd923b67fc1f49da4b7321ba11141
ms.sourcegitcommit: c3be4de522874fd73fe6854333b379b85619b907
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2018
---
# <a name="connect-to-application-insights-with-power-bi"></a>Подключение к Application Insights с помощью Power BI
Используйте Power BI для создания эффективных пользовательских панелей мониторинга на базе телеметрии [Application Insights](https://azure.microsoft.com/documentation/articles/app-insights-overview/). Взгляните на данные телеметрии вашего приложения под новым углом. Сочетайте метрики из нескольких приложений или служб компонентов на одной информационной панели. Этот первый выпуск пакета содержимого Power BI для Application Insights включает в себя мини-приложения для распространенных метрик использования, например активных пользователей, просмотра страниц, сеансов, версии браузера и ОС, а также географического распределения пользователей на карте.

Подключите [пакет содержимого Application Insights для Power BI](https://app.powerbi.com/getdata/services/application-insights).

>[!NOTE]
>Для подключения требуется доступ к колонке общих сведений Application Insights в вашем приложении портала предварительной версии Azure. Дополнительные сведения о требованиях см. ниже.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
    ![Кнопка "Получить данные"](media/service-connect-to-application-insights/pbi_getdata.png)
2. В поле **Службы** выберите **Получить**.
   
    ![Кнопка "Получить службы"](media/service-connect-to-application-insights/pbi_getservices.png)
3. Выберите **Application Insights** > **Получить**.
   
    ![Пакет содержимого Application Insights](media/service-connect-to-application-insights/appinsights.png)
4. Укажите сведения о приложении, к которому вы хотите подключиться, включая **имя ресурса Application Insights**, **группу ресурсов** и **идентификатор подписки**. Дополнительные сведения см. в разделе [Поиск параметров Application Insights](#FindingAppInsightsParams) ниже.
   
    ![Диалоговое окно подключения Application Insights](media/service-connect-to-application-insights/pbi_contpkappinsitconnectndialog.png)    
5. Выберите **Вход** и следуйте инструкциям для подключения.
   
    ![Вход для подключения Application Insights](media/service-connect-to-application-insights/pbi_contpkappinsitconnectn2.png)
6. Процесс импорта начинается автоматически. После завершения отображается уведомление, а в области навигации появляется новая информационная панель, отчет и набор данных, отмеченные звездочкой.  Выберите панель мониторинга, чтобы просмотреть импортированные данные.
   
    ![Информационная панель Application Insights](media/service-connect-to-application-insights/pbi_contpkappinsitdash.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](power-bi-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="whats-included"></a>Содержимое
Пакет содержимого Application Insights включает следующие таблицы и метрики:  

     ´´´
    - ApplicationDetails  
    - UniqueUsersLast7Days   
    - UniqueUsersLast30Days   
    - UniqueUsersDailyLast30Days  
    - UniqueUsersByCountryLast7Days  
    - UniqueUsersByCountryLast30Days   
    - PageViewsDailyLast30Days   
    - SessionsLast7Days   
    - SessionsLast30Days  
    - PageViewsByBrowserVersionDailyLast30Days   
    - UniqueUsersByOperatingSystemLast7Days   
    - UniqueUsersByOperatingSystemLast30Days    
    - SessionsDailyLast30Days   
    - SessionsByCountryLast7Days   
    - SessionsByCountryLast30Days   
    - PageViewsByCountryDailyLast30Days  
   ´´´ 

<a name="FindingAppInsightsParams"></a>

## <a name="finding-parameters"></a>Поиск параметров
Все нужные значения — имя, группу ресурсов и идентификатор подписки — можно найти на портале Azure. При выборе имени откроется подробное представление, где с помощью раскрывающегося списка основных сведений можно найти все необходимые значения.

![Параметры Application Insights](media/service-connect-to-application-insights/pbi_contpkappinsitparams.png)

Скопируйте эти значения и вставьте их в поля в Power BI:

![Параметры Application Insights](media/service-connect-to-application-insights/pbi_contpkappinsitparam2.png)

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Получение данных в Power BI](service-get-data.md)
