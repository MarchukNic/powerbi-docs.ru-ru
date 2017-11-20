---
title: "Power BI — основные понятия"
description: "Power BI — основные понятия"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: B2vd4MQrz4M
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/31/2017
ms.author: mihart
ms.openlocfilehash: f20ea18fb46928bf7533caacf55a0cdb3d761571
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2017
---
# <a name="power-bi---basic-concepts-for-power-bi-service"></a>Power BI — основные понятия, связанные со службой Power BI
<!-- Shared newnav Include -->
[!INCLUDE [newnavbydefault](./includes/newnavbydefault.md)]

В этой статье предполагается, что вы уже [зарегистрировались для использования Power BI](service-self-service-signup-for-power-bi.md) и [добавили некоторые данные](service-get-data.md).

При запуске службы Power BI открывается ***панель мониторинга***. Наличие панелей мониторинга отличает службу Power BI от средства Power BI Desktop.

![](media/service-basic-concepts/completenewer.png)

Пользовательский интерфейс службы Power BI содержит следующие элементы:

1. Панель навигации
2. Панель мониторинга с плитками
3. Окно вопросов и ответов
4. Кнопки справки и отзывов
5. Заголовок панели мониторинга
6. Средство запуска приложений Office 365
7. Кнопки домашней страницы Power BI
8. Дополнительные действия на панели мониторинга

Мы рассмотрим эти элементы ниже, а сейчас давайте повторим некоторые основные понятия Power BI.

Или вы можете просмотреть это видео, прежде чем читать оставшуюся часть статьи.  В этом видео Уилл рассматривает основные понятия, связанные со службой Power BI.

<iframe width="560" height="315" src="https://www.youtube.com/embed/B2vd4MQrz4M" frameborder="0" allowfullscreen></iframe>


## <a name="power-bi-concepts"></a>Основные понятия Power BI
Три основных стандартных блока в Power BI: ***панели мониторинга***, ***отчеты*** и ***наборы данных***. Панели мониторинга и отчеты не могут не содержать данных (они могут быть пустыми, но это не имеет особого смысла, пока в них не появятся значения), поэтому начнем со знакомства с **наборами данных**.

## <a name="datasets"></a>Наборы данных
*Набор данных* — это коллекция данных, которые вы *импортируете* или к которым *подключаетесь*. С помощью Power BI можно импортировать наборы данных различных типов, подключиться к ним и просматривать информацию по всем наборам данных в одном месте.  

На панели навигации наборы данных, к которым вы подключены или которые вы импортировали, указаны под заголовком **Наборы данных**. Каждый указанный набор данных представляет один источник данных, например книгу Excel на OneDrive, локальный набор табличных данных службы SSAS или набор данных Salesforce. Уже поддерживается множество различных источников данных, и мы постоянно добавляем новые. [См. список типов наборов данных, которые могут использоваться с Power BI](service-get-data.md).

**ОДИН** набор данных...

* можно использовать многократно;
* можно использовать в различных отчетах;
* визуализации из этого одного набора данных можно отображать на нескольких разных панелях мониторинга.
  
  ![](media/service-basic-concepts/drawing2.png)

Чтобы [подключиться к набору данных или импортировать его](service-get-data.md), щелкните **Получить данные** в нижней части панели навигации или значок "плюс" рядом с заголовком **Наборы данных**. Следуйте инструкциям, чтобы подключиться к определенному источнику или импортировать его, и добавить набор данных в рабочую область. Новые наборы данных расположены на левой панели навигации с желтой звездочкой. Работа, выполняемая в Power BI, не приводит к изменению базового набора данных.

Если вы [участвуете в ***рабочей области приложения***](service-collaborate-power-bi-workspace.md), то наборы данных, добавленные одним участником рабочей области, будут доступны другим ее участникам.

Наборы данных можно обновлять, переименовывать, исследовать, удалять и использовать для создания отчетов. Для просмотра набора данных выберите его. При этом он откроется в редакторе отчетов, где вы сможете приступить к изучению данных и созданию визуализаций. Поэтому сейчас мы перейдем к следующей теме: отчетам.

### <a name="dig-deeper"></a>Дополнительная информация
* [Что такое Power BI Premium?](service-premium.md)
* [Получение данных для Power BI](service-get-data.md)
* [Образцы наборов данных и пакетов содержимого для Power BI](sample-datasets.md)

## <a name="reports"></a>Отчеты
Отчет в Power BI представлен в виде визуализаций (схем и диаграмм, например графиков, круговых диаграмм, диаграмм "дерево" и т. д.), размещенных на одной или нескольких страницах. Визуализации также называют ***визуальными элементами***. Все визуализации отчета связаны с одним набором данных. Отчеты можно создавать с нуля в Power BI, импортировать с помощью панелей мониторинга, опубликованных вашими коллегами, или создавать автоматически при подключении к наборам данных из Excel, Power BI Desktop, баз данных и приложений SaaS, а также [пакетов содержимого](service-organizational-content-pack-introduction.md).  Например, при подключении к книге Excel, содержащий листы Power View, Power BI создает отчет, основанный на этих таблицах. Когда вы подключаетесь к приложению SaaS, Power BI импортирует готовый отчет.

Просматривать отчеты и взаимодействовать с ними можно в [режиме чтения](service-report-open-in-reading-view.md) и [режиме правки](service-interact-with-a-report-in-editing-view.md).  Функции просмотра, конструирования, разработки и публикации в ***режиме правки*** доступны только его создателю, совладельцам, а также пользователям, которым предоставлены соответствующие разрешения. Пользователи, которым предоставлен доступ к отчету, могут просматривать его и взаимодействовать с ним в ***режиме чтения***.   

В области навигации ваши отчеты перечислены под заголовком **Отчеты**. Каждый из перечисленных отчетов содержит одну или несколько страниц визуализаций на основе одного базового набора данных. Чтобы открыть отчет, просто выберите его. По умолчанию отчет сначала открывается в режиме чтения.  Чтобы открыть отчет в представлении редактирования (при условии наличия необходимых разрешений), просто выберите **Изменить отчет**.  Если общая панель мониторинга содержит отчеты, вы НЕ увидите их в списке на панели навигации. Вместо этого вы можете открывать их непосредственно с этой панели с помощью плитки панели (дополнительные сведения об этом приведены ниже).

**ОДИН** отчет...

* может быть связан с несколькими панелями мониторинга (плитки из одного отчета могут отображаться на нескольких панелях);
* может быть создан с использованием данных из одного набора (небольшое исключение: приложение Power BI Desktop позволяет объединить в один отчет несколько наборов данных, и этот отчет можно импортировать в Power BI).
  
  ![](media/service-basic-concepts/drawing3new.png)

## <a name="dashboards"></a>Панели мониторинга
*Панель мониторинга* — это то, что создали вы или создал ваш коллега и предоставил вам для общего доступа. Это один холст, содержащий ноль или больше плиток и мини-приложений. На каждой плитке отображается одна [визуализация](power-bi-report-visualizations.md), созданная на основе набора и закрепленная на панели мониторинга. Добавить плитку на панель мониторинга можно различными способами, которые невозможно рассмотреть подробно в этой обзорной статье. Дополнительные сведения см. в статье [Плитки панели мониторинга в Power BI](service-dashboard-tiles.md). 

На панели навигации ваши панели мониторинга перечислены под заголовком **Панели мониторинга** . «Ваши» в данном случае означает, что у вас есть к ним доступ (при этом они могут быть созданы другими пользователями). Каждая из панелей мониторинга содержит настроенное представление некоторого подмножества базовых наборов данных.  Если вы являетесь владельцем панели мониторинга, у вас также есть доступ ко всем наборам данных, на которых она основана, и они отображаются на панели навигации в разделе **Наборы данных**.  Если вам был предоставлен доступ к панели мониторинга, рядом с ней отображается соответствующий значок ![](media/service-basic-concepts/sharing-icon.png), а связанные с ней наборы данных могут быть указаны либо не указаны на вашей панели навигации в зависимости от параметров совместного доступа.

> [!NOTE]
> Плитки и их закрепление подробнее рассмотрены ниже в разделе "Плитки панели мониторинга".
> 
> 

**ОДНА** панель мониторинга...

* может отображать визуализации из многих разных наборов данных;
* может отображать визуализации из многих разных отчетов;
* может отображать визуализации, закрепленные с помощью других средств (например, Excel).
  
  ![](media/service-basic-concepts/drawing1.png)

### <a name="dig-deeper"></a>Дополнительная информация
**Панель мониторинга можно [создать с нуля](service-dashboard-create.md)** — создайте новую пустую панель, а затем получите некоторые данные. 

**Вы или ваш коллега можете создать панель мониторинга и [предоставить ее для общего доступа](service-share-dashboards.md)**: когда вы принимаете соответствующее приглашение, общая панель мониторинга (а также связанные с ней отчет и набор данных) добавляются на панель навигации. В Power BI Pro требуется для совместного использования панели мониторинга и просмотра общей панели мониторинга.

**Иногда панели мониторинга импортируются с набором данных или создаются при подключении к набору данных**. Например, мастер **получения данных** для Salesforce запрашивает, нужна ли панель мониторинга и следует ли создать отчет из набора данных. 

**Зачем создаются панели мониторинга?**  Вот лишь некоторые причины:

* чтобы сразу просмотреть все сведения, необходимые для принятия решений;
* чтобы отслеживать наиболее важные сведения о бизнес-деятельности;
* чтобы убедиться, что все коллеги просматривают и используют в работе одни и те же сведения;
* для наблюдения за состоянием предприятия, продукта, подразделения, маркетинговой кампании и т. д.;
* для создания индивидуального представления большой панели мониторинга — со всеми важными метриками.

## <a name="my-workspace"></a>Моя рабочая область
Мы вернулись к панелям мониторинга и рабочей области Power BI. Теперь подробнее рассмотрим элементы целевой страницы службы Power BI.

![](media/service-basic-concepts/completenewer.png)

### <a name="1-navigation-bar-navbar"></a>1. **Панель навигации**
Панель навигации предназначена для перемещения между стандартными блоками Power BI — панелями мониторинга, отчетами и наборами данных.  

  ![](media/service-basic-concepts/navpane-new.png)

* Щелкните **Получить данные**, чтобы [добавить наборы данных, отчеты и панели мониторинга в Power BI](service-get-data.md).
* Разворачивайте и сворачивайте панель навигации с помощью значка ![](media/service-basic-concepts/expand-icon.png).
* Используйте поле **Поиск** , чтобы искать на панели навигации определенные элементы.
* Щелкните значок плюса ![](media/service-basic-concepts/pbi_nancy_plus.png), чтобы создать новую панель мониторинга или получить новый набор данных.
* Вам доступны перечисленные на панели навигации **панели мониторинга, отчеты** и **наборы данных** .  Общие панели мониторинга доступны только для чтения и отображаются со значком общего доступа ![](media/service-basic-concepts/sharing-icon.png).
* Имена панелей мониторинга, отчетов и наборов данных обычно соответствует имени файла базового набора данных, но вы можете [переименовать их](service-rename.md).
* Щелкните правой кнопкой мыши панель мониторинга, отчет или набор данных, чтобы открыть контекстное меню. 
  
  ![](media/service-basic-concepts/menu.png)

Щелкните один раз:

* заголовок, чтобы свернуть или развернуть его;
* панель мониторинга, чтобы отобразить ее;
* отчет, чтобы открыть его в режиме чтения;
* набор данных, чтобы изучить его.

### <a name="2-dashboard-with-tiles"></a>2. **Панель мониторинга с плитками**
Панели мониторинга состоят из [плиток](service-dashboard-tiles.md).  Плитки можно создать в представлении редактирования отчетов, с помощью компонента "Вопросы и ответы" или других панелей мониторинга, либо закрепить из Excel, SSRS и других источников. Плитка особого типа, называемая [мини-приложением](service-dashboard-add-widget.md), добавляется непосредственно на панель мониторинга. Плитки, которые отображаются на панели мониторинга, были специально помещены туда создателем или владельцем отчета.  Добавление плитки на панель мониторинга называется *закреплением*.

![](media/service-basic-concepts/canvas.png)

Дополнительные сведения см. выше в разделе **Панели мониторинга**.

### <a name="3-qa-question-box"></a>3. **Окно вопросов и ответов**
Один из способов исследования данных заключается в том, чтобы задать вопрос и позволить вопросам и ответам Power BI дать ответ в форме визуализации. Вопросы и ответы не могут использоваться для добавления содержимого в отчет — только для добавления содержимого в виде плиток в панели мониторинга.

Вопросы и ответы ищут ответ в наборах данных, подключенных к панели мониторинга.  Подключенный набор данных должен иметь по крайней мере одну плитку, закрепленную на этой панели мониторинга.

![](media/service-basic-concepts/qna.png)

Как только вы начинаете вводить свой вопрос, вы попадаете на страницу вопросов и ответов. По мере ввода вопросы и ответы помогают вам задать правильный вопрос и найти лучший ответ, используя перефразирование, автозаполнение, предложенные варианты и многое другое. Получив нужную визуализацию (ответ), закрепите ее на панели мониторинга. Дополнительные сведения см. в статье [Вопросы и ответы в Power BI](service-q-and-a.md).

### <a name="4-full-screen-notifications-settings-downloads-help-and-feedback"></a>4. **Значки полноэкранного режима, уведомлений, параметров настройки, загрузок, справки и обратной связи**
Значки в верхнем правом углу представляют ресурсы для параметров, уведомлений, скачиваний, получения справки и отправки отзывов команде Power BI. Чтобы развернуть панель мониторинга **во весь экран**, щелкните двойную стрелку.  

![](media/service-basic-concepts/help-new.png)

### <a name="5-dashboard-title-aka-what-dashboard-is-active"></a>5. **Заголовок панели мониторинга** (какая панель мониторинга активна?)
Не всегда легко понять, какая панель мониторинга активна.  Заголовок панели мониторинга отображается на странице представления панели мониторинга, на странице вопросов и ответов, в режиме правки отчета, в режиме чтения отчета и при открытии набора данных.   

![](media/service-basic-concepts/dash-title-new.png)

### <a name="6-office-365-app-launcher"></a>6. **Средство запуска приложений Office 365**
Средство запуска приложений помогает вам получить доступ к приложениям Office 365.

![](media/service-basic-concepts/basicconcepts2-newer.png)

### <a name="7-power-bi-home"></a>7. **Главная страница Power BI**
Выберите этот элемент, чтобы вернуться к панели мониторинга, которую вы просматривали последней.

   ![](media/service-basic-concepts/version-new.png)

### <a name="8-options"></a>8. **Параметры**
Эта область панели мониторинга содержит значки для взаимодействия с ней.  Рядом со значками **добавления плитки**, **просмотра избранного** и **предоставления общего доступа** есть многоточие. Если щелкнуть его, появятся команды для дублирования, печати, обновления панели мониторинга и выполнения других действий.

   ![](media/service-basic-concepts/options.png)

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)  
[Видео о службе Power BI](videos.md)  
[Что такое Power BI Premium?](service-premium.md)

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)
