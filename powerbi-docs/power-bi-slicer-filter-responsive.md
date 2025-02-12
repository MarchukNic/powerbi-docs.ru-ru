---
title: Создание адаптивного визуального элемента "Срез" в Power BI
description: Узнайте, как создать адаптивный визуальный элемент "Срез", размер которого можно изменять, чтобы он поместился в отчет
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/04/2018
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: fed4119946cb762fb4d9aee3b5300be225a6e379
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61419915"
---
# <a name="create-a-responsive-slicer-you-can-resize-in-power-bi"></a>Создание адаптивного визуального элемента "Срез" в Power BI

Адаптивные срезы изменяют размер, чтобы помещаться в любое пространство в отчете. Вы можете менять размеры и формы адаптивных срезов, например с горизонтального элемента на квадратный, с квадратного на вертикальный. Значения в срезе отобразятся в новом порядке в соответствии с изменениями. В Power BI Desktop и в службе Power BI можно делать адаптивными горизонтальные срезы и среды даты и диапазона. В срезах даты и диапазона также улучшена область сенсорного ввода, что позволяет легко изменять их. Вы можете как угодно уменьшать и увеличивать размер адаптивных срезов. Они также автоматически изменяют размер, чтобы помещаться в отчетах в службе Power BI и в мобильных приложениях Power BI. 

![Адаптивные срезы могут принимать любую форму](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-0-slicer.gif)

## <a name="create-a-slicer"></a>Создание среза

Чтобы создать динамический срез, сначала нужно создать базовый срез. 

1. Выберите значок **среза** ![Значок среза](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-0-slicer-icon.png) в области **Визуализации**.
2. Перетащите поле, по которому нужно выполнить фильтрацию, в область **Поле**.

    ![Добавление поля в срез](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-1-create.png)

## <a name="convert-to-a-horizontal-slicer"></a>Преобразование в горизонтальной срез

1. Выберите срез, а затем в области **Визуализации** выберите раздел **Формат**.
2. Разверните раздел **Общие**, затем для параметра **Ориентация** выберите значение **Горизонтальная**.

    ![Выбор горизонтальной ориентации](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-2-horizontal.png) 

1.  Возможно, потребуется расширить срез, чтобы показать дополнительные значения.

     ![Расширение среза](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-3-wider.png)

## <a name="make-it-responsive-and-experiment-with-it"></a>Как делать срез адаптивным и экспериментировать с ним

Это легко. 

1. Прямо под параметром **Ориентация** в разделе **Общие** вкладки **Формат** укажите для параметра **Адаптивный** значение **Вкл**.  

    ![Теперь это адаптивный срез](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-4-responsive-on.png)

1. Теперь вы можете экспериментировать со срезом. Перетащите углы, чтобы укоротить его, сделать выше, расширить или сузить. Если сделать его очень маленьким, он станет просто значком фильтра.

    ![Очень маленький адаптивный срез превратился в значок фильтра](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-5-mini-icon.png)

## <a name="add-it-to-a-phone-report-layout"></a>Добавление в макет отчета для телефона

В Power BI Desktop можно создать макет для телефона для каждой страницы отчета. Если для страницы есть макет для телефона, она отображается на мобильном телефоне в книжной ориентации. Если нет, она отображается в альбомной ориентации. 

1. В меню **Представление** выберите значок **Макет телефона**.

     ![Значок "Макет телефона", меню "Представление"](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-6-phone-layout-button.png)
    
1. Перетащите в сетку все визуальные элементы, которые нужно отобразить в отчете на телефоне. Если вы перетаскиваете адаптивный срез, измените его размер до нужного. В нашем случае это значок фильтра.

    ![Добавление среза в макет отчета для телефона](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-7-phone-slicer-icon.png)

Подробнее о создании [отчетов, оптимизированных для мобильных приложений Power BI](desktop-create-phone-report.md).

## <a name="make-a-time-or-range-slicer-responsive"></a>Как сделать адаптивным срез времени или диапазона

Нужно выполнить те же действия, чтобы сделать адаптивным срез времени или диапазона. После установки для параметра **Адаптивный** значения **Вкл.** вы увидите несколько изменений.

- Визуальные элементы оптимизируют порядок полей ввода в зависимости от размера, разрешенного на холсте. 
- Отображение элемента данных оптимизировано, чтобы срез был как можно более удобным в зависимости от размера, разрешенного на холсте. 
- Новый круглые ползунки оптимизируют взаимодействие при сенсорном вводе. 
- Когда визуальный элемент становится слишком мелким, он превращается в значок, который представляет тип визуального элемента на его месте. Для взаимодействия с ним просто дважды коснитесь значка, чтобы открыть визуальный элемент в режиме фокусировки. Таким образом на странице отчета сохраняется свободное пространство без потери функциональности.

## <a name="next-steps"></a>Дальнейшие действия

- [Срезы в службе Power BI](visuals/power-bi-visualization-slicers.md)
- Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)