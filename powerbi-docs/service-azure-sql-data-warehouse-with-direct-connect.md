---
title: "Хранилище данных SQL Azure с DirectQuery"
description: "Хранилище данных SQL Azure с DirectQuery"
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 08/10/2017
ms.author: asaxton
ms.openlocfilehash: 0f712763f37df60814d93080c9d0149541b8530c
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="azure-sql-data-warehouse-with-directquery"></a>Хранилище данных SQL Azure с DirectQuery
Хранилище данных SQL Azure с DirectQuery позволяет создавать динамические отчеты на основе данных и метрик, которые уже присутствуют в хранилище данных SQL Azure. Если используется DirectQuery, при просмотре данных запросы отправляются обратно в хранилище данных SQL Azure в режиме реального времени. В сочетании с масштабированием хранилища данных SQL это позволяет пользователям за считанные минуты создавать динамические отчеты из терабайтов данных. Кроме того, добавление кнопки **Открыть в Power BI** позволяет пользователям напрямую подключать Power BI к хранилищу данных SQL без необходимости задавать информацию вручную.

При использовании соединителя с хранилищем данных SQL:

* укажите при подключении полное имя сервера (см. дополнительные сведения ниже);
* убедитесь, что настроены правила брандмауэра "Разрешить доступ к службам Azure";
* каждое действие, например выбор столбца или добавление фильтра, отправляет запрос непосредственно в хранилище данных;
* плитки обновляются примерно раз в 15 минут (обновление не требуется планировать),  его можно настроить в разделе дополнительных параметров при подключении;
* функция вопросов и ответов для наборов данных DirectQuery недоступна;
* изменения схемы не извлекаются автоматически.

Эти ограничения и примечания могут быть изменены по мере улучшения службы. Ниже приведены инструкции по подключению.

## <a name="using-the-open-in-power-bi-button"></a>Использование кнопки "Открыть в Power BI"
Самый простой способ перемещения между хранилищем данных SQL и Power BI — с помощью кнопки **Открыть в Power BI** на портале предварительной версии Azure. Эта кнопка позволяет легко начать создание новых панелей мониторинга в Power BI.

1. Чтобы приступить к работе, перейдите в экземпляр хранилища данных SQL на портале предварительной версии Azure. Обратите внимание, что сейчас хранилище данных SQL присутствует на портале предварительной версии Azure в единственном экземпляре.
2. Нажмите кнопку **Открыть в Power BI** .
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/openinpowerbi.png)
3. Если не удается выполнить вход напрямую или у вас нет учетной записи Power BI, необходимо зарегистрироваться.
4. Вы будете перенаправлены на страницу подключения к хранилищу данных SQL; будут использованы регистрационные данные для вашего хранилища данных SQL. Введите свои учетные данные и нажмите кнопку "Подключить" для создания подключения.

## <a name="connecting-through-power-bi"></a>Подключение через Power BI
Хранилище данных SQL также указано на странице получения данных Power BI. 

1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.  
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/getdatabutton.png)
2. В области **Базы данных**выберите **Получить**.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/databases.png)
3. Выберите **Хранилище данных SQL** \> **Подключить**.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/azuresqldatawarehouseconnect.png)
4. Введите данные, необходимые для подключения. На рисунке ниже в разделе **Поиск параметров** показано расположение этих данных на портале Azure.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/servername.png)
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/servernamewithadvanced.png)
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/username.png)
   
   > [!NOTE]
   > Имя пользователя соответствует пользователю, определенному в вашем экземпляре хранилища данных Azure SQL.
   > 
   > 
5. Перейдите к набору данных, щелкнув новую плитку или только что созданный набор данных, указанный звездочкой. Этот набор данных будет иметь имя, совпадающее с именем вашей базы данных.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/dataset2.png)
6. Вы можете просматривать все таблицы и столбцы. При выборе столбца источнику отправляется запрос, при этом динамически создается визуальный элемент. Фильтры также будут переводиться в запросы к хранилищу данных. Эти визуальные элементы можно сохранить в новом отчете и закрепить на панели мониторинга.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/explore3.png)

## <a name="finding-parameter-values"></a>Поиск значений параметров
Полное имя сервера и имя базы данных можно найти на портале предварительной версии Azure. Обратите внимание, что сейчас хранилище данных SQL присутствует на портале предварительной версии Azure в единственном экземпляре.

![](media/service-azure-sql-data-warehouse-with-direct-connect/azureportal.png)

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)  
[Получение данных для Power BI](service-get-data.md)  
[Хранилище данных SQL Azure](https://azure.microsoft.com/en-us/documentation/services/sql-data-warehouse/)  
Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
