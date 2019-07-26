---
title: Уведомления о перебое в работе служб
description: Сведения о том, как получать уведомления по электронной почте при нарушении или снижении производительности в службе Power BI.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 07/19/2019
ms.author: mblythe
ms.openlocfilehash: 0bb78e29cc3e9b9792d5916050179703281aa01a
ms.sourcegitcommit: 850e7883e21190151684e32f4d957beecd08e959
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2019
ms.locfileid: "68366756"
---
# <a name="service-interruption-notifications"></a>Уведомления о перебое в работе служб

Крайне важно иметь представление о доступности критически важных бизнес-приложений. Power BI обеспечивает уведомление об инциденте, поэтому вы можете получать сообщения электронной почты при нарушении или снижении производительности в службе. Хотя благодаря Соглашению об уровне обслуживания (SLA) в 99,9 % для Power BI такие события возникают нечасто, мы хотим проинформировать вас об этом. На следующем снимке экрана показан тип сообщения электронной почты, которое вы получите при включении уведомлений:

![Уведомление по электронной почте об обновлении](media/service-interruption-notifications/refresh-notification-email.png)

Сейчас мы отправляем сообщения электронной почты для следующих _сценариев надежности_:

- Надежность открытия отчетов
- Надежность обновления моделей
- Надежность обновления запросов

После разрешения инцидента вы получите сообщение электронной почты с дальнейшими указаниями.

> [!NOTE]
> Сейчас эта функция доступна только для выделенных емкостей в Power BI Premium. Она недоступна для общей емкости.

## <a name="enable-notifications"></a>Включение уведомлений

Администратор клиента Power BI включает уведомления на портале администрирования:

1. Найдите или создайте группу безопасности с включенной поддержкой электронной почты, которая должна получать уведомления.

1. На портале администрирования выберите **Параметры клиента**. В разделе **Параметры справки и поддержки** разверните узел **Получать уведомления о сбоях службы и инцидентах по электронной почте**.

1. Включите уведомления, войдите в группу безопасности и нажмите кнопку **Применить.**

    ![Включение уведомлений службы](media/service-interruption-notifications/enable-notifications.png)

> [!NOTE]
> Power BI отправляет уведомления из учетной записи no-reply-powerbi@microsoft.com. Убедитесь, что эта учетная запись внесена в список разрешений, чтобы уведомления не попадали в папку нежелательной почты.

## <a name="next-steps"></a>Дальнейшие действия

[Варианты поддержки Power BI Pro и Power BI Premium](service-support-options.md)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)