---
title: Руководство. Изучение Сервера отчетов Power BI в виртуальной машине
description: С помощью этого руководства вы создадите виртуальную машину с установленным Сервером отчетов Power BI и изучите его веб-портал.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: tutorial
ms.date: 05/06/2019
ms.author: maggies
ms.openlocfilehash: d30a396eeb4d461d7c36cecf9759306236810cab
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65240071"
---
# <a name="tutorial-explore-the-power-bi-report-server-web-portal-in-a-vm"></a>Руководство. Изучение возможностей веб-портала Сервера отчетов Power BI на виртуальной машине
С помощью этого руководства вы создадите виртуальную машину с установленным Сервером отчетов Power BI, чтобы изучить возможности просмотра, редактирования и управления, предоставляемые в Power BI. В руководстве используется пример отчетов с разбивкой на страницы и ключевых показателей эффективности.

![Веб-портал сервера отчетов](media/tutorial-explore-report-server-web-portal/power-bi-report-server-browser-in-vm-no-numbers.png)

В рамках этого руководства выполняются следующие задачи:

> [!div class="checklist"]
> * создание виртуальной машины и подключение к ней;
> * запуск веб-портала Сервера отчетов Power BI и навигация по нему;
> * назначение тега избранному элементу;
> * просмотр и редактирование отчета Power BI;
> * просмотр, изменение отчета с разбивкой на страницы и управление им;
> * просмотр книги Excel в Excel Online.

Для работы с этим руководством требуется подписка Azure. Если у вас ее нет, [создайте бесплатную учетную запись](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) перед началом работы.

## <a name="create-a-power-bi-report-server-vm"></a>Создание виртуальной машины для Сервера отчетов Power BI

Команда разработки Power BI подготовила очень удобный образ виртуальной машины с предустановленным Сервером отчетов Power BI.

1. В Azure Marketplace выберите сервер отчетов Power BI. Эта ссылка открывает его напрямую: [Сервер отчетов Power BI](https://azuremarketplace.microsoft.com/marketplace/apps/reportingservices.technical-preview?tab=Overview).  

2. Выберите **Get it now** (Получить).
3. Щелкните **Продолжить**, чтобы подтвердить согласие с условиями использования и политикой конфиденциальности.

4. Выберите **Создать**.

    ![Создание виртуальной машины для Сервера отчетов Power BI](media/tutorial-explore-report-server-web-portal/power-bi-report-server-create.png)

5. В **основы шаг 1**, для **имя виртуальной Машины**, вызвать его **reportservervm**.

    Имя виртуальной Машины для сервера отчетов BI Power, не может содержать дефисы.

5. Назначьте имя пользователя и пароль.

6. Для **группы ресурсов**выберите **создать**и назовите его **reportserverresourcegroup** > **ОК**.

    Если вы проходите учебник несколько раз, нужно дать группе ресурсов другое имя. В одной подписке невозможно использовать два одинаковых имени группы ресурсов. 

    ![Присвоение имен виртуальной машине и группе ресурсов](media/tutorial-explore-report-server-web-portal/power-bi-report-server-create-resource-group.png)

7. Для остальных параметров сохраните значения по умолчанию и нажмите кнопку **ОК**.

8. В **шаг 2 параметров**, оставить значения по умолчанию > **ОК**.
 
    **Учетную запись хранения SQL** и **учетной записи хранения диагностики** значения должны быть уникальными. Если более одного раза ознакомьтесь с руководством необходимо присвоить им разные имена.

9. В **Сводка 3 шага**, просмотрите выбранные параметры > **ОК**.

10. В **шаг 4 купить**, ознакомьтесь с условиями политики пользователя и конфиденциальности > **создать**.

    **Идет отправка развертывания для сервера отчетов Power BI** процесс может занять несколько минут.

## <a name="connect-to-your-virtual-machine"></a>Подключение к виртуальной машине

1. В области навигации Azure слева выберите **Виртуальные машины**. 

2. В поле **Filter by name** (Фильтрация по имени) введите "report" (отчет). 

3. Выберите виртуальную машину с именем **REPORTSERVERVM**.

    ![Просмотр данных виртуальной машины](media/tutorial-explore-report-server-web-portal/power-bi-report-server-view-virtual-machine.png)

4. Для виртуальной машины REPORTSERVERVM выберите действие **Подключиться**.

    ![Подключение к виртуальной машине](media/tutorial-explore-report-server-web-portal/power-bi-report-server-connect-to-virtual-machine.png)

5. В **подключиться к виртуальной машине** области оставить значения по умолчанию и выберите **загрузить RDP-файл**.

1. В **удаленный рабочий стол** выберите **Connect**.

6. Введите имя и пароль, которые вы назначили для этой виртуальной машины и щелкните **ОК**.

7. Говорит следующее окно **подлинность удаленного компьютера не удается определить**. Нажмите кнопку **ОК**.

   Готово! Открывается виртуальная машина.

## <a name="power-bi-report-server-on-the-vm"></a>Сервер отчетов Power BI на виртуальной машине

Открыв удаленный рабочий стол виртуальной машины, вы увидите указанные ниже элементы.

![Запуск виртуальной машины для Сервера отчетов Power BI](media/tutorial-explore-report-server-web-portal/power-bi-report-server-vm-5-numbers.png)

|Число  |Назначение элемента  |
|---------|---------|
|![Номер 1](media/tutorial-explore-report-server-web-portal/number-1.png) | Примеры отчетов Power BI (PBIX) |
|![Номер 2](media/tutorial-explore-report-server-web-portal/number-2.png) | Ссылки на документацию по Серверу отчетов Power BI |
|![Номер 3](media/tutorial-explore-report-server-web-portal/number-3.png) | Запускает Power BI Desktop, оптимизированного для сервера отчетов Power BI (января 2019 г.) |
|![Номер 4](media/tutorial-explore-report-server-web-portal/number-4.png) | Открытие в браузере веб-портала Сервера отчетов Power BI |
|![Номер 5](media/tutorial-explore-report-server-web-portal/number-5.png) | Запуск SQL Server Data Tools для создания отчета с разбивкой на страницы (RDL) |

Дважды щелкните значок **веб-портала сервера отчетов**. В браузере откроется страница `http://localhost/reports/browse`. На веб-портале отображаются разные файлы, сгруппированные по типам. 

![Веб-портал сервера отчетов Power BI](media/tutorial-explore-report-server-web-portal/power-bi-report-server-browser-in-vm.png)

|Число  |Назначение элемента  |
|---------|---------|
|![Номер 1](media/tutorial-explore-report-server-web-portal/number-1.png) | Ключевые показатели эффективности, созданные на веб-портале |
|![Номер 2](media/tutorial-explore-report-server-web-portal/number-2.png) |  Отчеты Power BI (PBIX)  |
|![Номер 3](media/tutorial-explore-report-server-web-portal/number-3.png) | Мобильные отчеты, созданные в издателе мобильных отчетов для Microsoft SQL Server  |
|![Номер 4](media/tutorial-explore-report-server-web-portal/number-4.png) |  Отчеты с разбивкой на страницы, созданные в построителе отчетов или с помощью SQL Server Data Tools  |
|![Номер 5](media/tutorial-explore-report-server-web-portal/number-5.png) | Книги Excel   | 
|![Номер 6](media/tutorial-explore-report-server-web-portal/number-6.png) | Источники данных для отчетов с разбивкой на страницы | 


## <a name="tag-your-favorites"></a>Маркировка избранных элементов
Вы можете добавлять теги к избранным отчетам и ключевым показателям эффективности. Их проще найти, так как они все собраны в одну папку "Избранное" и на веб-портале, и в мобильных приложениях Power BI. 

1. Щелкните значок многоточия ( **…** ) в правом верхнем углу окна ключевого показателя эффективности **Удельная прибыль**, затем выберите действие **Добавить в избранное**.
   
    ![Добавление в избранное](media/tutorial-explore-report-server-web-portal/power-bi-report-server-add-to-favorites.png)
2. На ленте веб-портала выберите вкладку **Избранное** — в списке появится только что добавленный элемент.
   
    ![Просмотр избранного](media/tutorial-explore-report-server-web-portal/power-bi-report-server-favorites.png)

3. Выберите **Обзор**, чтобы вернуться к веб-порталу.
   
## <a name="view-items-in-list-view"></a>Просмотр элементов в представлении списка
По умолчанию веб-портал отображает содержимое в виде плиток.

Вы можете поменять представление на список, в котором можно легко перемещать или удалять несколько элементов одновременно. 

1. Выберите **Плитки** > **Список**.
   
    ![Переключение представлений](media/tutorial-explore-report-server-web-portal/report-server-web-portal-list-view.png)

2. Вернитесь к представлению плиток, последовательно выбрав **Список** > **Плитки**.

## <a name="power-bi-reports"></a>Отчеты Power BI

На веб-портале вы можете просматривать отчеты Power BI и работать с ними, а также запустить приложение Power BI Desktop.

### <a name="view-power-bi-reports"></a>Просмотр отчетов Power BI

1. На веб-портале в разделе **Отчеты Power BI** выберите **Sample Customer Overview Report** (Пример отчета с общими сведениями о клиентах). Выбранный отчет откроется в окне браузера.

1. Выберите в схеме дерева блок "США", чтобы проверить выделение связанных значений в других визуальных элементах.

    ![Выделенный отчет Power BI](media/tutorial-explore-report-server-web-portal/power-bi-report-server-power-bi.png)

### <a name="edit-in-power-bi-desktop"></a>Редактирование в Power BI Desktop

1. Выберите **Edit in Power BI Desktop** (Редактирование в Power BI Desktop).

1. Выберите **Разрешить**, чтобы этот сайт получил возможность открывать программу на локальном компьютере. 

     В Power BI Desktop откроется отчет. Запишите имя на верхней панели, «Power BI Desktop (января 2019 г.)». Это версия, оптимизированная для Сервера отчетов Power BI.

    Используйте версию Power BI Desktop, установленную в виртуальной машине. Невозможно перейти в другой домен для отправки отчета.

3. На панели полей разверните таблицу Customers (Клиенты) и перетащите из нее поле Occupation (Род занятий) в фильтры уровня отчетов.

    ![Перетаскивание поля в панель фильтров](media/tutorial-explore-report-server-web-portal/power-bi-report-server-desktop-filter.png)

1. Сохраните отчет.

1. Вернитесь к отчету, открытому в браузере, и щелкните значок **Обновить** в интерфейсе браузера.

    ![Значок обновления браузера](media/tutorial-explore-report-server-web-portal/power-bi-report-server-browser-refresh.png)

8. Разверните панель **Фильтры** справа, чтобы увидеть добавленный фильтр **Occupation** (Род занятий). Выберите **Professional** (Профессиональный).

    ![Отфильтрованный отчет Power BI](media/tutorial-explore-report-server-web-portal/power-bi-report-server-power-bi-filtered.png)

3. Выберите **Обзор**, чтобы вернуться к веб-порталу.

## <a name="paginated-rdl-reports"></a>Отчеты с разбивкой на страницы (RDL)

На веб-портале вы можете просматривать отчеты с разбивкой на страницы и управлять ими, а также запускать построитель отчетов.

### <a name="manage-a-paginated-report"></a>Управление отчетом с разбивкой на страницы

1. На веб-портале в разделе **Отчеты с разбивкой на страницы** выберите значок многоточия (...) рядом с элементом **Заказ на продажу** > **Управление**.

1. Выберите **Параметры**, затем замените значение по умолчанию в поле **SalesOrderNumber** строкой **SO50689** и выберите  > **Применить**.

   ![Настройка параметров отчета](media/tutorial-explore-report-server-web-portal/power-bi-report-server-set-parameters.png)

3. Выберите **Обзор**, чтобы вернуться к веб-порталу.

### <a name="view-a-paginated-report"></a>Просмотр отчета с разбивкой на страницы

1. Выберите на веб-портале **Заказ на продажу**.
 
3.  Вы увидите ранее настроенный параметр **заказа** со значением **SO50689**. 

    ![Параметр отчета с разбивкой на страницы](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated.png)

    Здесь вы можете изменить этот параметр, а также любые другие параметры, не изменяя значения по умолчанию.

1. Последовательно выберите **Order** **SO48339 (Заказ SO48339)**  > **Просмотр отчета**.

4. Откроется страница 1 из 2. Щелкните стрелку вправо, чтобы открыть вторую страницу. Откроется вторая страница с продолжением таблицы.

    ![Отчет с разбивкой на страницы, страница 2 из 2](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated-2-of-2.png)

5. Выберите **Обзор**, чтобы вернуться к веб-порталу.

### <a name="edit-a-paginated-report"></a>Редактирование отчета с разбивкой на страницы

Вы можете изменить отчет с разбивкой на страницы в построителе отчетов, который можно запустить непосредственно из браузера.

1. На веб-портале щелкните значок многоточия (...) рядом с элементом **Заказ на продажу** и выберите  > **Edit in Report Builder** (Изменить в построителе отчетов).

1. Выберите **Разрешить**, чтобы этот сайт получил возможность открывать программу на локальном компьютере.

1. В построителе отчетов в режиме конструктора откроется отчет о заказе на продажу.

    ![Представление конструктора для отчета с разбивкой на страницы](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated-design-view.png)

1. Выберите **Запустить**, чтобы посмотреть отчет.

    ![Предварительный просмотр отчета с разбивкой на страницы](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated-preview.png)

5. Закройте построитель отчетов и вернитесь к окну браузера.

## <a name="view-excel-workbooks"></a>Просмотр книг Excel

Вы можете просматривать книги Excel и работать с ними, используя Excel Online в Сервере отчетов Power BI. 

1. Выберите книгу Excel **Office Liquidation Sale.xlsx**. Возможно, поступит запрос на ввод учетных данных. Выберите в нем **Отменить**. 
    Книга откроется на веб-портале.
1. Выберите срез **Устройство**.

    ![Excel Online на веб-портале](media/tutorial-explore-report-server-web-portal/power-bi-report-server-excel-online.png)

1. Выберите **Обзор**, чтобы вернуться к веб-порталу.

## <a name="clean-up-resources"></a>Очистка ресурсов

Итак, вы завершили работу с нашим руководством. Теперь можно удалить группу ресурсов, виртуальную машину и все связанные с ними ресурсы. 

- Для этого выберите группу ресурсов для виртуальной машины и щелкните **Удалить**.

## <a name="next-steps"></a>Дальнейшие действия

С помощью этого руководства вы создали виртуальную машину с предустановленным Сервером отчетов Power BI. Затем вы применили некоторые функции веб-портала, а также открыли отчет Power BI и отчет с разбивкой на страницы в соответствующих редакторах. На этой виртуальной машине установлены источники данных SQL Server Analysis Services. Вы можете попробовать создать собственные отчеты Power BI и отчеты с разбивкой на страницы с помощью тех же источников данных. 

В следующих руководствах цикла представлены дополнительные сведения о создании отчетов для Сервера отчетов Power BI.

> [!div class="nextstepaction"]
> [Создание отчета Power BI для Сервера отчетов Power BI](./quickstart-create-powerbi-report.md)



