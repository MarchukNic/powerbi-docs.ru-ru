---
title: Обновление набора данных, созданного из файла Power BI Desktop в OneDrive (на локальном диске)
description: Обновление набора данных, созданного из файла Power BI Desktop на локальном диске
author: mgblythe
manager: kfile
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 06/04/2019
ms.author: mblythe
LocalizationGroup: Data refresh
ms.openlocfilehash: 58727627656a3cb22ad7fce626d0c7e6ce746440
ms.sourcegitcommit: 206806d8ddb6bdfc322c1a46fb34a1b0678acba2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2019
ms.locfileid: "66816484"
---
# <a name="refresh-a-dataset-created-from-a-power-bi-desktop-file-on-a-local-drive"></a>Обновление набора данных, созданного из файла Power BI Desktop на локальном диске

## <a name="whats-supported"></a>Что поддерживается?

В Power BI поддерживаются функции "Обновить сейчас" и "Расписание обновлений" для наборов данных, которые созданы из файлов Power BI Desktop, импортированных с локального диска, когда операция "Получение данных" или редактор запросов используется для подключения и загрузки данных из любого из следующих источников данных.

### <a name="power-bi-gateway---personal"></a>Шлюз Power BI — персональный

- Все источники данных в сети, отображаемые в редакторе запросов и разделе "Получение данных" в Power BI Desktop.
- Все локальные источники данных, отображаемые в редакторе запросов и разделе "Получение данных" в Power BI Desktop, кроме файла Hadoop (HDFS) и Microsoft Exchange.

<!-- Refresh Data sources-->
[!INCLUDE [refresh-datasources](./includes/refresh-datasources.md)]

> [!NOTE]
> Следует установить и запустить шлюз, чтобы служба Power BI могла подключаться к локальным источникам данных и обновлять набор данных.
>
>

Вы можете выполнить однократное ручное обновление в Power BI Desktop, нажав кнопку **Обновить** на вкладке "Главная" ленты. При нажатии этой кнопки **Обновить** данные в модели *файла* обновляются измененными данными из исходного источника данных. Такое обновление, выполняемое прямо из приложения Power BI Desktop, отличается от ручного или запланированного обновления в Power BI, и важно понимать, чем именно они различаются.

![Обновить](media/refresh-desktop-file-local-drive/pbix-refresh.png)

При импорте файла Power BI Desktop с локального диска данные вместе с другими сведениями о модели загружаются в набор данных в службе Power BI. В службе Power BI (не Power BI Desktop) требуется обновлять данные в наборе данных, так как именно на нем основаны ваши отчеты в службе Power BI. Так как источники данных являются внешними, вы можете вручную обновить набор данных с помощью функции **Обновить сейчас** или настроить **Расписание обновления**.

При обновлении набора данных служба Power BI не подключается к файлу на локальном диске для запроса обновленных данных. Она использует данные в наборе данных для подключения непосредственно к источникам данных, чтобы получить обновленные данные, которые затем загружает в набор данных.

> [!NOTE]
> Обновленные данные в наборе данных не синхронизируются с файлом на локальном диске.
>
>

## <a name="how-do-i-schedule-refresh"></a>Как составить расписание обновления?

При настройке расписания обновления служба Power BI подключается непосредственно к источникам данных, используя сведения о подключении и учетные данные в наборе данных для запроса обновленных данных, а затем загружает их в набор данных. Также обновляются все визуализации в отчетах и информационных панелях, основанных на этом наборе данных в службе Power BI.

Дополнительные сведения о настройке запланированного обновления см. в разделе [Настройка запланированного обновления](refresh-scheduled-refresh.md).

## <a name="when-things-go-wrong"></a>Действия в случае возникновения проблем

Возникающие проблемы обычно вызваны тем, что Power BI не удается выполнить вход в источники данных либо набор данных подключается к локальному источнику данных, а шлюз находится вне сети. Убедитесь, что служба Power BI может выполнить вход в источники данных. Если изменяется пароль, который вы используете для входа в источник данных или Power BI выполняет выход из источника данных, не забудьте повторно войти в источники данных в разделе «Учетные данные источника данных».

Не забудьте оставить флажок **Отправлять мне уведомления по электронной почте об ошибке обновления** установленным. Вам необходимо оперативно получать информацию о сбое запланированного обновления.

## <a name="troubleshooting"></a>Устранение неполадок

Иногда обновление данных может завершиться неправильно. Как правило, проблема связана со шлюзом. Ознакомьтесь со статьями об устранении неполадок со шлюзом и узнайте о соответствующих средствах и известных проблемах.

- [Устранение неполадок локального шлюза данных](service-gateway-onprem-tshoot.md)
- [Устранение неполадок с Power BI Gateway — Personal](service-admin-troubleshooting-power-bi-personal-gateway.md)

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)

