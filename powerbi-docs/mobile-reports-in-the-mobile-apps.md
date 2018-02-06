---
title: "Просмотр отчетов в мобильных приложениях Power BI"
description: "Узнайте, как просматривать отчеты и работать с ними в мобильных приложениях Power BI на телефоне или планшетном ПК. Вы можете создавать отчеты в службе Power BI или в приложении Power BI Desktop, а затем работать с ними в мобильных приложениях. "
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 01/25/2018
ms.author: maggies
ms.openlocfilehash: 51006f70d0be13f08de7047f0097f7530d32a470
ms.sourcegitcommit: be5223b62e9a5d57c52f8588d4e539d814751dd6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2018
---
# <a name="explore-reports-in-the-power-bi-mobile-apps"></a>Просмотр отчетов в мобильных приложениях Power BI
Область применения:

| ![iPhone](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![iPad](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![Телефон Android](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Планшет Android](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Устройства под управлением Windows 10](media/mobile-reports-in-the-mobile-apps/win-10-logo-40-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhone |iPad |Телефоны под управлением Android |Планшеты Android |Устройства под управлением Windows 10 |

Отчет Power BI — это интерактивное представление данных с визуальными элементами, которые отображают различные результаты и сведения, полученные из этих данных. Просмотр отчетов в мобильных приложениях Power BI — это последний шаг трехэтапной процедуры.

1. [Создание отчетов в Power BI Desktop](desktop-report-view.md). В Power BI Desktop можно даже [оптимизировать отчет для телефонов](mobile-apps-view-phone-report.md). 
2. Публиковать эти отчеты можно в службе Power BI [(https://powerbi.com)](https://powerbi.com) или на сервере [Power BI Report Server](report-server/get-started.md).  
3. После этого вы можете работать с отчетами в мобильных приложениях Power BI.

## <a name="open-a-power-bi-report-in-the-mobile-app"></a>Открытие отчета Power BI в мобильном приложении
Расположение отчетов Power BI в мобильном приложении зависит от места их получения. Они могут быть в расположении "Приложения", "Мне предоставлен доступ", "Рабочие области" (включая страницу "Моя рабочая область") или на сервере отчетов. Иногда получить отчет можно при помощи связанной панели мониторинга, а иногда они представлены в списке.

* На панели мониторинга коснитесь многоточия (...) в правом верхнем углу плитки и выберите команду **Открыть отчет**.
  
  ![Открытие отчета](media/mobile-reports-in-the-mobile-apps/power-bi-android-open-report-tile.png)
  
  Не на всех плитках можно открыть отчет. Например, плитки, созданные после ввода данных в поле вопросов и ответов, не открывают отчеты при касании. 
  
  На телефоне отчет открывается в альбомной ориентации, если он не [оптимизирован для просмотра на телефоне](mobile-reports-in-the-mobile-apps.md#view-reports-optimized-for-phones).
  
  ![Мобильный отчет в альбомном режиме](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-landscape.png)

## <a name="view-reports-optimized-for-phones"></a>Просмотр отчетов, оптимизированных для телефона
Можно создать макет отчета Power BI, оптимизированный для телефонов. Для страниц отчетов, оптимизированных для телефонов, добавлены новые возможности. Например, можно детализировать и сортировать визуальные элементы в режиме фокусировки и получать доступ к [фильтрам, который добавил на страницу отчета автор отчета](mobile-apps-view-phone-report.md#filter-the-report-page-on-a-phone). В списке оптимизированный отчет отмечен специальным значком ![Значок отчета для телефона](media/mobile-reports-in-the-mobile-apps/power-bi-phone-report-icon.png):

![Открытие мобильного отчета](media/mobile-reports-in-the-mobile-apps/power-bi-android-phone-report.png)

На телефоне такой отчет открывается в книжной ориентации.

![Отчет в книжной ориентации](media/mobile-reports-in-the-mobile-apps/07-power-bi-phone-report-portrait.png)

 Отчет может содержать ряд страниц, не оптимизированных для телефонов. В таком случае представление для каждой страницы будет переключаться с книжной в альбомную ориентацию.

Узнайте больше об [отчетах, оптимизированных для представления телефона](mobile-apps-view-phone-report.md).

## <a name="use-slicers-to-filter-a-report-page"></a>Использование срезов для фильтрации данных на странице отчета
При создании отчетов в приложении Power BI Desktop или службе Power BI попробуйте [добавить на страницу отчета срезы](power-bi-visualization-slicers.md). Вы и ваши коллеги можете использовать их для фильтрации данных страницы в браузере и в мобильных приложениях. При просмотре отчета на телефоне вы можете видеть срезы и взаимодействовать с ними в альбомной ориентации, а также на странице, оптимизированной для книжной ориентации телефона.

* Когда вы выбираете значение в срезе на странице отчета, фильтруются и другие визуальные элементы.
  
  ![Срез отчетов](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-slicer.png)
  
  На изображении ниже срез фильтрует гистограмму для отображения значений только за июль.

## <a name="cross-filter-and-highlight-a-power-bi-report-page"></a>Перекрестная фильтрация и выделение страницы отчета Power BI
При выборе значения в визуальном элементе другие визуальные элементы не фильтруются. Связанные значения в других визуальных элементах выделяются.

* Коснитесь значения в визуальном элементе.
  
  ![Перекрестная фильтрация страницы](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-highlight.png)
  
  При касании столбца "Large" в одном визуальном элементе выделяются связанные значения в других визуальных элементах. 

## <a name="sort-a-visual-on-an-ipad-or-a-tablet"></a>Сортировка визуальных элементов на iPad или планшетном ПК
* Коснитесь диаграммы, многоточия (**…**), а затем коснитесь имени поля.
  
   ![Сортировка визуального элемента](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-sort.png)
* Чтобы изменить порядок сортировки, снова коснитесь многоточия (**...**), а затем еще раз коснитесь того же имени поля.

## <a name="drill-down-and-up-in-a-visual-on-an-ipad-or-a-tablet"></a>Детализация и ее отмена в визуальном элементе на iPad или планшетном ПК
Эта возможность позволяет детализировать визуальный элемент на iPad или планшетном ПК, чтобы просматривать значения, составляющие его определенную часть. Детализацию можно [добавить в визуальный элемент](power-bi-visualization-drill-down.md) в службе Power BI Desktop или Power BI. 

> [!NOTE]
> Сейчас функция детализации карт на устройствах iPad и планшетных ПК не работает.
> 
> 

* Коснитесь визуального элемента. Если в верхних углах есть стрелки вверх и вниз, ![Значки детализации](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up-down.png)вы можете выполнить детализацию. Для увеличения детализации на одно значение коснитесь стрелки в правом верхнем углу и коснитесь значения в визуальном элементе &#151. В данном случае это темно-синий пузырек FD-04.
  
  ![Детализация в визуальном элементе](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-down-one.png)
* Чтобы детализировать резервное копирование, коснитесь стрелки вверх в левом верхнем углу экрана.
  
  ![Уменьшение детализации](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up.png)

## <a name="go-back-to-my-workspace"></a>Возврат на страницу "Моя рабочая область"
* Коснитесь стрелки рядом с именем отчета и выберите **Моя рабочая область**.
  
  ![Возврат](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-back.png)

## <a name="next-steps"></a>Дальнейшие действия
* [Просмотр отчетов Power BI, оптимизированных для телефона, и взаимодействие с ними](mobile-apps-view-phone-report.md)
* [Создание отчетов, оптимизированных для мобильных приложений Power BI](desktop-create-phone-report.md)
* У вас появились вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)
