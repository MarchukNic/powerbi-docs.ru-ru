---
title: "Подключение к Центру разработки для Windows с помощью Power BI"
description: "Windows Dev Center для Power BI"
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
ms.openlocfilehash: d88e10b4ee2e76444fccec0edabddd2a123d6b62
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-windows-dev-center-with-power-bi"></a>Подключение к Центру разработки для Windows с помощью Power BI
С помощью этого пакета содержимого для Power BI вы сможете просматривать и отслеживать аналитические данные приложения Центра разработки для Windows в службе Power BI. Данные автоматически обновляются раз в день.

Подключите [пакет содержимого Центра разработки для Windows](https://app.powerbi.com/getdata/services/devcenter) для Power BI.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
   ![](media/service-connect-to-windows-dev-center/getdata.png)
2. В поле **Службы** выберите **Получить**.
   
   ![](media/service-connect-to-windows-dev-center/services.png)
3. Выберите **Центр разработки для Windows** \> **Получить**.
   
   ![](media/service-connect-to-windows-dev-center/windowsdev.png)
4. Введите идентификатор приложения, которое вам принадлежит, и нажмите кнопку «Далее». Сведения о том, как [найти эти параметры](#FindingParams), см. ниже.
   
   ![](media/service-connect-to-windows-dev-center/params.png)
5. В качестве **метода проверки подлинности** выберите **oAuth2** \> **Войти**. Когда будет предложено, введите свои учетные данные Azure Active Directory, связанные с вашей учетной записью Центра разработки для Windows (дополнительные сведения см. в [требованиях к системе](#Requirements)).
   
    ![](media/service-connect-to-windows-dev-center/creds.png)
   
    ![](media/service-connect-to-windows-dev-center/creds2.png)
6. После утверждения процесс импорта начнется автоматически. После завершения в области навигации появятся новая панель мониторинга, отчет и модель. Чтобы просмотреть импортированные данные, выберите панель мониторинга. Чтобы перейти к соответствующим отчетам, выберите плитку.
   
    ![](media/service-connect-to-windows-dev-center/dashboard.png)
   
    ![](media/service-connect-to-windows-dev-center/report.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](service-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="whats-included"></a>Содержимое
Пакет содержимого Центра разработки для Windows для Power BI обеспечивает доступ к аналитическим данным для приложения, сведениям о его работоспособности, покупках в приложении, оценках и отзывах. Данные доступны за последние три месяца, причем этот диапазон является динамическим (то есть содержимое обновляется по мере обновления набора данных).

<a name="Requirements"></a>

## <a name="system-requirements"></a>Требования к системе
Для работы с этим пакетом содержимого у вас должно быть опубликовано хотя бы одно приложение в Магазине Windows, а также необходима учетная запись в Центре разработки для Windows (дополнительные сведения приведены [здесь](https://msdn.microsoft.com/windows/uwp/publish/manage-account-users)).

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Поиск параметров
Чтобы найти идентификатор своего приложения, зайдите на страницу удостоверения приложения (раздел управления приложениями).

Идентификатор указан в конце URL-адреса для Магазина Windows 10: https://www.microsoft.com/store/apps/ **{идентификатор_приложения}**

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Получение данных в Power BI](service-get-data.md)
