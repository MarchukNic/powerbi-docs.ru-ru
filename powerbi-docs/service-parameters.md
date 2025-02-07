---
title: Изменение настроек параметров в службе Power BI
description: Параметры запроса создаются в Power BI Desktop, однако их можно просматривать и изменять в службе Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 11/21/2018
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: 8db6f106ecc2285cb66ff980bc72fa666456f81a
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61226033"
---
# <a name="edit-parameter-settings-in-the-power-bi-service"></a>Изменение настроек параметров в службе Power BI
Авторы отчетов добавляют параметры запросов в отчеты в Power BI Desktop. Параметры позволяют создавать части отчетов в зависимости от *значений* одного или нескольких параметров. Например, автор отчета может создать параметр, который ограничивает данные одной страной или регионом, или параметр, который определяет число допустимых форматов для таких полей, как поле даты, времени и текста.

![Вкладка "Главная" с пунктом "Управление параметрами" в Desktop](media/service-parameters/power-bi-manage-parameters.png)

## <a name="review-and-edit-parameters-in-power-bi-service"></a>Просмотр и изменение параметров в службе Power BI

Вы, как автор отчета, определяете параметры в Desktop. Когда вы [публикуете этот отчет в службе Power BI](desktop-upload-desktop-files.md), настройки параметров и выбранные варианты переносятся вместе с ним. Вы можете просмотреть и изменить некоторые настройки параметров в службе Power BI, но не параметры, ограничивающие доступные данные, а параметры, которые определяют и описывают допустимые значения.

1. В службе Power BI щелкните значок шестеренки ![значок шестеренки](media/service-parameters/power-bi-cog.png), чтобы открыть окно **Параметры**.

2. Выберите вкладку **Наборы данных** и выделите набор данных в списке. 
    
    ![Окно "Параметры" с выбранной вкладкой "Наборы данных"](media/service-parameters/power-bi-select-dataset2.png)

3. Разверните узел **Параметры**.  Если выбранный набор данных не содержит параметры, вы увидите сообщение со ссылкой для получения дополнительных сведений о параметрах запроса. Однако если набор данных содержит параметры, развернув заголовок **Параметры**, вы увидите эти параметры. 

    ![Окно "Параметры" с развернутым разделом параметров](media/service-parameters/power-bi-settings.png)

    Просмотрите настройки параметров и при необходимости внесите изменения. Неактивные поля недоступны для редактирования. 


## <a name="next-steps"></a>Дальнейшие действия
Ситуативный способ добавления простых параметров путем [изменения URL-адреса](service-url-filters.md).