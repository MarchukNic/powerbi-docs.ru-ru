---
title: "Параметры отображения и просмотра страницы для отчета"
description: "Параметры отображения и просмотра страницы для отчета"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: 
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/24/2017
ms.author: mihart
ms.openlocfilehash: 57c441c489bf71db4b45bdfb96821b3cc2dcdec3
ms.sourcegitcommit: 804ee18b4c892b7dcbd7d7d5d987b16ef16fc2bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/09/2018
---
# <a name="page-display-settings-in-a-power-bi-report"></a>Параметры отображения страницы в отчете Power BI
Очень важно обеспечить точное и качественное отображение макета отчета. В некоторых случаях это может оказаться сложной задачей, так вы и ваши коллеги просматриваете эти отчеты на экранах разных размеров и с различным соотношением сторон. 

По умолчанию используется представление **Вписать в страницу** , размер экрана по умолчанию — **16:9**. Если требуется заблокировать другие пропорции или по-другому расположить отчет, можно воспользоваться двумя средствами: параметрами ***режима страницы*** и параметрами ***размера страницы***.

<iframe width="560" height="315" src="https://www.youtube.com/embed/5tg-OXzxe2g" frameborder="0" allowfullscreen></iframe>


## <a name="where-to-find-page-view-settings-in-power-bi-service-and-power-bi-desktop"></a>Где найти параметры просмотра страницы в службе Power BI и Power BI Desktop
Параметры просмотра страницы доступны как в службе Power BI, так и в Power BI Desktop. Но интерфейс немного отличается. В следующих двух разделах объясняется, где найти параметры просмотра в каждом средстве Power BI.

### <a name="in-power-bi-desktop"></a>Power BI Desktop
В представлении отчетов выберите вкладку **Просмотр**, чтобы открыть параметры просмотра страницы и параметры макета для телефона.

  ![область выделения](media/power-bi-report-display-settings/power-bi-desktop-view-settings.png)

### <a name="in-power-bi-service-apppowerbicom"></a>Служба Power BI (app.powerbi.com)
В службе Power BI откройте отчет и выберите **Просмотр** в строке меню в левой верхней части окна.

![](media/power-bi-report-display-settings/power-bi-change-page-view.png)

Параметры просмотра страницы доступны в [режиме чтения и режиме правки](service-reading-view-and-editing-view.md). В режиме правки владелец отчета может назначить параметр просмотра для отдельных страниц отчета. Эти параметры сохраняются вместе с отчетом. Когда коллеги открывают отчет в режиме чтения, страницы отчета отображаются с примененными параметрами владельца.  В режиме чтения коллеги могут изменить *некоторые* параметры просмотра страницы, но при закрытии отчета изменения не сохраняются.

##    <a name="page-view-settings"></a>Параметры просмотра страницы
Первый набор параметров для *просмотра страницы* позволяет управлять отображением страницы отчета относительно окна браузера.  Доступны следующие параметры:

* **По размеру страницы** (по умолчанию): масштаб содержимого подбирается к размеру страницы.
* **По ширине**: масштаб содержимого подбирается к ширине страницы.
* **Фактический размер**: содержимое отображается в полном размере.

Второй набор параметров для *просмотра страницы* позволяет управлять расположением объектов на холсте отчета:

* **Показать линии сетки.** Линии сетки помогут разместить объекты на холсте отчета.
* **Привязать к сетке.** Используйте этот параметр с **отображением линий сетки**, чтобы точно расположить и выровнять объекты на холсте отчета. 
* **Блокировка объектов.** Блокируются все объекты на холсте, чтобы нельзя было изменить их расположение и размер.
* **Область выделения.** В области выделения отображается список всех объектов на холсте. Вы можете решить, какие из них показать, а какие скрыть.

    ![область выделения](media/power-bi-report-display-settings/power-bi-selection-pane.png)



## <a name="page-size-settings"></a>Параметры размера страницы
![](media/power-bi-report-display-settings/power-bi--page-size.png)

Параметры *размера страницы* доступны только для владельцев отчетов. В службе Power BI (app.powerbi.com) это означает возможность открыть отчет в [режиме правки](service-reading-view-and-editing-view.md). Эти параметры используются для управления соотношением отображения и фактическим размером (в пикселях) холста отчета.   

* Соотношение 4:3
* Соотношение 16:9 (по умолчанию)
* Кортана
* Письмо
* Выборочно (высота и ширина в пикселях)

## <a name="next-steps"></a>Дальнейшие действия
[Узнайте, как использовать параметры просмотра и размера страницы в своих отчетах Power BI](power-bi-change-report-display-settings.md).

Дополнительные сведения об [отчетах в Power BI](service-reports.md)

[Power BI — основные понятия](service-basic-concepts.md)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
