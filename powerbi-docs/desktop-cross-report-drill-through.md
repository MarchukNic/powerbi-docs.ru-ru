---
title: Использование детализации кросс отчет в Power BI Desktop
description: Узнайте, как перейти от одного к другой в Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 04/08/2019
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 45a7cdd3c7b5324f3d618eaba4bdb3968a9549a5
ms.sourcegitcommit: 8bf2419b7cb4bf95fc975d07a329b78db5b19f81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66375192"
---
# <a name="use-cross-report-drillthrough-in-power-bi-desktop"></a>Использование детализации кросс отчет в Power BI Desktop

С возможностью детализации кросс report в Power BI Desktop можно сегментировать переходить от одного отчета в другой отчет. Это верно до тех пор, пока отчеты находятся в пределах одной и той же рабочей области или приложения в службе Microsoft Power BI. Использование кросс report детализации для подключения двух и более отчетов, которые связывают содержимое, а также передавать контекст фильтра вместе с соединения отчета перекрестной. В этой статье вы узнаете, как настройка детализации кросс отчетов для отчетов Power BI и что пользователей с помощью кросс report детализации для себя.

![Параметр детализации снимок экрана Power BI Desktop](media/desktop-cross-report-drill-through/cross-report-drill-through-01.png)

Следующие определения важны для понимания, прежде чем начать настройке и использовании кросс report детализации:

* **Исходного визуального элемента:** Визуальный элемент, который вызывает действие детализации, используя visual контекстного меню.
* **Исходный отчет:** Отчет, который содержит исходный визуальный для кросс report детализации.
* **Конечная страница:** Страница, переходе пользователя на после инициации действия детализации.
* **Целевой отчет:** Отчет, который содержит целевой страницы для кросс report детализации.

## <a name="enable-cross-report-drillthrough"></a>Включение детализации кросс отчет

Чтобы включить отчет в качестве целевого детализированного отчета перекрестной, необходимо включить функцию для этого отчета в **параметры** окна. Перейдите к **файл** > **параметры и настройки** > **параметры**, а затем перейдите **параметры отчетов** практически нижней части страницы слева.

Выберите **разрешить визуальных элементов в этом отчете, чтобы использовать детализацию целевые объекты из других отчетов** флажок, как показано на следующем рисунке.

![Снимок экрана о параметрах окне с выделенным параметрами отчетов](media/desktop-cross-report-drill-through/cross-report-drill-through-02.png)

Теперь включена детализация кросс отчета.

## <a name="set-up-cross-report-drillthrough"></a>Настройка детализации кросс отчет

Настройка детализации отчета перекрестной аналогична Настройка детализации в отчет. Детализация включена на целевой странице, что другие визуальные элементы на странице включено для детализированного отчета. Шаги по созданию детализации в одном отчете, см. в разделе [использование детализации в Power BI Desktop](desktop-drillthrough.md).

Чтобы начать процесс установки, вам нужно выполнить несколько начальных действий:

* Настройте параметры страницы целевой объект детализации, к которому можно получить из других отчетов в рабочей области или приложении.
* Разрешить отчет для просмотра страниц детализации из за пределами его собственных отчетов.

Поиск параметров детализации в **поля** раздел **визуализации** области, как показано на следующем рисунке.

![Снимок экрана для визуализации области с выделенным параметров детализации](media/desktop-cross-report-drill-through/cross-report-drill-through-03.png)

Для проверки моделей данных для исходной и целевой отчетов является первым шагом Включение детализации для страницы. Убедитесь, что: 

* Поля, которые вы хотите передать существуют в обеих моделях данных.
* Имена полей и имена таблиц, к которым они принадлежат, идентичны (строк должно также совпадать и чувствительны к регистру).

Например, если вы хотите передать фильтра по полю *страны* внутри таблицы *Geography*, должен иметь обе модели *Geography* таблицы и *страны* поле в этой таблице. В противном случае необходимо обновить имя поля или имя таблицы в базовой модели. Достаточно обновить отображаемое имя поля не будет правильно работать для кросс report детализированного отчета. (Обратите внимание, что схемы в каждом отчете нет необходимости в точности совпадать.)

Чтобы приступить к работе с программой установки, необходимо подготовить целевой страницы. В Power BI Desktop, перейдите на страницу и убедитесь, что **кросс report** переключатель детализации устанавливается в **на**. 

![Снимок экрана отчета перекрестной переключатель в положении на](media/desktop-cross-report-drill-through/cross-report-drill-through-03.png)

Затем перетащите поля, которые вы хотите использовать в качестве целевой объект детализации на холст. Выберите поле для использования как категория, или суммировать как мера. На этом этапе можно выбрать, хотите ли вы отключите **сохранить все фильтры** переключатель для визуального элемента. Если вы не хотите передать другие примененные фильтры из источника visual вашей целевой объект детализации visual, выберите **Off**.

> [!NOTE]
> Если вы используете для детализированного отчета перекрестной только страницы, следует удалить **обратно** кнопка, которая добавляется автоматически. **Обратно** кнопка работает только для nagivation в одном отчете. 

После настройки визуального элемента, убедитесь в том, сохранить отчет в том случае, если вы находитесь в службе Power BI или сохранить и опубликовать отчет в том случае, если вы используете Power BI Desktop.

В предыдущем разделе описан способ включения детализации отчета перекрестной для Power BI Desktop (в **параметры** окна). Если вы используете службу Power BI для создания целевой детализированный отчет перекрестной, включение детализации отчета перекрестной необходимо выполнить следующее: 

1. Выберите рабочую область, в которой находятся целевой отчет и исходный отчет.
2. Выберите **отчеты**.
3. Выберите **параметры** значок для исходного отчета.
4. Убедитесь, что переключатель детализации отчета перекрестной **на**.
5. Сохраните отчет.

Вот и все. Ваш отчет готов для результатов отчета перекрестной детализации. 

В следующем разделе мы рассмотрим процесс работы с точки зрения пользователя.

## <a name="cross-report-drillthrough-experience"></a>Возможности детализации кросс отчет

При настройке качества детализации кросс отчета для отчета, можно поместить этот компонент для использования.

Выберите исходный отчет в службе Power BI, а затем выберите визуальный элемент, который использует поле или поля, указанные при настройке целевой страницы как. После этого щелкните правой кнопкой мыши точку данных, чтобы открыть visual контекстного меню и выберите **детализации**.

![Снимок экрана исходного отчета в службе Power BI с выделенным детализации](media/desktop-cross-report-drill-through/cross-report-drill-through-01.png)

Вы увидите результаты на целевой странице детализации кросс отчет, так же, как можно настроить их при создании целевой объект. Результаты будут отфильтрованы в соответствии с параметрами детализации.

> [!IMPORTANT]
> Power BI кэширует объекты детализации кросс report. Если вы вносите изменения, убедитесь, что вы обновите страницу в браузере, если вы не видите целей детализации должным образом. 

Целевые объекты кросс report отформатированы следующим образом: 

`Target Page Name [Target Report Name]`

После выбора целевой страницы, к которому требуется выполнить детализацию, Power BI переход на эту страницу. Передается контекст фильтра, в соответствии с параметрами целевой страницы. 

Контекст фильтра из исходного визуального элемента могут включать следующее: 

* Отчет, страницы и фильтры уровня визуальных элементов влияет на исходный визуальный. 
* Кроссфильтрации и перекрестного выделения, влияющие на исходный визуальный. 
* Срезы на странице, а также синхронизация срезов.
* Параметры URL-адреса.

Когда вы попадете в целевой отчет для детализированного отчета, Power BI применяется только фильтры для полей, для которых она обнаруживает, что соответствует точная строка для поля имени и имени таблицы. Power BI не применяется прикрепленные фильтры из целевого отчета. Это Однако применяется личные закладки по умолчанию, если он существует. Например, если личные закладки по умолчанию включает в себя фильтр на уровне отчета для *Country = US*, Power BI применяет фильтр, во-первых, перед применением контекст фильтра из исходного визуального элемента. 

Для детализации отчета между Power BI передает контекст фильтра все стандартные страницы в целевом отчете. Power BI не передать контекст фильтра для страниц подсказок, так как страниц подсказок фильтруются в источнике visual, который вызывает всплывающей подсказки.

Если вы хотите вернуться к отчету источника после действия детализации кросс отчет, используйте браузер **обратно** кнопки. 

## <a name="next-steps"></a>Дальнейшие действия

Рекомендуем также ознакомиться со следующими материалами:

* [Использование срезов в Power BI Desktop](visuals/power-bi-visualization-slicers.md)
* [Использование детализации в Power BI Desktop](desktop-drillthrough.md)

