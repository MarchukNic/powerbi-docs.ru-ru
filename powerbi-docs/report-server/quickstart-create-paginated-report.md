---
title: Создание отчета с разбивкой на страницы BI для Сервера отчетов Power BI
description: Узнайте, как создать отчет c разбивкой на страницы Power BI для сервера отчетов Power BI за несколько простых шагов.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 10/22/2018
ms.author: maggies
ms.openlocfilehash: 9e3a45e7648fd38413c2d45582981bac5e91cd2a
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "64770513"
---
# <a name="create-a-paginated-report-for-power-bi-report-server"></a>Создание отчета с разбивкой на страницы BI для Сервера отчетов Power BI
Как и предполагает название, отчеты c разбивкой на страницы могут выполняться на большом количестве страниц. Они поддерживают точную настройку и создаются в фиксированном формате. Отчеты с разбивкой на страницы это RDL-файлы.

Отчеты c разбивкой на страницы можно хранить на веб-портале сервера отчетов Power BI веб-портале и там же управлять ими, так же как и на веб-портале служб SQL Server Reporting Services (SSRS). Вы можете создавать и редактировать отчеты в построителе или конструкторе отчетов в SQL Server Data Tools (SSDT), а затем публиковать их на любом веб-портале. Затем сообщите читателям в вашей организации, что отчеты можно просматривать в браузере или в мобильном приложении Power BI на мобильных устройствах.

![Отчет с разбивкой на страницы на сервере отчетов Power BI](media/quickstart-create-paginated-report/reportserver-paginated-report.png)

Если вы уже создавали отчеты с разбивкой на страницы в построителе или конструкторе отчетов, вы можете создавать такие же отчеты для сервера отчетов Power BI. Если вы еще не создавали такие отчеты, ниже описаны действия, с помощью которых можно быстро приступить к работе.

## <a name="step-1-install-and-start-report-builder"></a>Шаг 1. Установка и запуск построителя отчетов
Возможно, вы уже установили построитель отчетов для создания отчетов для сервера SSRS. Вы можете использовать ту же версию или построитель отчетов, чтобы создавать отчеты для сервера отчетов Power BI. Если построитель отчетов еще не установлен, это легко исправить.

1. На веб-портале сервера отчетов Power BI выберите **Создать** > **Отчет с разбивкой на страницы**.
   
    ![Меню создания отчета с разбивкой на страницы](media/quickstart-create-paginated-report/reportserver-new-paginated-report-menu.png)
   
    Если построитель отчетов еще не установлен, эти действия сразу приведут вас к установке.
2. После установки в построителе отчетов откроется экран **создания отчета или набора данных**.
   
    ![Экран создания отчета или набора данных](media/quickstart-create-paginated-report/reportserver-paginated-new-report-screen.png)
3. Выберите мастер для типа отчета, который требуется создать:
   
   * таблица или матрица;
   * диаграмма;
   * карта;
   * пустой отчет.
4. Начнем с мастера диаграмм.
   
    Мастер диаграмм поможет вам создать простую диаграмму в отчете. После этого вы сможете настраивать отчет практически до бесконечности.

## <a name="step-2-go-through-the-chart-wizard"></a>Шаг 2. Использование мастера диаграмм
С помощью мастера диаграмм вы пройдете основные этапы создания визуализации в отчете.

Отчеты с разбивкой на страницы можно подключать к разным источникам данных: от Microsoft SQL Server и базы данных Microsoft Azure SQL до Oracle, Hyperion и многих других. Прочитайте статью об [источниках данных, которые поддерживаются отчетами с разбивкой на страницы](connect-data-sources.md).

На первой странице в мастере диаграмм (**Выбор набора данных**) можно создать набор данных или выбрать общий набор данных на сервере. *Наборы данных* возвращают данные отчета из запроса к внешнему источнику данных.

1. Щелкните **Обзор**, а затем выберите общий набор данных на сервере и щелкните **Открыть** > **Далее**.
   
    ![Мастер диаграмм: Выбор набора данных](media/quickstart-create-paginated-report/reportserver-paginated-choose-dataset.png)
   
     Необходимо создать набор данных? См. статью о [создании общего или внедренного набора данных](https://docs.microsoft.com/sql/reporting-services/report-data/create-a-shared-dataset-or-embedded-dataset-report-builder-and-ssrs).
2. Выберите тип диаграммы (в нашем случае это линейчатая диаграмма).
   
    ![Мастер диаграмм: тип диаграммы](media/quickstart-create-paginated-report/reportserver-paginated-choose-chart-type.png)
3. Упорядочите поля, перетаскивая их в окна **Категории**, **Серии** и **Значения**.
   
    ![Мастер диаграмм: Размещение полей](media/quickstart-create-paginated-report/reportserver-paginated-arrange-fields.png)
4. Нажмите кнопку **Далее** > **Готово**.

## <a name="step-3-design-your-report"></a>Шаг 3. Создание отчета
Теперь вы находитесь в представлении конструктора отчетов. Обратите внимание, что вы видите данные заполнителя, а не свои данные.

![Представление конструктора отчетов](media/quickstart-create-paginated-report/reportserver-paginated-preview-report.png)

* Чтобы просмотреть свои данные, выберите **Выполнить**.
  
     ![Запуск отчета](media/quickstart-create-paginated-report/reportserver-paginated-run-report.png)
* Чтобы вернуться в представление конструктора, выберите **Конструктор**.

Теперь можно изменить созданную диаграмму, изменив макет, значения или условные обозначения — то есть практические любые параметры.

Вы даже можете добавить любые визуализации: датчики, таблицы, матрицы, таблицы, схемы и т. д. Можно добавить верхние и нижние колонтитулы для нескольких страниц. См. [руководства по построителю отчетов](https://docs.microsoft.com/sql/reporting-services/report-builder-tutorials), чтобы попробовать все возможности.

![Представление построителя отчетов](media/quickstart-create-paginated-report/reportserver-paginated-finished-design-report.png)

## <a name="step-4-save-your-report-to-the-report-server"></a>Шаг 4. Сохранение отчета на сервере отчетов
Когда отчет будет готов, вы сможете сохранить его на сервере отчетов Power BI.

1. В меню **Файл** выберите **Сохранить как** и сохраните отчет на сервере отчетов. 
2. Теперь вы можете просмотреть его в браузере.
   
    ![Отчет с разбиением на страницы в браузере](media/quickstart-create-paginated-report/reportserver-paginated-report.png)

## <a name="next-steps"></a>Дальнейшие действия
Есть много отличных ресурсов, которые помогут вам создавать отчеты в построителе и в конструкторе отчетов в SQL Server Data Tools. Стоит начать с руководств по построителю отчетов.

* [Руководства по построителю отчетов](https://docs.microsoft.com/sql/reporting-services/report-builder-tutorials)
* [Что такое Сервер отчетов Power BI?](get-started.md)  

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](https://community.powerbi.com/)

