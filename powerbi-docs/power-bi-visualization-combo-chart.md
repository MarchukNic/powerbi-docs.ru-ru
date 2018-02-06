---
title: "Руководство по комбинированной диаграмме"
description: "Это руководство по комбинированным диаграммам описывает, как их применять и создавать в службе Power BI и версии Desktop."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: lnv66cTZ5ho
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/21/2018
ms.author: mihart
ms.openlocfilehash: 9ab6514e2ce5ba81b17f6862eae6c6c76fd9bf7b
ms.sourcegitcommit: c3be4de522874fd73fe6854333b379b85619b907
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2018
---
# <a name="combo-chart-in-power--tutorial"></a>Комбинированная диаграмма в Power (руководство)
В Power BI комбинированная диаграмма представляет собой визуализацию, сочетающую график и гистограмму. Объединение двух диаграмм в одну позволяет быстрее сравнивать данные.

Комбинированная диаграмма может содержать одну или две оси Y.

## <a name="when-to-use-a-combo-chart"></a>Сферы применения комбинированной диаграммы
Комбинированная диаграмма отлично подходит:

* при наличии графика и гистограммы с одной и той же осью X;
* для сравнения нескольких показателей с другими диапазонами значений;
* для демонстрации корреляции между двумя показателями в одной визуализации;
* для проверки соответствия одного показателя целевому, который определяется другим показателем;
* чтобы освободить место на холсте.

### <a name="prerequisites"></a>Предварительные требования
Комбинированные диаграммы доступны как в службе Power BI, так и в Power BI Desktop. В этом руководстве мы создадим комбинированную диаграмму с помощью службы Power BI. Чтобы перейти к выполнению руководства, откройте службу Power BI и подключитесь к примеру "Анализ розничной торговли" согласно [приведенным ниже инструкциям](#create).


## <a name="create-a-basic-single-axis-combo-chart"></a>Создание простой комбинированной диаграммы с одной осью
Посмотрите, как Уилл создает комбинированную диаграмму на основе примера "Продажи и маркетинг".

<iframe width="560" height="315" src="https://www.youtube.com/embed/lnv66cTZ5ho?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

<a name="create"></a> Чтобы создать собственную комбинированную диаграмму, войдите в Power BI и выберите **Получение данных \> Примеры \>Анализ розничной торговли — пример > Подключиться > Перейти к панели мониторинга**.

1. На панели мониторинга "Анализ розничной торговли — пример" выберите **Total Stores** (Всего магазинов), чтобы открыть отчет "Анализ розничной торговли — пример".
2. Выберите пункт **Изменить отчет** , чтобы открыть отчет в режиме редактирования.
3. [Добавьте новую страницу отчета](power-bi-report-add-page.md).
4. Создайте гистограмму, отображающую продажи за этот год и валовую прибыль по месяцам.

    а.  В области "Поля" выберите **Sales** \> **This Year Sales** > **Value** (Продажи > Продажи за этот год > Значение).

    б.  Перетащите **Sales** \> **Gross Margin This Year** (Продажи > Валовая прибыль за этот год) в область **Value** (Значение).

    в.  Выберите **Time** \> **FiscalMonth** (Время > Отчетный месяц), чтобы добавить время в качестве **оси**.

    ![](media/power-bi-visualization-combo-chart/combotutorial1new.png)
5. Щелкните многоточие (...) в правом верхнем углу визуализации и выберите **Sort by FiscalMonth** (Сортировать по отчетному месяцу). Чтобы изменить порядок сортировки (по возрастанию или по убыванию), выберите это же действие повторно.

6. Преобразуйте гистограмму в комбинированную диаграмму. Выделив гистограмму, откройте область **Визуализации** и выберите **Линейная гистограмма и гистограмма с группировкой**.

    ![](media/power-bi-visualization-combo-chart/converttocombo_new2.png)
7. В области **Поля** перетащите **Sales** \> **Last Year Sales** (Продажи > Продажи за прошлый год) в контейнер **Значения строк**.

   ![](media/power-bi-visualization-combo-chart/linevaluebucket.png)

   Ваша комбинированная диаграмма должна выглядеть следующим образом:

   ![](media/power-bi-visualization-combo-chart/combochartdone-new.png)

## <a name="create-a-combo-chart-with-two-axes"></a>Создание комбинированной диаграммы с двумя осями
В этом задании мы сравним валовую прибыль и продажи.

1. Создайте новый график для отслеживания **процента валовой прибыли за прошлый год** по **месяцам**.  В январе процент валовой прибыли составил 35 %, в апреле вырос до 45 %, в июле упал, а в августе снова подскочил. Похожа ли эта картина на данные за предыдущий год?

   ![](media/power-bi-visualization-combo-chart/combo1_new.png)
2. Добавьте к графику показатели **This Year Sales (Выручка за этот год) > Значение** и **Last Year Sales** (Выручка за прошлый год). Масштаб показателя **Gross Margin Last Year %** (Процент валовой прибыли за прошлый год) намного меньше, чем масштаб показателя **Sales** (Продажи), что усложняет сравнение.      

   ![](media/power-bi-visualization-combo-chart/flatline_new.png)
3. Чтобы упростить чтение и понимание визуального элемента, преобразуйте график в линейную гистограмму и гистограмму с накоплением.

   ![](media/power-bi-visualization-combo-chart/converttocombo_new.png)
4. Перетащите параметр **Gross Margin Last Year %** (% валовой прибыли за прошлый год) из области **Значения столбцов** в область **Значения строк**. Power BI создаст две оси, позволяя масштабировать наборы данных независимо друг от друга. Левая ось служит обозначает объемы продаж в долларах, а правая — проценты.

   ![](media/power-bi-visualization-combo-chart/power-bi-combochart.png)    

## <a name="add-titles-to-the-axes"></a>Добавление заголовков осей
1. Откройте панель форматирования, щелкнув значок валика ![](media/power-bi-visualization-combo-chart/power-bi-paintroller.png).
2. Щелкните стрелку вниз, чтобы развернуть параметры **оси Y** .
3. В разделе **Ось Y (столбец)** задайте для параметра **Расположение** значение **Слева**, для переключателя **Заголовок** — положение **Вкл.**, для параметра **Стиль** — значение **Показать только заголовок**, а для параметра **Отображение** — значение **Миллионы**.

   ![](media/power-bi-visualization-combo-chart/power-bi-y-axis-column.png)
4. В разделе **Ось Y (столбец)** прокрутите страницу вниз и убедитесь, что переключатель **Показать вторичные** установлен в положение **Вкл**. Здесь показаны параметры форматирования графика на комбинированной диаграмме.

   ![](media/power-bi-visualization-combo-chart/power-bi-show-secondary.png)
5. Для раздела **Ось Y (строка)** оставьте для параметра **Расположение** значение **Справа**, установите переключатель **Заголовок** в расположение **Вкл.** и задайте для параметра **Стиль** значение **Показать только заголовок**.

   На комбинированной диаграмме теперь отображаются две оси с заголовками.

   ![](media/power-bi-visualization-combo-chart/power-bi-titles-on.png)

6. При желании вы можете изменить шрифт, размер и цвет, а также настроить другие параметры форматирования, чтобы сделать диаграмму более красивой и удобной.

Здесь можно выполнять следующие действия:

* [Добавьте комбинированную диаграмму как плитку панели мониторинга](service-dashboard-tiles.md).
* [Сохраните отчет](service-report-save.md).

## <a name="cross-highlighting-and-cross-filtering"></a>Перекрестное выделение и перекрестная фильтрация

Когда вы выделяете столбец или строку в комбинированной диаграмме, срабатывает перекрестное выделение и перекрестная фильтрация этих данных в других визуализациях на странице отчета (и наоборот). Чтобы изменить это стандартное поведение, используйте элемент управления [Взаимодействие визуальных элементов](service-reports-visual-interactions.md).

## <a name="next-steps"></a>Дальнейшие действия

Сводная информация о [визуализациях в отчетах Power BI](power-bi-report-visualizations.md).

[Типы визуализаций в Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Power BI — основные понятия](service-basic-concepts.md)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)