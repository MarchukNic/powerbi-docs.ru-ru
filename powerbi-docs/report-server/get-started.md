---
title: "Начало работы с сервером отчетов Power BI"
description: "Узнайте, как установить сервер отчетов Power BI. "
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
ms.date: 11/01/2017
ms.author: asaxton
ms.openlocfilehash: 86b0c188d2fada9b42e05bf037dc0630a8c75428
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2017
---
# <a name="get-started-with-power-bi-report-server"></a>Начало работы с сервером отчетов Power BI
Создание и развертывание отчетов Power BI, мобильных отчетов и отчетов с разбивкой на страниц, а также управление ими в локальной среде с помощью готовых средств и служб, которые предоставляет сервер отчетов Power BI.

## <a name="create-deploy-and-manage-reports"></a>Создание и развертывание отчетов и управление ими
Сервер отчетов Power BI — это решение, которое клиенты развертывают в локальной среде для создания и публикации отчетов и управления ими, а также доставки отчетов конкретным пользователям разными способами: через браузер, на мобильное устройство или по электронной почте.

Сервер отчетов Power BI предоставляет следующий набор продуктов:

* Современный веб-портал, который можно просматривать в любом современном браузере. На веб-портале можно упорядочивать и отображать отчеты и ключевые индикаторы производительности. Кроме того, на портале можно хранить книги Excel.
* Отчеты Power BI, создаваемые службой Power BI Desktop, которые вы просматриваете на веб-портале или в своей среде.
* Отчеты с разбивкой на страницы — современные отчеты и инструменты для их создания.
* Мобильные отчеты — характеризуются гибким макетом, который позволяет использовать отчеты на разных устройствах и в разной ориентации.

Подробнее об этом читайте ниже.

### <a name="whats-new-in-power-bi-report-server"></a>Новые возможности сервера отчетов Power BI
Из этих источников вы можете узнавать о новых возможностях сервера отчетов Power BI.

* [Новые возможности сервера отчетов Power BI](whats-new.md)
* [Блог Microsoft Power BI](https://powerbi.microsoft.com/blog/)
* [Блог команды разработчиков SQL Server Reporting Services](https://blogs.msdn.microsoft.com/sqlrsteamblog/)
* [Канал YouTube Guy in a Cube](https://aka.ms/guyinacube)

## <a name="web-portal"></a>Веб-портал
![](media/get-started/web-portal.png)

Для перехода на сервер отчетов Power BI используется современный веб-портал, который можно открывать и просматривать в любом современном браузере. На этом портале доступны все отчеты и ключевые показатели эффективности.

На веб-портале можно использовать собственную [фирменную символику](https://docs.microsoft.com/sql/reporting-services/branding-the-web-portal). Можно также создавать ключевые показатели эффективности прямо на веб-портале. Ключевые показатели эффективности могут отображать ключевые метрики вашей компании непосредственно в браузере без необходимости открывать отчет.

Содержимое на веб-портале упорядочено по типу: отчеты Power BI, мобильные отчеты, отчеты с разбивкой на страницы и ключевые показатели эффективности, а также книги Excel, общие наборы данных и общие источники данных для использования в качестве стандартных блоков для отчетов. Вы можете безопасно хранить их и управлять ими здесь, в традиционной иерархии папок. Вы можете отмечать тегами избранное и управлять содержимым, если у вас есть соответствующие права.

Кроме того, вы можете планировать обработку отчетов, получать доступ к отчетам по требованию и подписываться на отчеты, опубликованные на новом веб-портале.

Дополнительные сведения о [веб-портале](https://docs.microsoft.com/sql/reporting-services/web-portal-ssrs-native-mode).

## <a name="power-bi-reports"></a>Отчеты Power BI
![](media/get-started/powerbi-reports.png)

Отчет Power BI — это разностороннее представление набора данных с визуализациями, которые отображают различные результаты и сведения, полученные из этого набора данных.  В отчете может быть одна визуализация или несколько страниц, заполненных визуализациями. В зависимости от назначенной вам роли вы можете создавать или использовать отчеты.

Отчеты формируются на основе одного набора данных. Каждая визуализация в отчете представляет собой фрагмент данных. и не является статической. Работая с данными, вы можете добавить и удалить их, изменить типы визуализации и применить фильтры и срезы (учитывая углубленное изучение данных), чтобы обнаружить дополнительные сведения и получить ответы на вопросы. Как и информационная панель, отчет предоставляет широкие возможности для взаимодействия и настройки, при этом обновление визуализаций происходит при изменении базовых данных.

## <a name="paginated-reports"></a>Отчеты с разбивкой на страницы
![](media/get-started/paginated-reports.png)

Отчеты с разбивкой на страницы — это отчеты в виде документов с разбивкой на страницы. Чем больше у вас данных, тем больше строк в таблицах, а чем больше строк в таблицах, тем больше страниц в отчете. Эти отчеты отлично подходят для создания документов с фиксированным макетом и разрешением, оптимизированных для печати, например файлов в формате PDF и Word.

Для создания этих современных отчетов используется [построитель отчетов](https://docs.microsoft.com/sql/reporting-services/report-builder/report-builder-in-sql-server-2016) или конструктор отчетов в [SQL Server Data Tools (SSDT)](https://docs.microsoft.com/sql/reporting-services/tools/reporting-services-in-sql-server-data-tools-ssdt).

## <a name="report-server-programming-features"></a>Функции программирования сервера отчетов
Воспользуйтесь преимуществами функций программирования сервера отчетов Power BI, которые позволяют расширять и настраивать функциональность отчетов с помощью API-интерфейсов для интеграции или расширения данных и обработки отчетов в пользовательских приложениях.

См. дополнительные сведения в [документации разработчика сервера отчетов](https://docs.microsoft.com/sql/reporting-services/reporting-services-developer-documentation).

## <a name="next-steps"></a>Дальнейшие действия
[Руководство пользователя](user-handbook-overview.md)  
[Руководство администратора](admin-handbook-overview.md)  
[Краткое руководство по установке сервера отчетов Power BI](quickstart-install-report-server.md)  
[Install Report Builder](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder) (Установка построителя отчетов)  
[Download SQL Server Data Tools (SSDT)](http://go.microsoft.com/fwlink/?LinkID=616714) (Скачивание SQL Server Data Tools (SSDT))

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](https://community.powerbi.com/)
