---
title: Общие сведения о взаимодействии визуальных элементов в отчете
description: Документация для пользователей Power BI с описанием механизма взаимодействия визуальных элементов на странице отчета.
author: mihart
manager: kvivek
ms.custom: seodec18
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 05/29/2019
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: 7148a52d7c7475fbe685f83b1e1cc325521460db
ms.sourcegitcommit: d88cc6a87d4ba82ad2c4d496a3634f927e4ac529
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/30/2019
ms.locfileid: "66413171"
---
# <a name="how-visuals-cross-filter-each-other-in-a-power-bi-report"></a>Перекрестная фильтрация визуальных элементов в отчете Power BI
Одно из главных преимуществ Power BI заключается во взаимосвязи всех визуальных элементов на странице отчета. Когда вы выбираете точку данных на любом из визуальных элементов, с учетом этого изменяется содержимое всех остальных визуальных элементов на странице. 

![Видео о взаимодействии визуальных элементов](media/end-user-interactions/interactions.gif)

По умолчанию, выбрав точку данных в одной визуализации на странице отчета будет кросс фильтр, перекрестное выделение и других визуализаций на странице детализации. 

Это может быть полезно для идентификации как одно значение данных участвует в другой. Например выбрав "сегмент" модерации в кольцевой диаграмме представлены вклад из сегмента для каждого столбца в общее количество единиц по диаграмме месяца, и он отфильтровал график справа.

![Снимок экрана: взаимодействия визуальных элементов](media/end-user-interactions/power-bi-interactions.png)

См. раздел [Сведения о фильтрации и выделении](../power-bi-reports-filters-and-highlighting.md). 

Конкретные правила взаимодействия визуальных элементов на странице определяются *конструктором* отчета. Конструкторы могут включать и выключать средства взаимодействия, а также изменять настроенные по умолчанию поведения перекрестной фильтрации, перекрестного выделения и детализации. 
  
> [!NOTE]
> Термины *кроссфильтрация* и *перекрестное выделение* используются для отделения поведения, описанного здесь, от того, что происходит при использовании области **Фильтры** для фильтрации и выделения визуализаций.  

## <a name="considerations-and-troubleshooting"></a>Рекомендации и устранение неполадок
- Если отчет содержит визуализацию, которая поддерживает [детализации](../power-bi-visualization-drill-down.md), по умолчанию детализация одной визуализации не влияет на другие визуализации на странице отчета.     
- Если вы используете visualA для взаимодействия с visualB, фильтрах уровня визуальных элементов из visualA применяются к visualB.

## <a name="next-steps"></a>Дальнейшие действия
[Использование фильтров отчетов](../power-bi-how-to-report-filter.md)
