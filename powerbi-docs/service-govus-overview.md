---
title: "Общие сведения о Power BI для клиентов из государственных организаций США"
description: "Ознакомьтесь с возможностями и ограничениями службы Power BI для государственных организаций США"
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 9c8e2b44c128db283bef65198204e4aee1bfdd7a
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="power-bi-for-us-government-customers"></a>Power BI для клиентов из государственных организаций США
Существует версия **службы Power BI** для клиентов из государственных организаций США, доступная в рамках подписок **Office 365 для сообщества государственных организаций США**. Версия **службы Power BI**, описанная в этой статье, специально предназначена для клиентов из государственных организаций США и отличается от коммерческой версии **службы Power BI**.

![](media/service-govus-overview/service_usgov_overview-1.png)

В следующих разделах описываются *возможности* и *ограничения* версии **службы Power BI** для государственных организаций США, приводятся **часто задаваемые вопросы** и ответы на них (включая инструкции по регистрации), а также ссылки на дополнительные сведения.

## <a name="features-of-power-bi-us-government"></a>Возможности Power BI для государственных организаций США
Важно помнить, что версия **Power BI для государственных организаций США** доступна только в рамках **лицензии Pro**. При использовании бесплатной лицензии эта версия недоступна. В **Power BI для государственных организаций США** доступны только определенные функции службы Power BI.

Ниже приведены функции службы **Power BI для государственных организаций США**, доступные в рамках лицензии **Pro**.

* создание и просмотр панелей мониторинга и отчетов;
* [ограничение емкости данных;](service-admin-manage-your-data-storage-in-power-bi.md)
* [обновление данных по расписанию;](refresh-data.md)
* обновляемые информационные панели группы;
* группы Active Directory для совместного использования и управления доступом;
* [импорт данных](service-get-data.md) и отчетов из файлов Excel, CSV и Power BI Desktop;
* Шлюз управления данными
* шифрование всех данных в Azure SQL и хранилище BLOB-объектов для Power BI;
* подключение к службам с помощью [пакетов содержимого](service-connect-to-services.md).

## <a name="limitations-of-power-bi-us-government"></a>Ограничения Power BI для государственных организаций США
Некоторые функции, доступные в коммерческой версии **службы Power BI**, *отсутствуют* в версии **службы Power BI** для государственных организаций США. Команда разработчиков Power BI прилагает все усилия, чтобы сделать эти функции доступными для клиентов из государственных организаций США. Когда они станут доступными, эта статья будет обновлена.

* Служба **Power BI для государственных организаций США** доступна только в рамках лицензии **Pro**. Все ссылки на лицензии Power BI (бесплатные) на портале администрирования (или как пользователи) выполняются в коммерческой облачной службе Power BI.
* **Аудит.** Аудит недоступен в Центре безопасности и соответствия требованиям на портале Office 365.

Если учетной записи назначены бесплатные лицензии на службу **Power BI**, эти учетные записи выполняются в коммерческой версии **Power BI** и не входят в состав предложения **Power BI для государственных организаций США**. С бесплатными учетными записями могут возникнуть следующие проблемы:

* Не удается выполнить аутентификацию шлюза, мобильных устройств и рабочего стола.
* Не удается получить доступ к коммерческим источникам данных Azure.
* PBIX-файлы должны передаваться из коммерческих источников данных вручную.
* Мобильные приложения Power BI недоступны.

Для решения этих проблем, обратитесь к представителю учетной записи.

## <a name="frequently-asked-questions-faq-for-the-us-government-version-of-the-power-bi-service"></a>Часто задаваемые вопросы о версии службы Power BI для государственных организаций США
Следующий список вопросов и ответов поможет вам быстро найти необходимые сведения об этой службе.

**Вопрос.** Как перенести данные из коммерческой версии **Power BI** в **службу Power BI** для государственных организаций США?

**Ответ.** Ваш администратор должен создать новый экземпляр **Power BI** в рамках отдельной подписки для государственной организации США. После этого вы сможете реплицировать свои данные из коммерческой версии в **службу Power BI** для государственных организаций США, удалить коммерческую лицензию и связать существующий домен с новой службой для государственных организаций США.

**Вопрос.** Почему не удается подключиться к определенному пакету содержимого?

**Ответ.** Прежде чем подключаться к этому пакету содержимого, убедитесь, что ваша подписка включена.

**Вопрос.** Я хочу использовать **Power BI** в своей государственной организации в США. С чего начать?

**Ответ.** Процесс регистрации (иногда называемый *подключением*) может отличаться в зависимости от имеющейся лицензии и подписки. Дополнительные сведения см. в статье о [регистрации государственных организаций США в службе Power BI](service-govus-signup.md).

**Вопрос.** Отличается ли URL-адрес для подключения к службе **Power BI** для государственных организаций США от URL-адреса для подключения к коммерческой службе **Power BI**?

**Ответ.** Да, эти URL-адреса отличаются. Оба они приведены в следующей таблице.

| URL-адрес коммерческой версии | URL-адрес версии для государственных организаций США |
| --- | --- |
| https://app.powerbi.com/ |[https://app.powerbigov.us](https://app.powerbigov.us) |

## <a name="next-steps"></a>Дальнейшие действия
Служба Power BI предоставляет широкие возможности. Дополнительные сведения и руководства, включая статью с инструкциями по регистрации в службе, см. по следующим ссылкам:

* [Регистрация в службе Power BI для государственных организаций США](service-govus-signup.md)
* <a href="https://channel9.msdn.com/Blogs/Azure/Cognitive-Services-HDInsight-and-Power-BI-on-Azure-Government">Power BI US Government Demo</a> (Power BI для государственных организаций США (демо-версия))
* [Интерактивное обучение работе с Power BI](guided-learning/gettingstarted.yml#step-1)
* [Приступая к работе со службой Power BI](service-get-started.md)
* [Начало работы с Power BI Desktop](desktop-getting-started.md)
