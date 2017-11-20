---
title: "Использование пользовательских визуализаций на основе R в Power BI"
description: "Использование пользовательских визуализаций на основе R в Power BI"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 1ab68b945c078e554e7d33914ed447d056a6d190
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="use-r-powered-custom-visuals-in-power-bi"></a>Использование пользовательских визуализаций на основе R в Power BI
Начиная с выпуска за октябрь 2016 г., в **Power BI Desktop** и **службе Power BI** можно использовать пользовательские визуализации на основе R (далее в этой статье — R-визуализации). Для этого не нужно знать язык R или писать на нем какие-либо сценарии. Это позволяет использовать аналитические и графические возможности визуализаций и сценариев R без изучения языка R и самостоятельного программирования на нем.

Чтобы использовать пользовательские R-визуализации, сначала выберите и скачайте нужный элемент из раздела **R-визуализаций** в коллекции Power BI **пользовательских визуальных объектов**.

![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_1.png)

В следующих разделах объясняется, как выбрать, скачать и использовать R-визуализации в **Power BI Desktop**.

### <a name="using-r-custom-visuals"></a>Использование пользовательских R-визуализаций
Чтобы использовать пользовательские R-визуализации, скачайте нужные объекты из библиотеки **пользовательских визуальных объектов**. После этого вы сможете использовать их, как любой другой визуальный элемент в **Power BI Desktop**. Это делается следующим образом.

1. Перейдите в библиотеку [пользовательских визуализаций](http://app.powerbi.com/visuals) по адресу [http://app.powerbi.com/visuals](http://app.powerbi.com/visuals). Выберите *ссылку на R-визуализации* в верхней части страницы.
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_2.png)
2. Выберите в коллекции **R-визуализацию**, которую вы хотите использовать. Откроется диалоговое окно с дополнительными сведениями. Нажмите кнопку **Download Visual** (Скачать визуальный элемент), чтобы скачать выбранный элемент.
   
   > [!NOTE]
> Для разработки в **Power BI Desktop** необходимо установить R на локальном компьютере. Если пользователь будет просматривать R-визуализации в **службе Power BI**, устанавливать R локально *не* нужно.
   > 
   > 
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_3.png)
   
   Чтобы использовать пользовательские R-визуализации в **службе Power BI**, вам не нужно устанавливать R. Но если вы хотите использовать пользовательские R-визуализации в **Power BI Desktop**, вам *необходимо* установить R на локальный компьютер. Вы можете загрузить R из таких расположений:
   
   * [CRAN 3.3.1](https://cran.r-project.org/bin/windows/base/R-3.3.1-win.exe)
   * [MRO 3.3.1](https://mran.microsoft.com/install/mro/3.3.1/microsoft-r-open-3.3.1.msi)
3. Скачав визуализацию (как любой другой файл в браузере), откройте **Power BI Desktop**, на панели **Визуализации** щелкните правой кнопкой мыши кнопку с многоточием (...) и выберите **Импортировать настраиваемый визуальный элемент**.
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_4.png)
4. Появится предупреждение об импорте пользовательских визуальных элементов, как показано на рисунке ниже.
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_5.png)
5. Перейдите в папку, в которой сохранен файл визуального элемента, и выберите этот файл. Пользовательские визуализации **Power BI Desktop** имеют расширение .pbiviz.
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_6.png)
6. Вернувшись в Power BI Desktop, вы увидите на панели **Визуализации** новый тип визуального элемента.
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_7.png)
7. После того как вы импортировали новую визуализацию или открыли отчет, который содержит настраиваемую R-визуализацию, служба **Power BI Desktop** начнет устанавливать требуемые пакеты R.
   
   ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_8.png)

На этом этапе вы можете добавить данные в визуальный элемент так же, как в любой другой визуальный элемент **Power BI Desktop**. По завершении вы увидите готовый визуальный элемент на холсте. В следующем примере R-визуализация **Forecasting** (Прогнозирование) используется с прогнозами ООН относительно рождаемости (визуализация слева).

![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_10.png)

Как и в случае с любым другим визуальным элементом **Power BI Desktop**, вы можете опубликовать отчет с R-визуализациями в **службе Power BI** и предоставить к нему доступ другим пользователям.

Регулярно посещайте библиотеку [пользовательских R-визуализаций](https://app.powerbi.com/visuals/R-powered), поскольку она постоянно пополняется.

### <a name="contributing-r-powered-custom-visuals"></a>Публикация пользовательских R-визуализаций
Если вы создаете собственные R-визуализации для использования в отчетах, вы можете делиться ими со всем миром, публикуя их в **коллекции пользовательских визуализаций**. Публикация выполняется через GitHub. Процесс описан по ссылке ниже.

* [Публикация в коллекцию пользовательских R-визуализаций](https://github.com/Microsoft/PowerBI-visuals#building-r-powered-custom-visual-corrplot)

### <a name="troubleshooting-r-powered-custom-visuals"></a>Устранение неполадок пользовательских визуальных элементов на основе R
Чтобы визуальные элементы на основе R работали правильно, необходимо соблюдать определенные зависимости. Если пользовательские визуальные элементы на основе R выполняются или загружаются неправильно, это свидетельствует о какой-то из описанных ниже проблем:

* отсутствие модуля R;
* ошибки в скрипте R, на котором основывается визуальный элемент;
* пакеты R отсутствуют или устарели.

В следующем разделе описаны действия по устранению возникших неполадок.

#### <a name="missing-or-outdated-r-packages"></a>Пакеты R отсутствуют или устарели
При попытке установить пользовательский визуальный элемент на основе R могут возникнуть ошибки, связанные с отсутствием или устареванием пакетов R. Обычно это вызвано одной из следующих причин:

* установленный экземпляр R несовместим с пакетом R;
* настройки брандмауэра, антивирусных программ или прокси-сервера препятствуют подключению R к Интернету;
* медленное подключение к Интернету или проблема с подключением к нему.

Команда Power BI работает над устранением этих проблем, прежде чем они повлияют на вашу работу. Следующий выпуск Power BI Desktop будет включать обновления для решения этих проблем. До появления следующего выпуска можно выполнить предложенные ниже действия по устранению проблем.

1. Удалите пользовательский визуальный элемент и установите его снова. Это вызовет переустановку пакетов R.
2. Если у вас установлена не последняя версия R, обновите ее. Затем удалите или переустановите пользовательский визуальный элемент, как описано выше.
   
   * Поддерживаемые версии R указаны в описании каждого пользовательского визуального элемента на основе R (см. рисунок ниже).
     ![](media/desktop-r-powered-custom-visuals/powerbi-r-powered-custom-viz_11.png)
     > [!NOTE]
> Вы можете не удалять исходный установленный экземпляр R и связать Power BI Desktop только с устанавливаемой текущей версией. Выберите **Файл > Параметры и настройки > Параметры > Создание R-скриптов**.
3. Установите пакеты R вручную с помощью любой консоли R. Ниже описано, как это сделать.
   
   а.  Загрузите скрипт установки визуальных элементов на основе R и сохраните этот файл на локальный жесткий диск.
   
   б.  Из консоли R выполните следующую команду:
   
       > source(“C:/Users/david/Downloads/ScriptInstallPackagesForForecastWithWorkarounds.R”)    
   
   Обычные расположения установки по умолчанию:
   
       c:\Program Files\R\R-3.3.x\bin\x64\Rterm.exe (for CRAN-R)
       c:\Program Files\R\R-3.3.x\bin\x64\Rgui.exe (for CRAN-R)
       c:\Program Files\R\R-3.3.x\bin\R.exe (for CRAN-R)
       c:\Program Files\Microsoft\MRO-3.3.x\bin\R.exe (for MRO)
       c:\Program Files\Microsoft\MRO-3.3.x\bin\x64\Rgui.exe (for MRO)
       c:\Program Files\RStudio\bin\rstudio.exe (for RStudio)
4. Если предыдущие действия неэффективны, сделайте следующее:
   
   а. В **R Studio** выполните действия, описанные в разделе 3б выше (выполните строку скрипта из консоли R).
   
   б. Если это не поможет, в **R Studio** откройте **Tools (Сервис) > Global Options (Глобальные параметры) > Packages (Пакеты)** и установите флажок **Use Internet Explorer library/proxy for HTTP** (Использовать библиотеку/прокси-сервер Internet Explorer для HTTP), а затем повторите действия из раздела 3б выше.

### <a name="next-steps"></a>Дальнейшие действия
Ознакомьтесь с дополнительными материалами по R в Power BI.

* [Коллекция пользовательских визуальных элементов Power BI](https://app.powerbi.com/visuals/)
* [Выполнение сценариев R в Power BI Desktop](desktop-r-scripts.md)
* [Создание визуальных элементов Power BI с помощью R](desktop-r-visuals.md)
* [Использование внешней среды R IDE с Power BI](desktop-r-ide.md)
