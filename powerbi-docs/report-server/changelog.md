---
title: Журнал изменений для сервера отчетов Power BI
description: Этот журнал изменений предназначен для сервера отчетов Power BI и содержит новые элементы, а также исправления ошибок для каждой выпущенной сборки.
ms.author: jaimeta
author: jtarquino
manager: kfile
ms.reviewer: maggies
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 03/31/2018
ms.openlocfilehash: 0aa1d964485297c5e0dae3f4a309cc0dd15b92b2
ms.sourcegitcommit: 90ad0572a92f640684cdc32c9a6478d299de9dc0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2019
ms.locfileid: "68940897"
---
# <a name="changelog-for-power-bi-report-server"></a>Журнал изменений для сервера отчетов Power BI

Этот журнал изменений предназначен для сервера отчетов Power BI и содержит новые элементы, а также исправления ошибок для каждой выпущенной сборки.

Дополнительные сведения о новых возможностях см. в статье [Новые возможности сервера отчетов Power BI](whats-new.md). 

## <a name="may-2019"></a>Май 2019 г.

- **Сервер отчетов Power BI**          
    - *Версия 1.5.7074.36177 (сборка 15.0.1102.371), дата выпуска: 21 мая 2019 г.*
        - Исправленные ошибки
            - Отчеты с разбивкой на страницы
                - Исправление, чтобы всегда включать внедрение шрифтов для PDF.
                - Исправление для задания файлов cookie, отправленных по протоколу HTTPS, как безопасных.
                - Исправление для проблем, связанных с всплывающими окнами из-за ошибок сценария.
                - Исправление для проблем с отображением в мобильном приложении на телефонах с Android
                - Исправление навигатора по времени в мобильном отчете для отображения правильных номеров недель независимо от начала финансового года.
                - Добавлено настраиваемое свойство "RestrictedResourceMimeTypeForUpload", позволяющее администраторам указать запрещенные типы MIME.
         - Функции
            - Добавление поддержки для надежных визуальных элементов в PBIRS.

- **Power BI Desktop (оптимизировано для решения "Сервер отчетов Power BI")** .
    - *Версия: 2.69.5467.1801 (май 2019 г.), дата выпуска: 21 мая 2019 г.*
        - Исправленные ошибки
            - Исправление, позволяющее избежать повторного ввода учетных данных во время отправки PBIX в PBIRS.
            - Исправлено открытие документов с # в имени файла.
            - Добавлена более удобная ссылка для обратного перехода в окно выбора PBIRS.
            - Исправление для режима высокой контрастности в PBIRS для отображения кнопки "Назад" и предупреждающих сообщений для визуальных элементов.
            - Исправления пользовательского интерфейса для области выбора, масштабирования холста.

    - *Версия: 2.69.5467.5201 (май 2019 г.), дата выпуска: 30 июля 2019 г.*
        - Исправленные ошибки
            - Исправление некорректного ведения журнала телеметрии

## <a name="january-2019"></a>Январь 2019 г.

- **Сервер отчетов Power BI**          
    - *Версия 1.4.7024.16477 (сборка 15.0.1102.299), дата выпуска: 28 марта 2019 г.*
        - Исправленные ошибки
            - Отчеты Power BI
                - Исправлена проблема с основными учетными данными при использовании прямых запросов для SAP Hana и SAP BW.
                - Исправлена проблема, из-за которой обновление данных канала OData завершается ошибкой "Не удалось загрузить файл или сборку Microsoft.OData.Core.NetFX35.V7".

- **Сервер отчетов Power BI**            
    - *Версия 1.4.6969.7395 (сборка 15.0.1102.235), дата выпуска: 30 января 2019 г.*
        - Исправленные ошибки
            - Отчеты Power BI
                - Исправлена проблема с основными учетными данными при использовании прямых запросов.
                - Исправлена проблема с двунаправленной связью с применением фильтров безопасности на уровне строк.
                - Исправлена проблема с устаревшими данными после обновления модели при горизонтальном масштабировании среды.
                - Исправлена проблема с двойной полосой прокрутки для таблицы или матрицы в Firefox 63+.
                - Исправлена проблема с размером значка "+/-" в Internet Explorer.
            - Отчеты с разбивкой на страницы
                - Исправлена проблема с обновлением при использовании общего источника данных для отчета.

    - *Версия 1.4.6960.38798 (сборка 15.0.1102.222), дата выпуска: 22 января 2019 г.*
        - Функции
            - Отчеты Power BI 
                - Поддержка безопасности на уровне строк
                - Развертывание и свертывание заголовков строк матрицы
                - Копирование и вставка между PBIX-файлами
                - Интеллектуальные направляющие выравнивания
                - Поддержка соединителя SAP BW 2.0
            - Администраторы
                - Возможность ограничить набор расширений ресурсов, которые могут быть отправлены на сервер отчетов
                - Возможность ограничить поддерживаемые схемы гиперссылок
            - Возможность программирования
                - Новый веб-API: /PowerBIReports({Id})/DataModelRoles (GET).
                - Новый веб-API: /PowerBIReports({Id})/DataModelRoleAssignments (GET & PUT).
                - См. дополнительные сведения о [REST API Сервера отчетов Power BI](https://app.swaggerhub.com/apis/microsoft-rs/PBIRS/2.0).
        - Исправленные ошибки
            - Уязвимость к атакам путем внедрения кода HTML
            - При экспорте в PDF-файл не отображается символ евро
            - Сохранение пароля с несколькими источниками данных в отчетах Power BI делает недействительными не изменявшиеся пароли
            - Визуальные элементы отображаются в мобильном приложении Power BI после периода бездействия

- **Power BI Desktop (оптимизировано для решения "Сервер отчетов Power BI")** .
    - *Версия: 2.65.5313.1562 (январь 2019 г.), дата выпуска: 30 января 2019 г.*
        - Ярлык и закрепленные значки остаются после удаления Сервера отчетов Power BI.
        - Исправлена проблема с закреплением Сервера отчетов Power BI в начальном меню, когда на черном значке отображался черный текст.

    - *Версия: 2.65.5313.1421 (января 2019 г.), выпуск: 22 января 2019 г.* (новая сборка и новая версия)
        - Содержит изменения, необходимые для подключения к серверу отчетов Power BI (январь 2019 г.). 
    - *Версия: 2.65.5313.5141 (январь 2019 г.), дата выпуска: 31 июля 2019 г.* (новая сборка и новая версия)
        - Исправленные ошибки
            - Исправление некорректного ведения журнала телеметрии

## <a name="august-2018"></a>Август 2018 г.

- **Сервер отчетов Power BI**
    - *Версия 1.3.6816.37243 (сборка 15.0.2.557), дата выпуска: 30 августа 2018 г.*
        - Исправленные ошибки
            - Устранена проблема, при которой во время обновления сервера с более ранних версий сервера отчетов PBI перенаправление привязки не обновлялось и клиенты видели такое сообщение:      
            *`
            Failed to load expression host assembly. Details: Could not load file or assembly 'Microsoft.ReportingServices.ProcessingObjectModel, Version=2018.7.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) (rsErrorLoadingExprHostAssembly)
             `*
             
            - Исправлена ошибка прозрачности метки данных.
            
    - *Версия 1.3.6801.38816 (сборка 15.0.2.540), дата выпуска: 15 августа 2018 г.*
        - Функции
            - Теперь для отчетов Power BI доступна поддержка прямых запросов SSO для SAP HANA с Kerberos.
            - В состав выпуска входит API настраиваемых визуальных элементов версии 1.13.0.
            - Для настраиваемых визуальных элементов будет использоваться предыдущая версия, совместимая с текущей версией API сервера (если таковая доступна).

- **Power BI Desktop (оптимизировано для решения "Сервер отчетов Power BI")** .
    - *Версия: 2.61.5192.641 (август 2018 г.), дата выпуска: 15 августа 2018 г.*
        - Содержит изменения, необходимые для подключения к серверу отчетов Power BI (август 2018 г.).         
    - *Версия: 2.61.5192.7701 (август 2018 г.), дата выпуска: 8 августа 2019 г.* (новая сборка и новая версия)
        - Исправленные ошибки
            - Исправление некорректного ведения журнала телеметрии
            
## <a name="march-2018"></a>Март 2018 г.

- **Сервер отчетов Power BI**
    - *Версия 1.2.6690.34729 (сборка 15.0.2.402), дата выпуска: 27 апреля 2018 г.*
        - Исправленные ошибки
            - Включение миграции для каталогов SQL Server Reporting Services 2017.
            - Для отчетов Power BI (PBIX):
                - Отчеты можно обновлять, если на сервере настроена пользовательская аутентификация.
                - При изменении свойств отчета не сбрасываются учетные данные для источника данных.
            - Для отчетов с разбивкой на страницы (RDL):
                - Использование `Lookup()` или производных функций, таких как `LookupSet()` и `MultiLookup()`, в выражениях языка определения отчетов теперь не вызывает `#Error`.
                - В связанных отчетах при печати соблюдается размер страницы, настроенный для целевого отчета.
                - Можно создавать подписки для связанных отчетов, которые используют каскадные параметры.
                - При использовании IE11 можно изменять значения по умолчанию для параметров с несколькими значениями.
                - Можно изменять параметры доставки для управляемой данными подписки.
                - Подписки можно просматривать и редактировать во время выполнения подписки.
                - При настройке учетных данных для источника данных не удаляются строки подключения с выражениями.
            - Для ключевых показателей эффективности:
                - Линии тренда обновляются при обновлении данных.
            - Общее повышение надежности.

    - *Версия 1.2.6660.39920 (сборка 15.0.2.389), дата выпуска: 28 марта 2018 г.*
        - Исправленные ошибки
            - В отчетах Power BI (PBIX-файлы) исправлена проблема с экспортом данных из визуальных элементов Power BI.
            - В отчетах Power BI (PBIX-файлы) исправлена проблема с фильтрами URL-адресов.
            - В отчетах с разбиением на страницы (RDL-файлы) исправлена проблема с неправильным отображением в IE11 после обновления до мартовского выпуска Сервера отчетов Microsoft Power BI.

    - *Версия 1.2.6648.38132 (сборка 15.0.2.378), дата выпуска: 19 марта 2018 г.*
        - Обновления для системы безопасности
        - Улучшение специальных возможностей
        - Исправленные ошибки
            - Для отчетов с разбивкой на страницы (язык определения отчетов) исправлены параметры видимости в связанном отчете, который был возвращен после изменения его свойств
            - Исправлен веб-портал с проверкой подлинности с помощью пользовательских форм, игнорирующий файл cookie для скользящего срока действия.
            - Исправлена функция экспорта в Word, создающая строки неравной высоты при пустом содержимом строки.
            - Для отчетов с разбивкой на страницы (язык определения отчетов) исправлена строка подключения на основе выражений, которая удаляется при изменении учетных данных для источника данных.
            - Исправлена возможность использовать КПЭ с текстовыми значениями.
            - Для отчетов с разбивкой на страницы (язык определения отчетов) восстановлена возможность назначить новый набор данных существующему отчету с разбивкой на страницы (язык определения отчетов).
            - Другие исправления для повышения стабильности и удобства использования.

- **Power BI Desktop (оптимизировано для решения "Сервер отчетов Power BI")** .
    - Версия: 2.56.5023.1043 (март 2018 г.), дата выпуска: 19 марта 2018 г.
        - Содержит изменения, необходимые для подключения к Серверу отчетов Power BI (март 2018 г.).

## <a name="october-2017"></a>Октябрь 2017 г.

- **Сервер отчетов Power BI**
    - *Версия 1.1.6582.41691 (сборка 14.0.600.442), дата выпуска: 10 января 2018 г.*
        - Обновления для системы безопасности
        - Исправленные ошибки
            - Исправлена ошибка, при которой Model.GetParameters возвращает значение 400
            - Исправлена ошибка с назначением общего набора данных существующим отчетам с разбивкой на страницы (RDL)
            - Исправлена ошибка с исключением ExecutionNotFoundException при экспорте отчета с отличающимися значениями параметров в PDF

    - *Версия 1.1.6551.5155 (сборка 14.0.600.438), дата выпуска: 11 декабря 2017 г.*
        - Исправленные ошибки
            - Не удавалось сохранить данные после обновления некоторых отчетов Power BI Desktop.

    - *Версия 1.1.6530.30789 (сборка 14.0.600.437), дата выпуска: 17 ноября 2017 г.*
        - Исправленные ошибки
            - Исправление для сценариев обычной аутентификации. 
            - Исправлена ошибка, при которой нельзя было выбрать дни недели на странице расписания для подписок, планов обновления кэша и моментальных снимков журнала на портале.
            - Для отчетов с разбивкой на страницы (RDL) исправлена ошибка, при которой наличие в текстовом поле выражений со значением false для свойства CanGrow приводило к отсутствию цветов и ненадлежащему отображению шрифтов.
            - Для отчетов Power BI (PBIX) исправлена ошибка, при которой добавление условных обозначений в линейную диаграмму приводило к наличию пустых визуальных элементов.

    - *Версия 1.1.6514.9163 (сборка 14.0.600.434), дата выпуска: 1 октября 2017 г.*
        - Исправленные ошибки
            - Исправлены ошибки ненадежной загрузки для отчетов PBIX размером более 500 МБ.
            - Исправлены ошибки загрузки данных для отчетов PBIX размером более 1 ГБ.

    - *Версия 1.1.6513.3500 (сборка 14.0.600.433), дата выпуска: 31 октября 2017 г.*
        - Функции
            - Поддержка внедренных моделей данных
            - Просмотр книг Excel (с включенной интеграцией Office Online Server)
            - Обновление данных по расписанию (PBIX)
            - Поддержка прямых запросов
            - Поддержка больших файлов (до 2 ГБ)
            - Общедоступный REST API
            - Поддержка общего набора данных в Power BI Desktop (с помощью oData)
            - Поддержка параметров URL-адресов для файлов PBIX
            - Улучшение специальных возможностей

- **Power BI Desktop (оптимизировано для решения "Сервер отчетов Power BI")** .
    - *Версия: 2.51.4885.3981 (октябрь 2017 г.), дата выпуска: 10 апреля 2018 г.*
        - Обновления для системы безопасности

    - *Версия: 2.51.4885.2501 (октябрь 2017 г.), дата выпуска: 10 января 2018 г.*
        - Обновления для системы безопасности

    - *Версия: 2.51.4885.1423 (октябрь 2017 г.), дата выпуска: 17 ноября 2017 г.*
        - Исправленные ошибки
            - Исправлена ошибка, при которой 32-разрядные системы Power BI Desktop не удавалось запустить в ОС x86.
            - Для отчетов Power BI (PBIX) исправлена ошибка отображения линии сетки для оси X.
            - Другие незначительные исправления ошибок

    - *Версия: 2.51.4885.1041 (октябрь 2017 г.), дата выпуска: 31 октября 2017 г.*
        - Функции
            - Содержит изменения, необходимые для подключения к решению "Сервер отчетов Power BI" (октябрь 2017 г.).

## <a name="june-2017"></a>Июнь 2017 г.

- **Сервер отчетов Power BI**
    - *Сборка 14.0.600.309, дата выпуска: 10 января 2018 г.*
        - Обновления для системы безопасности

    - *Сборка 14.0.600.305, дата выпуска: 19 сентября 2017 г.*  
        - Исправленные ошибки
            - Обновление до последней версии [веб-элемента управления Картами Bing](https://msdn.microsoft.com/library/mt712542.aspx)

    - *Сборка 14.0.600.301, дата выпуска: 11 июля 2017 г.*
        - Исправленные ошибки
            - Тег `{{UserId}}` разрешался в сохраненные учетные данные, а не в данные пользователя, выполняющего отчет на сервере отчетов Power BI.
            - Некоторые изображения не обрабатывались в отчетах сервера отчетов Power BI.
            - Имя отчета Power BI невозможно было изменить на сервере отчетов Power BI.
            - Пользовательские визуальные элементы не загружались в мобильном приложении Power BI. Необходимо переустановить мобильное приложение, чтобы очистить локальный кэш.

    - *Сборка 14.0.600.271, дата выпуска: 12 июня 2017 г.*
        - Первоначальный выпуск сервера отчетов Power BI

- **Power BI Desktop (оптимизировано для решения "Сервер отчетов Power BI")** .
    - *Версия: 2.47.4766.4901 (июнь 2017 г.), дата выпуска: 10 января 2018 г.*
        - Обновления для системы безопасности

## <a name="next-steps"></a>Дальнейшие действия

[Что такое Сервер отчетов Power BI?](get-started.md)
[Обзор функций администратора](admin-handbook-overview.md)  
[Установка сервера отчетов Power BI](install-report-server.md)  
[Загрузка построителя отчетов](https://www.microsoft.com/download/details.aspx?id=53613)  
[Download SQL Server Data Tools (SSDT)](http://go.microsoft.com/fwlink/?LinkID=616714) (Скачивание SQL Server Data Tools (SSDT))

Появились дополнительные вопросы? [Попробуйте задать вопрос в сообществе Power BI.](https://community.powerbi.com/)
