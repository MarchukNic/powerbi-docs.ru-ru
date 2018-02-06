---
title: "Подключение к Acumatica с помощью Power BI"
description: "Acumatica для Power BI"
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
ms.openlocfilehash: 66d1544797008b4ed4c0ce2c7acd041aa60b967b
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-acumatica-with-power-bi"></a>Подключение к Acumatica с помощью Power BI
Пакет содержимого Acumatica для Power BI позволяет быстро анализировать данные возможностей. Power BI извлекает данные, включая возможности, учетные записи и клиентов, затем создает стандартную панель мониторинга и связанные отчеты, основанные на этих данных.

Подключите [пакет содержимого Acumatica](https://app.powerbi.com/getdata/services/acumatica) или прочтите дополнительные сведения об [интеграции Acumatica](https://powerbi.microsoft.com/integrations/acumatica) с Power BI.

>[!NOTE]
>Для этого пакета содержимого требуется Acumatica версии 5.2 или более поздней.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
   ![](media/service-connect-to-acumatica/getdata3.png)
2. В поле **Службы** выберите **Получить**.
   
   ![](media/service-connect-to-acumatica/getdata2.png)
3. Выберите **Acumatica** \> **Получить**.
   
   ![](media/service-connect-to-acumatica/acumatica.png)
4. Введите конечную точку OData Acumatica. Конечная точка OData позволяет внешней системе запрашивать данные из Acumatica. Конечная точка OData Acumatica имеет следующий формат и должна использовать протокол HTTPS:
   
     https://[sitedomain]/odata/[companyname]
   
   Название организации требуется указывать, только если выполняется развертывание в нескольких компаниях. Ниже приведены дополнительные сведения о том, как найти этот параметр в вашей учетной записи Acumatica.
   
   ![](media/service-connect-to-acumatica/parameters.png)
5. Выберите **обычную**проверку подлинности. Введите имя пользователя и пароль из учетной записи Acumatica, затем щелкните **Вход**.
   
    ![](media/service-connect-to-acumatica/creds2.png)
6. После импорта данных в Power BI в области навигации слева появятся новая панель мониторинга, отчеты и набора данных. Новые элементы помечены желтой звездочкой (\*), которая пропадает после выбора. При выделении панели мониторинга отобразится разметка, аналогичная следующей:
   
    ![](media/service-connect-to-acumatica/dashboard.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](power-bi-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="system-requirements"></a>Требования к системе
Для этого пакета содержимого требуется Acumatica версии 5.2 или более поздней. Версию можно узнать у администратора Acumatica.

## <a name="finding-parameters"></a>Поиск параметров
**Конечная точка Acumatica OData**

Конечная точка OData Acumatica имеет следующий формат и должна использовать протокол HTTPS:

    https://[sitedomain]/odata/[companyname]

Если вы выполнили вход в систему Acumatica, домен сайта приложения можно найти в адресной строке браузера. В приведенном ниже примере доменом сайта является https://pbi.acumatica.com, поэтому необходимой конечной точкой OData будет https://pbi.acumatica.com/odata.

 ![](media/service-connect-to-acumatica/url.png)

Название организации требуется указывать, только если выполняется развертывание в нескольких компаниях. Эти сведения можно найти на странице входа Acumatica.

![](media/service-connect-to-acumatica/signin2.png)

## <a name="troubleshooting"></a>Устранение неполадок
Если вы не можете войти в систему, убедитесь, что указанная вами конечная точка OData Acumatica имеет правильный формат.

    https://<application site domain>/odata/<company name>

Если возникают проблемы при подключении, узнайте у администратора, какую версию Acumatica вы используете. Этот пакет содержимого требует версию 5.2 или более позднюю.

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Получение данных в Power BI](service-get-data.md)
