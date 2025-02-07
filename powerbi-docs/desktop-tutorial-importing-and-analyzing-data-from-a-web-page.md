---
title: Руководство. Импорт и анализ данных веб-страницы
description: Руководство. Импорт и анализ данных веб-страницы с помощью Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: tutorial
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Learn more
ms.openlocfilehash: d6cdcf47b42be4a9b541aa355efb3dd5e9667204
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65514640"
---
# <a name="tutorial-analyze-web-page-data-using-power-bi-desktop"></a>Руководство. Анализ данных веб-страницы с помощью Power BI Desktop

Предположим, что вы уже долгое время являетесь футбольным болельщиком и хотите получить сведения о победителях Чемпионата Европы по футболу за разные годы. Power BI Desktop поможет вам импортировать в отчет нужные данные с веб-страницы и создать на их основе визуализации. Из этого руководства вы узнаете, как с помощью Power BI Desktop выполнить следующие действия:

- подключение к источнику данных в Интернете и переход по доступным в нем таблицам;
- сбор и преобразование данных в **редакторе Power Query**;
- присвоение запросу имени и импорт этого запроса в отчет Power BI Desktop; 
- создание и настройка визуализаций карты и круговой диаграммы.

## <a name="connect-to-a-web-data-source"></a>Подключение к веб-источнику данных

Данные о победителях Чемпионата Европы по футболу УЕФА можно найти в таблице результатов на странице Википедии по адресу http://en.wikipedia.org/wiki/UEFA_European_Football_Championship. 

![Таблица результатов в Википедии](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage1.png)

Обратите внимание на то, что веб-подключения устанавливаются только с помощью обычной проверки подлинности. Веб-сайты, требующие проверки подлинности, могут работать неправильно с веб-соединителем.

Чтобы импортировать данные, выполните следующие действия:

1. В Power BI Desktop на вкладке ленты **Главная** щелкните стрелку рядом с элементом **Получить данные** и в раскрывающемся списке выберите вариант **Интернет**.
   
   ![Элемент "Получить данные" на ленте](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web3.png) 
   
   >[!NOTE]
   >Можно также выбрать сам элемент **Получить данные** или элемент **Получить данные** в диалоговом окне Power BI **Начало работы**. После этого выберите **Интернет** из раздела **Все** или **Другое** в диалоговом окне **Получение данных** и щелкните **Подключить**.
   
2. В диалоговом окне **Из Интернета** вставьте URL-адрес `http://en.wikipedia.org/wiki/UEFA_European_Football_Championship` в текстовое поле **URL-адрес** и нажмите кнопку **ОК**.
   
    ![Получение данных из файлов](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web2.png)
   
   Когда вы установите подключение к веб-странице Википедии, откроется диалоговое окно Power BI **Навигатор** со списком доступных на этой странице таблиц. Вы можете выбрать имя любой таблицы, чтобы просмотреть содержащиеся в ней данные. Нужная нам информация содержится в таблице **Results[edit]** , но сейчас у нее не совсем удобный формат. Вам нужно обработать и очистить эти данные, прежде чем загружать их в отчет. 
   
   ![Диалоговое окно "Навигатор"](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/tutorialimanaly_navigator.png)
   
   >[!NOTE]
   >На панели **Предварительный просмотр** отображается только одна таблица, которую вы выбрали последней, но при выборе действия **Изменить** или **Загрузить** все выбранные таблицы будет загружены в **редактор Power Query**. 
   
3. Выберите таблицу **Results[edit]** в списке **Навигатор** и щелкните **Изменить**. 
   
   В **редакторе Power Query** откроется окно предварительного просмотра таблицы, где вы можете применить преобразования для очистки данных. 
   
   ![Редактор Power Query](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage3.png)
   
## <a name="shape-data-in-power-query-editor"></a>Формирование данных в редакторе Power Query

Чтобы данные было удобнее просматривать, сохраните в списке для отображения только годы и страны-победительницы. Для этого в **редакторе Power Query** можно применить процессы обработки и очистки.

Сначала удалите все столбцы, кроме **Year** (Год) и **Final Winners** (Победители финала).

1. В **редакторе Power Query** выберите столбцы **Year** (Год) и **Final Winners** (Победители финала). Чтобы выбрать несколько элементов, удерживайте нажатой клавишу **CTRL**.
   
2. Щелкните выбранные элементы правой кнопкой мыши и выберите в раскрывающемся меню действие **Удалить другие столбцы** или последовательно выберите **Удалить столбцы** > **Удалить другие столбцы** в группе **Управление столбцами** на вкладке ленты **Главная**. После этого все столбцы будут удалены из таблицы. 
   
   !["Удалить другие столбцы" в раскрывающемся списке](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web6.png) или !["Удалить другие столбцы" на ленте](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage4.png)

Теперь удалите лишнее слово **Details** (Сведения) из ячеек столбца **Year** (Год).

1. Выберите столбец **Year** (Год).
   
2. Щелкните его правой кнопкой мыши и выберите в раскрывающемся меню **Замена значений** или выберите **Замена значений** в группе **Преобразования** на вкладке ленты **Главная** (этот же пункт есть и в группе **Любой столбец** на вкладке **Преобразование**). 
   
   !["Замена значений" в раскрывающемся списке](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web7.png) или !["Замена значений" на ленте](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web8a.png)
   
3. В диалоговом окне **Замена значений** введите строку **Details** (Сведения) в текстовом поле **Значение для поиска**, а текстовое поле **Replace With** (Заменить на) оставьте пустым. Затем нажмите кнопку **ОК**, чтобы удалить слово "Details" (Сведения) из всех ячеек в столбце **Year** (Год).
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage6.png)

В некоторых ячейках поля **Year** (Год) вместо номера года есть только слово "Year" (Год). Установите фильтр по столбцу **Year** (Год), чтобы отображались только строки без слова "Year" (Год). 

1. Выберите стрелку раскрывающегося списка фильтра в столбце **Year** (Год).
   
2. Прокрутите вниз раскрывшийся список и снимите флажок рядом с вариантом **Year** (Год), а затем нажмите кнопку **ОК**, чтобы удалить строки, в которых столбец **Year** (Год) содержит только слово "Year" (Год). 

   ![Фильтрация данных](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage7.png)

Итак, вы очистили столбец **Year** (Год). Теперь можно приступать к столбцу **Final Winner** (Победитель финала). Так как в этом списке и так остались только победители финалов, вы можете смело присвоить ему имя **Country**(Страна). Чтобы переименовать столбец, сделайте следующее:

1. Дважды щелкните или нажмите и удерживайте заголовок столбца **Final Winner** (Победитель финала). 
   - Или щелкните правой кнопкой мыши заголовок столбца **Final Winners** (Победители финала) и выберите в открывшемся меню действие **Переименовать**. 
   - Либо же выберите столбец **Final Winners** и выберите команду **Переименовать** в группе **Любой столбец** на вкладке ленты **Преобразование**. 
   
   !["Переименовать" в раскрывающемся списке](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage7a.png) или !["Переименовать" на ленте](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web8.png)
   
2. Введите в заголовок текст **Country** (Страна) и нажмите клавишу **ВВОД**, чтобы переименовать столбец.

Также есть смысл отфильтровать некоторые строки, например за 2020-й год, чтобы в столбце **Country** (Страна) не осталось пустых значений. Для этого примените меню фильтра, как вы уже делали со значениями столбца **Year** (Год), или сделайте следующее:

1. Щелкните правой кнопкой мыши ячейку **Country** (Страна) в строке **2020**, которая содержит значение *NULL*. 
2. Последовательно выберите в контекстном меню **Текстовые фильтры** > **Не равно**, чтобы удалить все строки с таким же значением этой ячейки.
   
   ![Фильтрация по тексту](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web11.png)
   
## <a name="import-the-query-into-report-view"></a>Импорт запроса в представление отчета

Теперь вы подготовили данные в нужном формате, и этот запрос можно импортировать в отчет, присвоив ему имя "Euro Cup Winners" (Победители Чемпионата Европы).

1. В области **Параметры запроса** в текстовом поле **Имя** введите **Euro Cup Winners**(Победители Чемпионата Европы) и нажмите клавишу **ВВОД**.
   
   ![Присвоение запросу имени](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage8.png)

2. Последовательно выберите **Close & Apply (Закрыть и применить)**  > **Close & Apply (Закрыть и применить)** на вкладке ленты **Главная**.
   
   ![Закрыть и применить](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage9.png)
   
Созданный запрос будет загружен в **представление отчета** Power BI Desktop, где вы увидите его на панели **Поля**. 
   
   ![Панель "Поля"](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage11.png)
>[!TIP]
>Вы можете в любой момент снова открыть **редактор Power Query**, чтобы изменить и (или) уточнить запрос, выполнив одну из описанных ниже последовательностей действий:
>- выберите кнопку **Дополнительные параметры** с символом многоточия ( **...** ) рядом с отчетом **Euro Cup Winners** (Победители Чемпионата Европы) на панели **Поля** и выберите действие **Изменить запрос** в раскрывающемся списке;
>- выберите **Изменить запросы** > **Изменить запросы** в группе **Внешние данные** на вкладке ленты **Главная** в представлении отчета. 

## <a name="create-a-visualization"></a>Создание визуализации

Чтобы создать визуализацию на основе данных, сделайте следующее: 

1. Выберите поле **Country** (Страна) на панели **Поля** или перетащите это поле на холст отчета. Power BI Desktop автоматически распознает, что эти данные содержат названия стран, и создает визуализацию **карты**. 
   
   ![Визуализация карты](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web14.png)
   
2. Увеличьте эту карту, перетаскивая маркеры в ее углах, чтобы были видны имена всех победителей.  

   ![Увеличение карты](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage14.png)
   
3. На этой карте все точки, обозначающие страны-победительницы Чемпионата Европы по футболу, обозначены одинаковыми маркерами. Чтобы размер маркера отображал количество побед для каждой страны, перетащите поле **Year** (Год) в область **Drag data fields here** (Перетащите сюда поля данных) под элементом **Размер** в нижней части области **Визуализации**. Это поле автоматически преобразуется в меру **Count of Year** (Число значений Year), и на визуализации карты увеличится размер точек данных для тех стран, которые выиграли турнир несколько раз. 
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage15.png)
   

## <a name="customize-the-visualization"></a>Настройка визуализации

Вы убедились, что можно очень легко создать визуализации на основе данных. Ничуть не сложнее будет настроить эти визуализации, чтобы данные было удобно просматривать. 

### <a name="format-the-map"></a>Форматирование карты
Чтобы изменить внешний вид визуализации, выберите ее, а затем выберите значок **Формат** (с изображением валика) на панели **Визуализации**. Например, точка данных "Germany" (Германия) на этой визуализации вводит пользователя в заблуждение: дважды турнир выигрывала ФРГ и один раз объединенная Германия. Эти две точки накладываются друг на друга, но не объединяются и не разделяются. Чтобы прояснить эту ситуацию, раскрасьте точки разными цветами. Также вы можете присвоить диаграмме более подробный и привлекательный заголовок. 

1. Выберите визуализацию и щелкните значок **Формат**, а затем выберите **Цвета данных**, чтобы развернуть параметры цветов данных. 
   
   ![Форматирование цветов данных](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web15.png)
   
2. Для параметра **Показать все** выберите значение **Включено**, а затем выберите значок раскрывающегося списка рядом с элементом **West Germany** (ФРГ) и выберите для него желтый цвет. 
   
   ![Изменение цвета](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web16.png)
   
3. Выберите **Заголовок**, чтобы развернуть параметры заголовка, и замените текущее значение поля **Текст заголовка** текстовой строкой **Euro Cup Winners** (Победители Чемпионата Европы). 
4. Укажите для параметра **Цвет шрифта** значение "Красный", затем установите для параметра **Размер текста** значение **12** и измените **семейство шрифтов** на **Segoe (Bold)** (Segoe (полужирный)). 
   
   ![Форматирование цветов данных](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web17.png)
   

Теперь визуализация карты выглядит примерно так:

![Визуализация карты после настройки формата](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web18.png)
   
### <a name="change-the-visualization-type"></a>Изменение типа визуализации
Вы можете изменить тип визуализации, выбрав нужную визуализацию и значок другого типа в верхней части панели **Визуализация**. Например, на нашей визуализации карты отсутствуют данные для СССР и Чехословакии, поскольку их больше нет на карте мира. Другой тип визуализации, например диаграмма дерева или круговая диаграмма могут оказаться более точными, так как на них отображаются все значения. 

Чтобы заменить карту на круговую диаграмму, выберите карту и щелкните значок **круговой диаграммы** на панели **Визуализация**. 
   
![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web19.png)

>[!TIP]
>- После этого можно изменить **цвета данных**, чтобы ФРГ и объединенная Германия отображались одним и тем же цветом. 
>- Чтобы страны с наибольшим количеством побед отображались на круговой диаграмме рядом, выберите кнопку с многоточием ( **...** ) в верхнем правом углу визуализации и щелкните **Sort by Count of Year** (Сортировать по числу значений Year) в раскрывающемся списке. 

Power BI Desktop предоставляет удобные возможности для получения данных из разнообразных источников и их обработки для анализа и визуализации в интерактивном режиме. Готовый отчет можно [отправить в Power BI](desktop-upload-desktop-files.md) и создать на его основе панели мониторинга, к которым можно предоставить общий доступ для других пользователей Power BI.

## <a name="see-also"></a>См. также:
* [Прочитайте другие руководства по Power BI Desktop.](http://go.microsoft.com/fwlink/?LinkID=521937)
* [Посмотрите видеоматериалы по Power BI Desktop.](http://go.microsoft.com/fwlink/?LinkID=519322)
* [Посетите форум Power BI.](http://go.microsoft.com/fwlink/?LinkID=519326)
* [Прочитайте блог, посвященный Power BI.](http://go.microsoft.com/fwlink/?LinkID=519327)

