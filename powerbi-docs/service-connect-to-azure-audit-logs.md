---
title: "Подключение к журналам аудита Azure с помощью Power BI"
description: "Журналы аудита Azure для Power BI"
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
ms.openlocfilehash: cb52b8dc6aefc199ef09946bf8b58c98171c5aba
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-azure-audit-logs-with-power-bi"></a>Подключение к журналам аудита Azure с помощью Power BI
Пакет контента "Журналы аудита Azure" для Power BI позволяет анализировать и визуализировать информацию, хранящуюся в журналах аудита. Power BI извлекает данные, создает стандартную панель мониторинга и строит на основе этих данных отчеты.

[Подключитесь к пакету содержимого журналов аудита Azure](https://app.powerbi.com/getdata/services/azure-audit-logs) или прочтите дополнительные сведения об [интеграции журналов аудита Azure](https://powerbi.microsoft.com/integrations/azure-audit-logs) с Power BI.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.  
   
    ![](media/service-connect-to-azure-audit-logs/getdata.png)
2. В поле **Службы** выберите **Получить**.  
   
    ![](media/service-connect-to-azure-audit-logs/services.png) 
3. Выберите пункты **Журналы аудита Azure** > **Получить**.  
   
   ![](media/service-connect-to-azure-audit-logs/azureauditlogs.png)
4. При появлении запроса введите **идентификатор подписки Azure**. Сведения о том, как узнать свой [идентификатор подписки](#FindingParams), см. ниже.   
   
    ![](media/service-connect-to-azure-audit-logs/parameters.png)
5. В качестве **метода проверки подлинности** выберите **oAuth2** \> **Войти**.
   
    ![](media/service-connect-to-azure-audit-logs/creds.png)
6. Введите данные своей учетной записи для входа в систему.
   
    ![](media/service-connect-to-azure-audit-logs/login.png)
7. Power BI извлечет данные журналов аудита Azure и создаст информационную панель и отчет, готовые к использованию. 
   
    ![](media/service-connect-to-azure-audit-logs/dashboard.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](service-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="system-requirements"></a>Требования к системе
Для пакета содержимого журналов аудита требуется доступ к журналам аудита на портале Azure. Дополнительные сведения см. [здесь](https://azure.microsoft.com/en-us/documentation/articles/insights-debugging-with-events/).

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Поиск параметров
Вы можете определить свой идентификатор подписки одним из двух простых способов.

1. На сайте https://portal.azure.com -&gt; Обзор -&gt; Подписки -&gt; Идентификатор подписки
2. На сайте https://manage.windowsazure.com -&gt; Параметры -&gt; Идентификатор подписки

Идентификатор подписки представляет собой длинную последовательность цифр и букв, как в шаге \# 4 приведенного выше примера. 

## <a name="troubleshooting"></a>Устранение неполадок
Если происходит ошибка из-за недопустимых учетных данных или при попытке выполнить обновление, попробуйте удалить все экземпляры пакета содержимого журналов аудита Azure и повторите попытку подключения.

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)  
[Power BI — основные понятия](service-basic-concepts.md)  
