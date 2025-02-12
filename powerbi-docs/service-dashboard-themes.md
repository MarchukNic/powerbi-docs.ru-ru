---
title: Использование тем панели мониторинга в службе Power BI
description: Узнайте, как использовать настраиваемую цветовую палитру и применить ее ко всей панели мониторинга в службе Power BI
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 08/22/2018
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: 8e444c78c1f6f9f3f0be1375f96f7381489cc069
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61143716"
---
# <a name="use-dashboard-themes-in-power-bi-service"></a>Использование тем панели мониторинга в службе Power BI
С помощью **тем панели мониторинга** ко всей панели мониторинга можно применить требуемую цветовую тему, например корпоративные цвета, цвета времен года или другие цветовые темы. При применении **темы панели мониторинга** для всех визуальных элементов на панели мониторинга используются цвета из выбранной темы (c некоторыми исключениями, описанными далее в этой статье).

![пример панели мониторинга с темой](media/service-dashboard-themes/power-bi-full-dashboard-theme.png)

Изменение цветов для визуальных элементов отчета на панели мониторинга не влияет на визуальные элементы в отчете. Кроме того, при закреплении плиток из отчета, к которому уже [применена тема отчета](desktop-report-themes.md), можно оставить текущую тему или использовать тему панели мониторинга.


## <a name="prerequisites"></a>Предварительные требования
* Чтобы продолжить работу, откройте [панель мониторинга "Продажи и маркетинг — пример"](sample-datasets.md).


## <a name="how-dashboard-themes-work"></a>Как применяются темы панели мониторинга
Сначала откройте панель мониторинга, которую вы создали (или для которой имеете разрешение на изменение) и которую хотите настроить. Нажмите кнопку с многоточием (...) и выберите пункт **Тема панели мониторинга**. 

![пункт "Тема панели мониторинга"](media/service-dashboard-themes/power-bi-dashboard-theme.png)

В появившейся области панели мониторинга выберите одну из готовых тем.  В приведенном ниже примере мы выбрали тему **Темная**.

![Выбрана светлая тема](media/service-dashboard-themes/power-bi-theme-menu.png)

![Применена темная тема](media/service-dashboard-themes/power-bi-theme-dark.png)

## <a name="create-a-custom-theme"></a>Создание пользовательской темы

Тема по умолчанию для панелей мониторинга Power BI — **Светлая**. Чтобы настроить цвета или создать собственную тему, в раскрывающемся списке выберите пункт **Пользовательская**. 

![Выбор пункта "Пользовательская" в раскрывающемся списке](media/service-dashboard-themes/power-bi-theme-custom.png)

Чтобы создать собственную тему панели мониторинга, используйте пользовательские параметры. При добавлении фонового изображения рекомендуется, чтобы оно имело разрешение не менее 1920 x 1080 пикселей. Чтобы использовать изображение в качестве фона, отправьте его на общедоступный веб-сайт, скопируйте URL-адрес и вставьте его в поле для **URL-адреса изображения**. 

### <a name="using-json-themes"></a>Использование тем JSON
Другой способ создать пользовательскую тему — передать файл JSON с параметрами всех цветов, которые следует использовать для панели мониторинга. В Power BI Desktop авторы отчетов используют файлы JSON с целью [создания тем для отчетов](desktop-report-themes.md). Такие же файлы JSON можно передавать для панелей мониторинга. Кроме того, можно найти и передать файлы JSON со [страницы коллекции тем](https://community.powerbi.com/t5/Themes-Gallery/bd-p/ThemesGallery) в сообществе Power BI. 

![Сайт коллекции тем](media/service-dashboard-themes/power-bi-theme-gallery.png)

Вы также можете сохранить пользовательскую тему как файл JSON и поделиться им с другими создателями панелей мониторинга. 

### <a name="use-a-theme-from-the-theme-gallery"></a>Использование темы из коллекции тем

Так же как в случае со встроенными и пользовательскими параметрами, при передаче темы цвета применяются автоматически ко всем плиткам на панели мониторинга. 

1. Наведите указатель на тему и выберите пункт **Просмотреть отчет**.

    ![Просмотр отчета](media/service-dashboard-themes/power-bi-choose-theme.png)

2. Прокрутите содержимое окна вниз и найдите ссылку на файл JSON.  Щелкните значок скачивания и сохраните файл.

    ![JSON-файл Spring Day](media/service-dashboard-themes/power-bi-theme-json.png)

3. Вернувшись в службу Power BI, в окне пользовательской темы панели мониторинга нажмите кнопку **Отправить тему JSON**.

    ![Отправка файла JSON](media/service-dashboard-themes/power-bi-upload-theme.png)

4. Перейдите в расположение, в котором был сохранен JSON-файл темы, и нажмите кнопку **Открыть**.

5. На странице темы панели мониторинга нажмите кнопку **Сохранить**. Новая тема будет применена к панели мониторинга.

    ![применение новой темы](media/service-dashboard-themes/power-bi-json.png)

## <a name="considerations-and-limitations"></a>Рекомендации и ограничения

* Если в отчете используется тема, которая отличается от темы панели мониторинга, можно выбрать, сохранит ли визуальный элемент текущую тему или использует тему панели мониторинга для поддержания согласованности между визуальными элементами из разных источников. Чтобы оставить тему отчета при закреплении плитки на панели мониторинга, выберите параметр **Сохранить текущую тему**. Визуальный элемент на панели мониторинга сохранит тему отчета, включая параметры прозрачности. 

    Параметры **темы плиток** отображаются в единственной ситуации: если вы создали отчет в Power BI Desktop, [добавили тему отчета](desktop-report-themes.md), а затем опубликовали отчет в службе Power BI. 

    ![Выбранный параметр "Сохранить текущую тему"](media/service-dashboard-themes/power-bi-keep-current.png)

    Попробуйте повторно закрепить плитку и выбрать параметр **Использовать тему панели мониторинга**.

    ![Использовать целевую тему](media/service-dashboard-themes/power-bi-use-destination.png)

* Темы панели мониторинга не могут применяться к закрепленным динамическим страницам отчетов, плиткам IFrame, плиткам SSRS, плиткам книги или изображениям.
* Темы панели мониторинга можно просматривать на мобильных устройствах, но создавать их можно только в службе Power BI. 
* Пользовательские темы панели мониторинга работают только с плитками, закрепленными из отчетов. 

