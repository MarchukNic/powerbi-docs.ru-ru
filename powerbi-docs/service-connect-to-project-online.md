---
title: Подключение к Project Online с помощью Power BI
description: Project Online для Power BI
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: a6ada87813593fd0f06d7870fa1727bc35fe7d47
ms.sourcegitcommit: fe8a25a79f7c6fe794d1a30224741e5281e82357
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2019
ms.locfileid: "68324939"
---
# <a name="connect-to-project-web-app-with-power-bi"></a>Подключение к Project Web App с помощью Power BI
Microsoft Project Web App — это гибкое решение для управления портфелями проектов (PPM) и повседневной работы. Project Web App позволяет организациям приступить к работе, расставить приоритеты по инвестициям в портфель проектов, а также добиться запланированного уровня ценности для бизнеса. Приложение-шаблон Project Web App для Power BI позволяет использовать функции аналитики Project Web App для управления проектами, портфелями и ресурсами.

Подключитесь к [приложению-шаблону Project Web App](https://appsource.microsoft.com/product/power-bi/pbi_msprojectonline.pbi-microsoftprojectwebapp) для Power BI.

## <a name="how-to-connect"></a>Способы подключения

   ![](media/service-connect-to-project-online/GetApps.png)
1. Выберите **Приложения** в левой области навигации, а затем щелкните **Получить приложения** в правом верхнем углу.
2. В поле **Службы** выберите **Получить**.
   
   ![](media/service-connect-to-project-online/AppSource.png)
3. В AppSource на вкладке **Приложения** выполните поиск **приложения Microsoft Project Web**.
   
4. Вы получите сообщение **Установить это приложение Power BI?** , выберите **Установить**. 

   ![](media/service-connect-to-project-online/ProjectTile.png)
5. В области **Приложения** выберите заголовок **приложения-шаблона Microsoft Project**. 
   
   ![](media/service-connect-to-project-online/getstarted.png)
6. На экране **Начало работы с новым приложением** выберите **Подключиться к данным**.
   
   ![](media/service-connect-to-project-online/mproject.png)
7. В текстовом поле **URL-адрес Project Web App** введите URL-адрес для Project Web App (PWA), к которому требуется подключиться.  Обратите внимание, что в личном домене ситуация может отличаться от приведенной в примере. В текстовом поле **Язык сайта PWA** введите номер, который соответствует нужному языку сайта PWA. Введите одну цифру "1" для английского языка, "2" для французского языка, "3" для немецкого языка, "4" для португальского (Бразилия), "5" для португальского (Португалия) и "6" для испанского языка. 
   
   ![](media/service-connect-to-project-online/params.png)
8. В качестве метода проверки подлинности выберите **oAuth2** \> **Войти**. При появлении запроса введите учетные данные Project Web App и пройдите проверку подлинности.

    
Обратите внимание, что вам нужно использовать разрешения на уровне средства просмотра портфеля, диспетчера портфелей или администратора для Project Web App, к которому вы подключаетесь.

9. Вы увидите уведомление, указывающее на загрузку данных. В зависимости от размера вашей учетной записи это может занять некоторое время. После импорта данных в Power BI появится содержимое новой рабочей области. Возможно, вам потребуется обновить набор данных, чтобы получить последние обновления. 

После импорта данных в Power BI в левой области навигации появится отчет из 13 страниц и набор данных. 

10. После подготовки отчетов вы можете приступить к изучению данных Project Web App. Приложение-шаблон включает 13 удобных и подробных отчетов по обзору портфеля (6 страниц отчетов), обзору ресурсов (5 страниц отчетов) и состоянию проекта (2 страницы отчетов). 

   ![](media/service-connect-to-project-online/report1.png)
   
   ![](media/service-connect-to-project-online/report3.png)
   
   ![](media/service-connect-to-project-online/report2.png)

**Дальнейшие действия**

* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**

**Расширение приложения-шаблона**

Загрузка [PBIT-файла в GitHub](https://github.com/OfficeDev/Project-Power-BI-Content-Packs) для дальнейшей настройки и обновления пакета содержимого

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Получение данных в Power BI](service-get-data.md)

