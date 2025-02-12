---
title: Выполнение сценариев R в Power BI Desktop
description: Выполнение сценариев R в Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 188669525a210afc516cc9740d5d7e7c5682ea93
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65514732"
---
# <a name="run-r-scripts-in-power-bi-desktop"></a>Выполнение скриптов R в Power BI Desktop
Вы можете выполнять сценарии R непосредственно в **Power BI Desktop** и импортировать полученные наборы данных в модели данных Power BI Desktop.

## <a name="install-r"></a>Установка скрипта R
Для запуска сценариев R в Power BI Desktop необходимо установить **R** на локальном компьютере. Вы можете скачать и установить **R** бесплатно из различных расположений, включая [страницу скачивания Revolution Open](https://mran.revolutionanalytics.com/download/) и [репозиторий CRAN](https://cran.r-project.org/bin/windows/base/). В текущем выпуске R-скриптов в Power BI Desktop в пути установки поддерживаются символы Юникода, а также пробелы (пустые символы).

## <a name="run-r-scripts"></a>Выполнение скрипта R
С помощью всего нескольких действий в Power BI Desktop вы можете выполнять сценарии R и создать модель данных, из которой можно создавать отчеты и совместно использовать их в службе Power BI. Теперь R-скрипты в Power BI Desktop поддерживают числовые форматы, которые содержат десятичные знаки (.) и запятые (,).

### <a name="prepare-an-r-script"></a>Подготовка скрипта R
Чтобы запустить сценарий R в Power BI Desktop, создайте этот сценарий в локальной среде разработки R и убедитесь, что он выполняется успешно.

Чтобы запустить сценарий в Power BI Desktop, убедитесь, что этот сценарий успешно выполняется в новой и неизмененной рабочей области. Это означает, что все пакеты и зависимости должны загружаться и выполняться явным образом. Вы можете использовать *source()* для запуска зависимых сценариев.

При подготовке и выполнении сценария R в Power BI Desktop действуют некоторые ограничения.

* Импортируются только кадры данных, поэтому убедитесь, что импортируемые в Power BI данные представлены в кадре.
* Комплексные и векторные столбцы не импортируются, а в созданной таблице заменяются значениями ошибки.
* Значения Н/Д преобразуются в значения NULL в Power BI Desktop.
* Любой сценарий R, который выполняется дольше 30 минут, завершается по истечении времени ожидания.
* Интерактивные вызовы в сценарии R, например ожидание ввода данных пользователем, прерывают выполнение сценария.
* При настройке рабочего каталога в сценарии R *необходимо* задать полный, а не относительный путь каталога.

### <a name="run-your-r-script-and-import-data"></a>Выполнение скрипта R и импорт данных
1. Соединитель данных скрипта R в Power BI Desktop находится в области **Получить данные**. Чтобы выполнить сценарий R, выберите **Получить данные &gt; Подробнее…** , а затем выберите **Другие &gt; R-скрипт**, как показано на следующем рисунке:
   
   ![](media/desktop-r-scripts/r-scripts-1.png)
2. Если R установлен на локальном компьютере, в качестве подсистемы R выбирается самая новая установленная версия. Просто скопируйте сценарий в окне сценария и нажмите кнопку **ОК**.
   
   ![](media/desktop-r-scripts/r-scripts-2.png)
3. Если R не установлен, не определен или представлен несколькими разными установками на локальном компьютере, разверните **R Installation Settings** (Параметры установки R) для отображения параметров установки или выберите установку, в которой хотите запустить сценарий R.
   
   ![](media/desktop-r-scripts/r-scripts-3.png)
   
   Если R установлен, но не определен, можно явно указать его расположение в текстовом поле, отображаемом при развертывании области **Параметры установки R**. На приведенном выше рисунке в текстовом поле явным образом указан путь *C:\Program Files\R\R-3.2.0* .
   
   Параметры установки R централизованно расположены в разделе "Создание R-скриптов" в диалоговом окне "Параметры". Чтобы указать параметры установки R, выберите **Файл > Параметры и настройки**, а затем **Параметры > Создание R-скриптов**. Если доступно несколько установок R, появится раскрывающееся меню для выбора используемой установки.
   
   ![](media/desktop-r-scripts/r-scripts-4.png)
4. Нажмите кнопку **ОК** для выполнения сценария R. Если сценарий выполняется успешно, можно выбрать полученные кадры данных для добавления в модель Power BI.

### <a name="refresh"></a>Обновление
Вы можете обновить сценарий R в Power BI Desktop. При обновлении сценария R Power BI Desktop запускает его повторно в среде Power BI Desktop.

## <a name="next-steps"></a>Дальнейшие действия
Ознакомьтесь с дополнительными материалами по R в Power BI.

* [Создание визуальных элементов R в приложении Power BI Desktop](desktop-r-visuals.md)
* [Использование внешней среды R IDE с Power BI](desktop-r-ide.md)

