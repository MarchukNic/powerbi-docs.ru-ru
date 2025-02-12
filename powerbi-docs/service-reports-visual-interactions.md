---
title: Изменение способа взаимодействия визуальных элементов в отчете
description: Документация по настройке взаимодействия визуализаций в отчете службы Microsoft Power BI и отчете Power BI Desktop.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: N_xYsCbyHPw
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 02/11/2019
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: 6f739992ed282ada92b1049df09a8b5d4b3938a9
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61405990"
---
# <a name="change-how-visuals-interact-in-a-power-bi-report"></a>Изменение способа взаимодействия визуальных элементов в отчете Power BI
При наличии разрешений на изменение отчета вы можете использовать **взаимодействие визуализаций**, чтобы задавать влияние друг на друга визуализаций на странице отчета. 

По умолчанию визуализации на странице отчета можно использовать для кроссфильтрации и перекрестного выделения других визуализаций на странице.
Например, при выборе состояния в визуализации карты выделяется диаграмма столбца и фильтруется график, чтобы отобразить только данные, применимые к этому состоянию.
См. раздел [Сведения о фильтрации и выделении](power-bi-reports-filters-and-highlighting.md). При наличии визуализации, которая поддерживает [детализацию](consumer/end-user-drill.md), детализация одной визуализации по умолчанию не оказывает влияния на другие визуализации на странице отчета. Но вы можете переопределить оба этих способа работы по умолчанию и задать взаимодействия для каждой визуализации отдельно.

Эта статья описывает, как использовать **взаимодействие визуализаций** в [режиме редактирования](service-interact-with-a-report-in-editing-view.md) службы Power BI и в Power BI Desktop. Если отчет предоставлен вам другим пользователем, вы не сможете изменять настройки взаимодействия визуализаций.

> [!NOTE]
> Термины *кроссфильтрация* и *перекрестное выделение* используются для отделения поведения, описанного здесь, от того, что происходит при использовании области **Фильтры** для фильтрации и выделения визуализаций.  
> 
> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/N_xYsCbyHPw?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. Выберите визуализацию, чтобы сделать ее активной.  
2. Откройте параметры **Взаимодействия визуализаций**.
    - В службе Power BI щелкните раскрывающийся список в строке меню отчета.

       ![Раскрывающийся список взаимодействий визуализаций](media/service-reports-visual-interactions/power-bi-visual-interaction.png)

    - В версии Desktop выберите **Формат > Взаимодействия**.

        ![последовательный выбор пунктов "Формат" и "Взаимодействия"](media/service-reports-visual-interactions/pbi-visual-interaction-desktop.png)

3. Чтобы включить элементы управления взаимодействиями визуализаций, выберите **Изменить взаимодействия**. Power BI добавит значки перекрестной фильтрации и выделения во все остальные визуализации на странице отчета.
   
    ![отчет с включенными взаимодействиями визуализаций](media/service-reports-visual-interactions/power-bi-icons-on.png)
3. Укажите, как выбранная визуализация должна влиять на другие.  При необходимости повторите эти действия для всех остальных визуализаций на странице отчета.
   
   * Если нужно выполнить перекрестную фильтрацию визуализации, выберите значок **фильтра** ![значок фильтра](media/service-reports-visual-interactions/pbi-filter-icon-outlined.png).
   * Если нужно выполнить перекрестное выделение визуализации, выберите значок **выделения** ![значок выделения](media/service-reports-visual-interactions/pbi-highlight-icon-outlined.png).
   * Если влияния не должно быть, выберите значок **отсутствия влияния** ![значок отсутствия влияния](media/service-reports-visual-interactions/pbi-noimpact-icon-outlined.png).

4. Чтобы включить элементы управления детализации, выберите **Детализирующие фильтры для других визуализаций**.  Теперь при детализации (и обобщении) другие визуализации на странице отчета изменяются в зависимости от выбранных вариантов детализации. 

   ![Видео включения элементов управления детализации](media/service-reports-visual-interactions/drill2.gif)

