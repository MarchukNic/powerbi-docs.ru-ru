---
title: "Подключение к Marketo с помощью Power BI"
description: "Marketo для Power BI"
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
ms.openlocfilehash: fb2ebb35dd8a43d477bb300b7f601dd358339450
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-marketo-with-power-bi"></a>Подключение к Marketo с помощью Power BI
Пакет содержимого Power BI для Marketo позволяет получить подробные сведения об учетной записи Marketo с данными о потенциальных клиентах и их действиях. При создании этого подключения вы извлечете данные и автоматически получите панель мониторинга и связанные отчеты на основе этих данных.

Подключитесь к [пакету содержимого Marketo](https://app.powerbi.com/getdata/services/marketo) для Power BI.

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
   ![](media/service-connect-to-marketo/pbi_getdata.png)
2. В поле **Службы** выберите **Получить**.
   
   ![](media/service-connect-to-marketo/pbi_getservices.png) 
3. Выберите **Marketo** \> **Получить**.
   
   ![](media/service-connect-to-marketo/marketo.png)
4. Введите конечную точку REST Marketo, предоставленную вам Marketo или администратором Marketo, и нажмите кнопку "Далее".
   
   ![](media/service-connect-to-marketo/pbi_marketoconnect.png)
   
   Подробнее о конечной точке REST Marketo: [http://developers.marketo.com/documentation/rest/endpoint-url/](http://developers.marketo.com/documentation/rest/endpoint-url/).
5. Используя **обычную** проверку подлинности, введите идентификатор клиента как **имя пользователя** и секрет клиента как **пароль**. Идентификатор и секрет клиента предоставляются Marketo или администратором Marketo ([http://developers.marketo.com/documentation/rest/custom-service/](http://developers.marketo.com/documentation/rest/custom-service/)). 
   
   ![](media/service-connect-to-marketo/pbi_marketosignin.png)
   
   Это предоставляет пакету содержимого *Marketo для Power BI* доступ к вашим данным [аналитики Marketo](https://powerbi.microsoft.com/integrations/marketo) и позволяет анализировать их в Power BI. Данные обновляются раз в день.
6. После подключения к учетной записи Marketo загружается панель мониторинга со всеми данными:
   
   ![](media/service-connect-to-marketo/pbi_marketodash.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](service-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="whats-included"></a>Содержимое
В Marketo для Power BI, в которой между текущей датой и датой год назад произошло действие, доступны следующие данные:

| Имя таблицы | Описание |
| --- | --- |
| EmailActivities |Данные о сообщениях электронной почты, отправленных интересам и контактам, с подробными сведениями об устройствах, категориях, числе и проценте отклоненных, обработанных и открытых сообщений и имени программы. Действия по электронной почте, показанные в Power BI, — это абсолютный отчет о возможности доставки сообщений, он не применяет дополнительную логику к данным. Из-за этого возможно получение различных результатов в клиенте Marketo и в Power BI. |
| ProgramActivites |Данные о программах, для которых изменилось состояние. К ним относятся: причина, успех, число и процент приобретения программ, а также число и процент успешных выполнений программы. |
| WebPageActivities |Данные о посещении пользователями веб-страницы, включая агент поиска, агент пользователя, веб-страницу и время дня. |
| Datetable |Даты от сегодняшней даты до соответствующей даты в прошлом году.  Позволяет анализировать данные Marketo по дате. |
| Лиды |Сведения об интересе, такие как компания, размер дохода, число сотрудников, страна, отрасль, оценка и состояние интереса. Лиды извлекаются на основе их присутствия в действиях электронной почты, программы и веб-страницы. |

Все даты указаны в формате UTC. Даты зависят от того, какой часовой пояс используется для учетной записи (как и в клиенте Marketo).

## <a name="system-requirements"></a>Требования к системе
* У учетной записи Marketo, используемой для подключения, есть разрешения для доступа к лидам и действиям.
* Достаточное число вызовов API для подключения к данным.  У Marketo есть API для каждой учетной записи.  При достижении предела вы не сможете загружать данные в Power BI. 

**Сведения об ограничениях API**

Для импорта данных из Marketo используется API Marketo. К каждому клиенту Marketo применяется общее ограничение в 10 000 вызовов API в день, которые являются общими для всех приложений, использующих API-интерфейсы Marketo. Вы можете использовать API для других средств интеграции, а также для интеграции Power BI. Подробнее об интерфейсах API: <http://developers.marketo.com/documentation/rest/>.

Количество вызовов API, выполняемых Power BI к Marketo, зависит от объема данных в вашей учетной записи Marketo. Power BI импортирует всех лидов и все действия за последний год. Ниже приведен пример данных из Marketo и число вызовов API, используемых Power BI при импорте.  

| Тип данных | Число строк | Вызовы API |
| --- | --- | --- |
| Сведения об интересах |15 000 |50 |
| Действия электронной почты |150 000 |1000 |
| Действия программы |15 000 |100 |
| Веб-действия |150 000 |1000 |
| Изменения программы |7500 |50 |
| **Всего вызовов API** | |**2200** |

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Получение данных для Power BI](service-get-data.md)

[Блог Power BI. Мониторинг и анализ данных Marketo с помощью Power BI](http://blogs.msdn.com/b/powerbi/archive/2015/03/19/monitor-and-analyze-your-marketo-data-with-power-bi.aspx)
