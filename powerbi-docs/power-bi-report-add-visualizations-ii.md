---
title: "Часть 2. Добавление визуализаций в отчет Power BI (Руководство)"
description: "Учебник. Часть 2. Добавление визуализаций в отчет Power BI"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: 2b3f25c772a049d10bc03941db677c67c844da8b
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2017
---
# <a name="part-2-add-visualizations-to-a-power-bi-report-tutorial"></a>Часть 2. Добавление визуализаций в отчет Power BI (Руководство)
В [части 1](power-bi-report-add-visualizations-ii.md) вы создали базовую визуализацию, установив флажки рядом с именами полей.  Во второй части вы узнаете, как использовать функцию перетаскивания и полностью реализовать возможности панелей **Поля** и **Визуализации** для создания и изменения визуализаций.

## <a name="create-a-new-visualization"></a>Создание новой визуализации
В этом руководстве мы подробно рассмотрим набор данных по анализу розничной торговли и создадим несколько ключевых визуализаций.

### <a name="open-a-report-and-add-a-new-blank-page"></a>Откройте отчет и добавьте в него новую пустую страницу.
1. Откройте рабочую область, где был сохранен пример "Анализ розничной торговли". Выберите **Анализ розничной торговли — пример**, чтобы открыть отчет в режиме чтения.
   
   ![](media/power-bi-report-add-visualizations-ii/power-bi-open-report.png)
2. Выберите пункт **Изменить отчет** , чтобы открыть отчет в режиме редактирования.
   
   ![](media/power-bi-report-add-visualizations-ii/editreport1.png)
3. [Добавьте новую страницу](power-bi-report-add-page.md), выбрав желтый значок "плюс" в нижней части холста.
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_addreportpage.png)

### <a name="add-a-visualization-that-looks-at-this-years-sales-compared-to-last-year"></a>Добавьте визуализацию с отображением показателей объема продаж текущего года по сравнению с продажами в предыдущем году.
1. В таблице **Продажи** последовательно выберите элементы **Продажи этого года** > **Значение** и **Продажи прошлого года**. Power BI создаст гистограмму.  Она представляет интерес и требует более глубокого анализа. Как продажи распределяются по месяцам?  
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_4bnew.png)
2. Из таблицы времени перетащите **Месяц** в область **Оси**.  
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_5newnew.png)
3. [Измените визуализацию](power-bi-report-change-visualization-type.md) на диаграмму с областями.  Для выбора доступно множество типов визуализации. Сведения об использовании нужного типа см. в статьях с [описаниями каждого типа, советами, рекомендациями и учебниками](power-bi-visualization-types-for-reports-and-q-and-a.md). На панели "Визуализации" выберите значок диаграммы с областями.
4. Отсортируйте визуальные элементы, нажав кнопку с многоточием и выбрав пункт **Сортировать по месяцам**.
5. [Измените размер визуализации](power-bi-visualization-move-and-resize.md). Для этого выберите визуализацию, щелкните и перетащите один из кругов. Сделайте ее достаточно широкой, чтобы исключить полосу прокрутки, и достаточно небольшой, чтобы оставить место для добавления другой визуализации.
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_7b.png)
6. [Сохраните отчет](service-report-save.md).

### <a name="add-a-map-visualization-that-looks-at-sales-by-location"></a>Добавьте визуализацию карты для отслеживания продаж по расположению.
1. В таблице **Магазин** выберите **Территория**. Power BI распознает, что территория является расположением, и создает визуализацию карты.  
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_8newnew.png)
2. Перетащите элемент **Всего магазинов** в область "Размер".  
   ![](media/power-bi-report-add-visualizations-ii/power-bi-add-visual-to-a-reportnew.png)
3. Добавьте условные обозначения.  Чтобы просмотреть данные по названию магазина, перетащите элемент **Цепочка** в область условных обозначений.  
   ![](media/power-bi-report-add-visualizations-ii/power-bi-add-visual-to-a-report-3new.png)

## <a name="next-steps"></a>Дальнейшие действия
* Дополнительные сведения о панели "Поля" см. в статье [Обзор редактора отчетов](service-the-report-editor-take-a-tour.md).   
* Дополнительные сведения о фильтрации и выделении визуализаций см. в статье [Фильтры и выделение в отчетах Power BI](power-bi-reports-filters-and-highlighting.md).  
* Дополнительные сведения об использовании и изменении статистических выражений см. в статье [Статистические выражения в отчетах](service-aggregates.md).  
* Подробнее о [визуализациях в отчетах Power BI](power-bi-report-visualizations.md).  
* Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI](http://community.powerbi.com/).
