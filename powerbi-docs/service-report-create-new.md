---
title: "Руководство. Создание отчета из набора данных "
description: "Создание отчета Power BI из набора данных."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: mihart
ms.openlocfilehash: 7405f2c5663c071d58253f2103c9c7d778ea8299
ms.sourcegitcommit: be5223b62e9a5d57c52f8588d4e539d814751dd6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2018
---
# <a name="create-a-new-power-bi-report-by-importing-a-dataset"></a>Создание отчета Power BI путем импорта набора данных
Вы ознакомились со статьей [Отчеты в Power BI](service-reports.md) и хотите создать свои собственные отчеты. Существует много различных способов создания отчета. В этом разделе мы создадим очень простой из набора данных Excel. Поняв принцип создания отчета, вы можете ознакомиться с более подробными темами в разделе **Дальнейшие действия** ниже.  

> **Совет.** Сведения о создании отчета из имеющегося отчета см. [здесь](power-bi-report-copy.md).
> 
### <a name="prerequisites"></a>Предварительные требования
- Служба Power BI (для создания отчетов с помощью Power BI Desktop). См. статью [Представление отчетов в Power BI Desktop](desktop-report-view.md)   
- Набор данных "Анализ розничной торговли — пример"

## <a name="import-the-dataset"></a>Импорт набора данных
Чтобы создать отчет таким способом, сначала вам потребуется набор данных и пустой холст отчета. Для дальнейшей работы [скачайте набор данных Excel "Анализ розничной торговли — пример"](http://go.microsoft.com/fwlink/?LinkId=529778) и сохраните его в OneDrive для бизнеса (предпочтительный вариант) или в локальной среде.

1. Мы создадим отчет в рабочей области службы Power BI, поэтому создайте рабочую область или выберите существующую.
   
   ![](media/service-report-create-new/power-bi-workspaces2.png)
2. В нижней части панели навигации слева выберите **Получить данные**.
   
   ![](media/service-report-create-new/power-bi-get-data3.png)
3. Выберите **Файлы** и перейдите к расположению, в котором вы сохранили пример анализа розничной торговли.
   
    ![](media/service-report-create-new/power-bi-select-files.png)
4. Для этого упражнения выберите **Импорт**.
   
   ![](media/service-report-create-new/power-bi-import.png)
5. После импорта набора данных выберите **Просмотреть набор данных**.
   
   ![](media/service-report-create-new/power-bi-view-dataset.png)
6. При просмотре набора фактически запускается редактор отчетов.  На экране появляется пустой холст и инструменты для редактирования отчета.
   
   ![](media/service-report-create-new/power-bi-blank-report.png)

> **Совет.** Если вы еще не работали с холстом редактирования отчета или хотите вспомнить ранее изученные сведения, перед продолжением прочтите статью [Знакомство с редактором отчетов](service-the-report-editor-take-a-tour.md).
> 
> 

## <a name="add-a-radial-gauge-to-the-report"></a>Добавление диаграммы "Радиальный датчик" в отчет
После импорта набора данных сначала ответим на некоторые вопросы.  Руководитель отдела маркетинга хочет знать, насколько мы близки к запланированному показателю продаж в этом году. Визуальный элемент "Датчик" [хорошо подходит](power-bi-report-visualizations.md) для отображения такого типа информации.

1. В области "Поля" выберите **По продажам** > **This Year Sales** (Продажи за этот год) > **Значение**.
   
    ![](media/service-report-create-new/power-bi-report-step1.png)
2. Преобразуйте визуальный элемент в датчик, выбрав соответствующий шаблон ![](media/service-report-create-new/powerbi-gauge-icon.png) в области **Визуализации**.
   
    ![](media/service-report-create-new/power-bi-report-step2.png)
3. Перетащите поле **Sales** (Продажи) > **This Year Sales** (Продажи за этот год) > **Goal** (Цель) в столбец **Целевое значение**. Похоже, мы очень близки к цели.
   
    ![](media/service-report-create-new/power-bi-report-step3.png)
4. Теперь [сохраните отчет](service-report-save.md).
   
   ![](media/service-report-create-new/powerbi-save.png)

## <a name="add-an-area-chart-and-slicer-to-the-report"></a>Добавление диаграммы с областями и среза в отчет
Руководитель отдела маркетинга имеет дополнительные вопросы. Он хотел узнать об уровне продаж в этом году по сравнению с предыдущим, а также хотел бы увидеть результаты по региону.

1. Во-первых, создадим дополнительное пространство на холсте. Выберите визуальный элемент "Датчик" и переместите его в правый верхний угол. Затем перетащите один из углов, чтобы уменьшить размер холста.
2. Отмените выбор визуального элемента "Датчик". В области "Поля" выберите **По продажам** > **This Year Sales** (Продажи за этот год) > **Значение** и выберите **По продажам** > **Last Year Sales** (Продажи за прошлый год).
   
    ![](media/service-report-create-new/power-bi-report-step4.png)
3. Преобразуйте визуальный элемент в диаграмму с областями, выбрав соответствующий шаблон ![](media/service-report-create-new/power-bi-areachart-icon.png) в области **Визуализации**.
4. Выберите **Время** > **Период**, чтобы добавить время в качестве **оси**.
   
    ![](media/service-report-create-new/power-bi-report-step5.png)
5. Чтобы отсортировать визуальные элементы по времени, нажмите кнопку с многоточием и выберите **Sort by Period** (Сортировать по периоду).
6. Теперь добавим срез. Щелкните пустую область на холсте и выберите шаблон "Срез" ![](media/service-report-create-new/power-bi-slicer-icon.png). После этого на холсте появится пустой срез.
   
    ![](media/service-report-create-new/power-bi-report-step6.png)    
7. В области "Поля" выберите **District** (Округ) > **District** (Округ). Переместите срез и измените его размер.
   
    ![](media/service-report-create-new/power-bi-report-step7.png)  
8. Срез позволяет находить шаблоны и аналитические сведения по округу.
   
   ![](media/service-report-create-new/power-bi-slicer-video2.gif)  

Продолжайте анализировать данные и добавлять визуализации. Если вы найдете особенно интересную информацию, [закрепите ее на панели мониторинга](service-dashboard-pin-tile-from-report.md).

## <a name="next-steps"></a>Дальнейшие действия
* [Добавление страницы в отчет Power BI](power-bi-report-add-page.md)  
* [Закрепление плитки на панели мониторинга Power BI из отчета](service-dashboard-pin-tile-from-report.md)   
* Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
