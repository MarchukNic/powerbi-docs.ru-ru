---
title: "Обновление набора данных, созданного из файла данных с разделителями-запятыми (CSV) в OneDrive"
description: "Обновление набора данных, созданного из файла данных с разделителями-запятыми (CSV) в OneDrive"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 214f78c86a43341d177d72f60a2a5ecce4d8f8d5
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2017
---
# <a name="refresh-a-dataset-created-from-a-csv-file-on-onedrive-or-sharepoint-online"></a>Обновление набора данных, созданного из файла CSV в OneDrive или SharePoint Online
## <a name="what-are-the-advantages"></a>Каковы преимущества?
При подключении к CSV-файлу, расположенному в OneDrive или SharePoint Online, в Power BI создается набор данных. Затем данные из CSV-файла импортируются в набор данных в Power BI. После этого Power BI автоматически подключается к файлу и обновляет все изменения, используя набор данных в Power BI. Если вы изменяете CSV-файл в OneDrive или SharePoint Online и сохраняете его, эти изменения будут отражены в Power BI, обычно в течение одного часа. Все визуализации в Power BI, основанные на этом наборе данных, также обновляются автоматически.

Если ваши файлы находятся в общей папке OneDrive для бизнеса или SharePoint Online, с одним и тем же файлом могут работать другие пользователи. После сохранения все внесенные изменения автоматически обновляются в Power BI, обычно в течение часа.

Многие организации запускают процессы, которые автоматически запрашивают данные из баз данных. Эти данные ежедневно сохраняются в виде CSV-файла. Если файл хранится в OneDrive или SharePoint Online и ежедневно перезаписывается, а не создается каждый день с другим именем, вы можете подключиться к этому файлу в Power BI. Набор данных, который подключается к файлу, будет синхронизирован вскоре после обновления файла в OneDrive или SharePoint Online. Все визуализации, основанные на этом наборе данных, также обновляются автоматически.

## <a name="whats-supported"></a>Что поддерживается?
Файлы данных с разделителями-запятыми представляют собой простые текстовые файлы, поэтому подключения к внешним источникам данных и отчетам не поддерживаются. Вы не можете запланировать обновление набора данных, созданного из файла с разделителями-запятыми. Однако если файл находится в OneDrive или SharePoint Online, Power BI будет каждый час автоматически синхронизировать любые изменения в файле с набором данных.

## <a name="onedrive-or-onedrive-for-business-whats-the-difference"></a>OneDrive или OneDrive для бизнеса. В чем разница?
При наличии личного OneDrive и OneDrive для бизнеса рекомендуется хранить все файлы, которые нужно подключить к Power BI, в OneDrive для бизнеса. И вот почему. Скорее всего, для доступа к этим хранилищам вы используете две учетные записи.

Подключение к OneDrive для бизнеса в Power BI обычно выполняется автоматически, поскольку чаще всего для входа в Power BI и в OneDrive для бизнеса используется одна и та же учетная запись. Однако в личное хранилище OneDrive вы, скорее всего, входите с помощью другой [учетной записи Майкрософт](http://www.microsoft.com/account/default.aspx).

При выполнении входа с использованием учетной записи Майкрософт обязательно установите флажок "Оставаться в системе". После этого Power BI сможет синхронизировать все обновления с наборами данных в Power BI.

![](media/refresh-csv-file-onedrive/refresh_signin_keepmesignedin.png)

При внесении изменений в CSV-файл в OneDrive, который не удается синхронизировать с набором данных в Power BI из-за изменения учетных данных вашей учетной записи Майкрософт, потребуется подключиться к файлу и снова импортировать его из своего личного хранилища OneDrive.

## <a name="when-things-go-wrong"></a>Действия в случае возникновения проблем
Если данные в CSV-файле в OneDrive изменяются и эти изменения не отражаются в Power BI, скорее всего, Power BI не удается подключиться к OneDrive. Попробуйте подключиться к файлу и повторить его импорт. Если отображается запрос на вход, обязательно установите флажок **Оставаться в системе**.

## <a name="next-steps"></a>Дальнейшие действия
[Средства для устранения неполадок при обновлении](service-gateway-onprem-tshoot.md)
[Устранение неполадок в сценариях обновления](refresh-troubleshooting-refresh-scenarios.md)

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](https://community.powerbi.com/)
