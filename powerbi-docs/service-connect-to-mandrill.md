---
title: "Подключение к Mandrill с помощью Power BI"
description: "Mandrill для Power BI"
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
ms.openlocfilehash: 976ca32f0c43f6d8412f9468dc9f61ab9768fa4c
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-mandrill-with-power-bi"></a>Подключение к Mandrill с помощью Power BI
Пакет содержимого для Power BI извлекает данные из вашей учетной записи Mandrill и создает панель мониторинга, набор отчетов и набор данных, которые позволяют анализировать ваши данные. Решения аналитики Mandrill позволяют быстро анализировать кампании рассылки или маркетинговые кампании. Данные обновляются ежедневно, так что вам всегда доступны последние сведения.

Подключитесь к [пакету содержимого Mandrill для Power BI](http://app.powerbi.com/getdata/services/mandrill).

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
    ![](media/service-connect-to-mandrill/getdata.png)
2. В поле **Службы** выберите **Получить**.
   
    ![](media/service-connect-to-mandrill/services.png)
3. Выберите **Mandrill** > **Получить**.
   
    ![](media/service-connect-to-mandrill/mandrill.png)
4. Выберите в качестве **метода проверки подлинности****Ключ** и укажите ваш ключ API. Этот ключ можно найти на вкладке **Параметры** информационной панели Mandrill. Выберите **Вход**, чтобы начать импорт. Это может занять несколько минут в зависимости от объема данных в вашей учетной записи.
   
    ![](media/service-connect-to-mandrill/auth.png)
5. После импорта данных в Power BI в области навигации слева появятся новая панель мониторинга, отчеты и набора данных. Это панель мониторинга по умолчанию, которую Power BI создает для отображения данных.
   
    ![](media/service-connect-to-mandrill/mandrill-dashboard1.jpg)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](service-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Power BI — основные понятия](service-basic-concepts.md)
