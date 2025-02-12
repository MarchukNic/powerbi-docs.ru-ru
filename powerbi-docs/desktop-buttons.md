---
title: Использование кнопок в Power BI
description: Кнопки в Power BI Desktop позволяют вам создавать отчеты и панели мониторинга, которые работают как приложения и дают больше возможностей для взаимодействия пользователям
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/07/2019
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 9d884df7fdfa6d0f16e7963c00a1100186d70546
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65239500"
---
# <a name="using-buttons-in-power-bi"></a>Использование кнопок в Power BI
**Кнопки** в Power BI позволяют создавать отчеты и панели мониторинга, которые работают как приложения. С их помощью вы можете создать удобную среду, где пользователи могут эффективно взаимодействовать мышью с элементами Power BI. Добавив кнопки в отчеты **Power BI Desktop**, предоставьте к ним общий доступ или опубликуйте их в службе Power BI и создайте панели мониторинга, чтобы пользователи могли работать с отчетами, как с обычными приложениями.

![Кнопки в Power BI](media/desktop-buttons/desktop-buttons_01.png)

Кнопки, создаваемые в **Power BI Desktop**, могут использоваться в отчетах и панелях мониторинга, публикуемых в **службе Power BI**.

## <a name="creating-buttons-in-reports"></a>Создание кнопок в отчетах
Чтобы создать кнопку в отчете **Power BI Desktop**, на ленте **Главная** выберите элемент **Кнопки**. Появится раскрывающееся меню, где вы сможете выбрать нужные кнопки из доступных вариантов, как показано на следующем рисунке. 

![Добавление элемента управления "кнопка" в Power BI Desktop](media/desktop-buttons/desktop-buttons_02.png)

Когда вы создаете кнопку и выбираете ее на холсте отчета, в панели **Визуализации** отображаются разнообразные варианты настройки кнопки под ваши нужды. Например, вы можете добавить **Текст кнопки**, переместив ползунок соответствующей карточки в панели **Визуализации**. Вы также можете изменить значок кнопки, ее заливку, заголовок и действие, выполняемое при нажатии на кнопку в отчете или панели мониторинга, а также другие параметры.

![Форматирование кнопки в Power BI Desktop](media/desktop-buttons/desktop-buttons_03.png)

## <a name="set-button-properties-when-idle-hovered-over-or-selected"></a>Задание свойств кнопки при бездействии, наведении и выборе

У кнопок в Power BI есть три состояния: по умолчанию (кнопка не выбрана, и на нее не наведен указатель мыши), при наведении указателя мыши и при выборе (при *щелчке* по кнопке мышью). Многие карточки в панели **Визуализации** можно изменять на основе этих трех состояний. Таким образом, вы получаете значительную гибкость для индивидуальной настройки кнопок.

Следующие карточки в панели **Визуализации** позволяют изменять формат и поведение кнопки в зависимости от трех ее состояний.

* Текст кнопки
* Значок
* Контур
* Заливка

Чтобы настроить отображение кнопки для каждого состояния, разверните любую из этих карточек и откройте раскрывающийся список в ее верхней части. На следующем рисунке показана развернутая карточка **Контур** с раскрывающимся списком, содержащим три состояния кнопки.

![Три состояния кнопки в Power BI Desktop](media/desktop-buttons/desktop-buttons_04.png)


## <a name="select-the-action-for-a-button"></a>Выбор действия для кнопки

Вы можете выбрать действие, которое будет выполнено, когда пользователь нажмет кнопку в Power BI. Возможные действия для кнопки находятся в карточке **Действие** в панели **Визуализации**.

![Действие для кнопки в Power BI](media/desktop-buttons/desktop-buttons_05.png)

Для кнопок доступны следующие действия.

* Назад
* Закладка
* Вопросы и ответы

Действие **Назад** возвращает пользователя на предыдущую страницу отчета. Это особенно удобно для страниц детализации.

Действие **Закладка** открывает страницу по закладке, заданной для текущего отчета. См. [дополнительные сведения о закладках в Power BI](desktop-bookmarks.md). 

При выборе в раскрывающемся списке действия **Вопросы и ответы** открывается окно **Обозревателя вопросов и ответов**. 

Для определенных кнопок действие по умолчанию выбирается автоматически. Например, для кнопки типа **Вопросы и ответы** как действие по умолчанию автоматически выбирается **Вопросы и ответы**. Дополнительные сведения об **Обозревателе вопросов и ответов** см. в [этой записи блога](https://powerbi.microsoft.com/blog/power-bi-desktop-april-2018-feature-summary/#Q&AExplorer).

Чтобы опробовать созданные для отчета кнопки, нажимайте их, удерживая клавишу *CTRL*. 

## <a name="next-steps"></a>Дальнейшие действия
Дополнительные сведения о похожих функциях и о взаимодействии с кнопками см. в следующих статьях.

* [Использование детализации в Power BI Desktop](desktop-drillthrough.md)
* [Отображение плитки панели мониторинга или визуального элемента отчета в режиме фокусировки](consumer/end-user-focus.md)
* [Использование закладок для обмена аналитическими сведениями и создания историй в Power BI](desktop-bookmarks.md)

