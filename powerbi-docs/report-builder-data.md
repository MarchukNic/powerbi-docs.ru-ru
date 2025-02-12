---
title: Данные отчета в построителе отчетов Power BI
description: Первым шагом при разработке отчета в построителе отчетов с разбивкой на страницы Power BI является создание источников данных и наборов данных, представляющих базовые данные отчета.
author: maggiesMSFT
ms.author: maggies
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.custom: seodec18
ms.date: 06/06/2019
ms.openlocfilehash: 3c2f6882e9480802d40ff61580ebfda9bbf3b14a
ms.sourcegitcommit: 797bb40f691384cb1b23dd08c1634f672b4a82bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "66840333"
---
# <a name="report-data-in-power-bi-report-builder"></a>Данные отчета в построителе отчетов Power BI

Данные отчета могут поступать из нескольких источников данных в вашей организации. Первым шагом при разработке отчета в построителе отчетов Power BI является создание источников данных и наборов данных, представляющих базовые данные отчета. Каждый источник данных содержит сведения о подключении к данным. Каждый набор данных включает команду запроса, определяющую набор полей для использования в качестве данных из источника данных. Для визуализации данных из каждого набора данных добавьте область данных, например таблицу, матрицу, диаграмму или карту. При обработке отчета запросы выполняются в источнике данных, и каждая область данных расширяются по мере необходимости, чтобы отобразить результаты запроса для набора данных.  

См. сведения о [создании внедренного источника данных для отчетов с разбивкой на страницы в построителе отчетов Power BI](paginated-reports-embedded-data-source.md).


##  <a name="BkMk_ReportDataTerms"></a> Условия  
  
- **Подключение к данным**. Также называется *источником данных*. Подключение к данным включает в себя имя и свойства подключения, которые зависят от типа подключения. По умолчанию подключение к данным не включает учетные данные. Подключение к данным не указывает, какие данные нужно получить из внешнего источника данных. Чтобы сделать это, укажите запрос при создании набора данных.  
  
- **Строка подключения**. Строка подключения — это строковая версия свойств подключения, необходимых для подключения к источнику данных. Свойства подключения различаются в зависимости от типа подключения к данным.  
  
- **Внедренный источник данных**. Также называется *источником данных, зависящим от отчета*. Источник данных, определенный в отчете и используемый только этим отчетом.  
  
- **Учетные данные**. Учетные данные — это сведения для проверки подлинности, которые нужно предоставить для доступа к внешним данным.  
  
##  <a name="BkMk_ReportDataTips"></a> Советы по заданию данных отчета

 Используйте приведенные ниже сведения, чтобы разработать свою стратегию по данным отчета.  
  
- **Фильтрация данных**. Данные отчета можно фильтровать в запросе или отчете. Вы можете использовать наборы данных и переменные запросов, чтобы создать каскадные параметры, а также предоставить пользователю возможность сократить количество вариантов с нескольких тысяч до более приемлемого. Вы можете фильтровать данные в таблице или диаграмме на основе значений параметров или других указанных вами значений.  
  
- **Параметры**. Команды запросов для набора данных, которые включают в себя переменные запроса, автоматически создают соответствующие параметры отчета. Создавать параметры можно и вручную. При просмотре отчета на его панели инструментов отображаются параметры. Пользователи могут выбрать значения для управления данными или внешним видом отчета. Чтобы настроить данные отчета для конкретной аудитории, можно создать наборы параметров отчета с различными значениями по умолчанию, связанные с тем же определением отчета, или использовать встроенное поле **UserID**. 
  
- **Группирование и статистическая обработка данных**. Данные отчета можно группировать и статистически обрабатывать в запросе или отчете. Если вы осуществляете статистическую обработку значений в запросе, можно продолжать комбинировать значения в отчете с учетом ограничений по значимости.  
  
- **Сортировка данных**. Данные отчета можно сортировать в запросе или отчете. В таблицах можно также добавить кнопку интерактивной сортировки, чтобы позволить пользователю управлять порядком сортировки.  
  
- **Данные на основе выражений**. Так как большинство свойств отчета может быть основано на выражениях, а выражения могут включать ссылки на поля набора данных и параметры отчета, вы можете составлять эффективные выражения для управления данными и внешним видом отчета. Можно предоставить пользователю возможность управления отображаемыми данными с помощью определения параметров.  
  
- **Отображение данных из набора данных**. Данные из набора данных обычно отображаются в одной или нескольких областях данных, например таблицах и диаграммах.  
  
- **Отображение данных из нескольких наборов данных**. Вы можете составлять выражения в области данных, которая основана на одном наборе данных, обнаруживающие значения или агрегаты в других наборах данных. Вы можете включить вложенные отчеты в таблицу, основанную на одном наборе данных, чтобы отобразить данные из другого источника.  
  
 Используйте следующий список для определения источников данных для отчета.  
  
- Вам нужно понимать архитектуру слоя данных программного обеспечения для вашей организации и потенциальные проблемы, связанные с типами данных. Вам нужно разбираться, как модули обработки данных и расширения для обработки данных могут повлиять на результаты запроса. Различные источники данных, поставщики данных и данные, хранящиеся в файле определения отчета (RDL), содержат данные разных типов.  
  
- Источники и наборы данных создаются в отчете и публикуются в службе Power BI. После их публикации вы можете настроить учетные данные прямо в службе Power BI или в своем корпоративном шлюзе. 

## <a name="next-steps"></a>Дальнейшие действия

- [Сведения об отчетах с разбивкой на страницы в Power BI Premium](paginated-reports-report-builder-power-bi.md)  
