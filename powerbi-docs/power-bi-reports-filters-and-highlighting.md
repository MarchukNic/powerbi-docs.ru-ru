---
title: Фильтры и выделение в отчетах Power BI
description: О фильтрах и выделении в отчетах Power BI
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/22/2019
ms.author: maggies
LocalizationGroup: Reports
ms.openlocfilehash: 4584ad0f8c083a765b1a1a9943496b40a3ed4bdf
ms.sourcegitcommit: dc0258bb4f647ff646c6fff2aaffa29b413aa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/19/2019
ms.locfileid: "68342159"
---
# <a name="filters-and-highlighting-in-power-bi-reports"></a>Фильтры и выделение в отчетах Power BI
 Эта статья описывает фильтрацию и выделение данных в службе Power BI. В Power BI Desktop применяется практически такая же процедура. *Фильтры* удаляют все данные, кроме необходимых. *Выделение* отличается от фильтрации. Данные не удаляются — вместо этого выделяется подмножество видимых данных. При этом невыделенные данные остаются видимыми, но затемненными.

Есть много способов фильтровать и выделять отчеты в Power BI. Включение всех этих сведений в одну статью могло привести к путанице, поэтому мы разделили их на следующие разделы:

* Общие сведения о фильтрах и выделении (статья, которую вы читаете сейчас).
* Способы [создания и использования фильтров в режиме правки](power-bi-report-add-filter.md) в отчетах в Power BI Desktop и службе Power BI. При наличии разрешения на правку отчета можно создавать, изменять и удалять фильтры в отчетах.
* Способы [фильтрации и выделения визуальных элементов в отчете, к которому вам предоставлен совместный доступ,](consumer/end-user-interactions.md) в режиме чтения отчета в службе Power BI. При этом доступные операции ограничены, но вам предоставлен широкий набор возможностей фильтрации и выделения.  
* Подробный обзор [элементов управления фильтрации и выделения, доступных в режиме правки ](power-bi-report-add-filter.md) в Power BI Desktop и службе Power BI. Эта статья подробно рассматривает типы фильтров, например основанные на дате и времени, числовых значениях и тексте. Она также описывает различия между основными и дополнительными параметрами.
* После изучения возможностей фильтрации и выделения, доступных по умолчанию, ознакомьтесь со сведениями о том, как [изменить способ взаимной фильтрации и выделения для визуализаций](service-reports-visual-interactions.md).

**Знаете ли вы?** В Power BI доступны новые функции фильтров, предоставляемые в предварительной версии. См. дополнительные сведения о [новых функциях фильтров в отчетах Power BI](power-bi-report-filter.md).

![Новые функции фильтров](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading.png)


## <a name="intro-to-the-filters-pane"></a>Знакомство с панелью "Фильтры"

Фильтры можно применить на панели **Фильтры** или [выбрав срезы](visuals/power-bi-visualization-slicers.md) непосредственно в отчете. На панели "Фильтры" отображаются таблицы и поля, используемые в отчете, а также примененные фильтры, если таковые есть. 

![Панель "Фильтры"](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-reading-view.png)

Существует четыре типа фильтров.

- **Фильтр страницы** применяется ко всем визуальным элементам на странице отчета.     
- **Фильтр визуального элемента** применяется к одному визуальному элементу на странице отчета. Фильтры визуальных элементов отображаются, только если вы выбрали визуальный элемент на холсте отчета.    
- **Фильтр отчета** применяется ко всем страницам в отчете.    
- **Фильтр детализации** применяется к одной сущности в отчете.    

В режимах чтения и правки можно выполнять поиск с помощью фильтров страницы, визуального элемента и отчета, чтобы найти и выбрать нужное значение. 

![Поиск в фильтре](media/power-bi-reports-filters-and-highlighting/power-bi-search-filter.png)

Если рядом с фильтром стоит слово **All** (Все), значит все значения поля включены в фильтр.  Например, **Chain(All)** на снимке экрана ниже означает, что страница отчета включает данные обо всех торговых сетях.  В свою очередь, фильтр уровня отчета **FiscalYear is 2013 or 2014** означает, что в отчет включены только данные за 2013 и 2014 финансовые годы.

## <a name="filters-in-reading-or-editing-view"></a>Фильтры в режиме чтения или правки
Существует два режима взаимодействия с отчетами: [режим чтения](consumer/end-user-reading-view.md) и режим правки. Доступные возможности фильтрации зависят от используемого режима.

* В режиме правки можно добавлять фильтры страниц, отчетов, детализаций и визуальных элементов. При сохранении отчета фильтры сохраняются вместе с ним, даже если он открыт в мобильном приложении. Пользователи, просматривающие отчет в режиме чтения, могут работать с добавленными вами фильтрами, но не могут добавлять новые фильтры.
* В режиме чтения можно взаимодействовать с любыми уже существующими в отчете фильтрами, а также сохранять выбранные элементы. Новые фильтры добавлять нельзя.

### <a name="filters-in-reading-view"></a>Фильтры в режиме чтения
При наличии доступа к отчету только в режиме чтения панель "Фильтры" выглядит примерно так, как на этом снимке экрана:

![Фильтры в режиме чтения](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading-view.png)

На этой странице отчета есть шесть фильтров уровня страницы и один фильтр уровня отчета.

Каждый визуальный элемент может иметь фильтры для всех своих полей, и автор отчета может добавлять дополнительные фильтры. На изображении ниже к пузырьковой диаграмме применены шесть фильтров.

![Фильтр уровня визуальных элементов](media/power-bi-reports-filters-and-highlighting/power-bi-filter-visual-level.png)

Просмотрите данные в режиме чтения, изменяя существующие фильтры. Вносимые изменения сохраняются вместе с отчетом, даже если он открыт в мобильном приложении. Сведения об этом можно найти в [описании панели "Фильтры" отчета](consumer/end-user-report-filter.md).

При закрытии отчета фильтры сохраняются. Чтобы отменить настройки фильтрации и вернуться к настройкам фильтрации, срезов, детализации и сортировки по умолчанию, заданным автором отчета, в строке меню сверху выберите **Вернуться к значениям по умолчанию**.

![Значок возврата значений по умолчанию](media/power-bi-reports-filters-and-highlighting/power-bi-reset-to-default.png)

### <a name="filters-in-editing-view"></a>Фильтры в режиме правки
Если у вас есть разрешения владельца и вы открываете отчет в режиме правки, доступна не только панель **Фильтры**, но и несколько других панелей правки.

![Панель "Фильтры" в режиме правки](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-editing-view.png)

Как и в режиме чтения, на этой странице отчета есть шесть фильтров уровня страницы и один фильтр уровня отчета. Если выбрать пузырьковую диаграмму, мы увидим, что к ней применены шесть фильтров уровня визуальных элементов.

Фильтры и выделение в режиме правки предоставляют дополнительные возможности. В первую очередь мы можем добавлять новые фильтры. См. сведения о [добавлении фильтра в отчет](power-bi-report-add-filter.md) и других возможностях.

## <a name="ad-hoc-highlighting"></a>Индивидуальное выделение
Выберите значение или метку оси в визуальном элементе, чтобы выделить другие визуальные элементы на странице. Чтобы удалить выделение, снова выберите значение или любое пустое место в том же визуальном элементе. Выделение дает возможность быстро и легко анализировать влияние данных. Сведения о настройке перекрестного выделения такого типа см. в статье о [взаимодействии с визуальными элементами](service-reports-visual-interactions.md).

![Перекрестное выделение](media/power-bi-reports-filters-and-highlighting/power-bi-adhoc-filter.gif)


## <a name="next-steps"></a>Дальнейшие действия

[Новые функции фильтров в отчетах Power BI](power-bi-report-filter.md)

[Добавление фильтра в отчет (в режиме правки)](power-bi-report-add-filter.md)

[Ознакомление с фильтрами отчетов](consumer/end-user-report-filter.md)

[Взаимодействие с визуализациями в отчете Power BI](consumer/end-user-interactions.md)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)

