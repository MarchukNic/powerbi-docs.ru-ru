---
title: "Выделенные пользователи Office 365. Известные проблемы"
description: "Поддержка выделенных пользователей Office 365 — известные проблемы. В этом разделе описаны вопросы, связанные с выделенными пользователями Office 365, включая ограничения для функции работы с группами, а также приложение для iPhone с именными доменами."
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 06/28/2017
ms.author: maghan
ms.openlocfilehash: cd518803eb04f7baceca5d8bc4fdfb1129622016
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2018
---
# <a name="office-365-dedicated-customers---known-issues"></a>Выделенные пользователи Office 365. Известные проблемы
Power BI теперь поддерживается для выделенных пользователей Office 365.  Если вы являетесь выделенным пользователем Office 365, то можете выполнить вход с учетной записью из данного клиента и использовать Power BI. В настоящее время известны две проблемы.

## <a name="groups"></a>Группы
При выборе пункта **Члены** или **Календарь** в контекстном меню группы пользователь будет перенаправлен на приложение работы с электронной почтой.  Пункты **Файлы** и **Беседы** работают должным образом.

![](media/service-admin-office-365-dedicated-known-issues/group-menu.png)

## <a name="iphone-app---sign-in-with-vanity-domain-leads-to-error"></a>Приложение для iPhone — вход с использованием именного домена приводит к ошибке
При выполнении входа в приложение для iPhone использование учетных данных с именным доменом может привести к ошибке.

*Ошибка входа*  
*Произошла непредвиденная внутренняя ошибка. Повторите попытку.*

Чтобы обойти эту проблему, при входе вместо именного домена используйте адрес электронной почты, который отображается при щелчке значка пользователя в службе Power BI.

![](media/service-admin-office-365-dedicated-known-issues/sign-in-address.png)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
