---
title: Использование соединителя SAP BW в Power BI Desktop
description: Использование соединителя SAP BW в Power BI Desktop
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: af227d2bcbbba2a27804ec74f14003f54aa89dde
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65514677"
---
# <a name="use-the-sap-bw-connector-in-power-bi-desktop"></a>Использование соединителя SAP BW в Power BI Desktop
С помощью Power BI Desktop вы можете получить доступ к данным **SAP Business Warehouse (BW)** .

Сведения о том, какие преимущества могут получить клиенты SAP, подключив Power BI к своим системам SAP Business Warehouse (BW), см. в [этом документе](https://aka.ms/powerbiandsapbw). Сведения об использовании DirectQuery с SAP BW см. в статье [DirectQuery и SAP Business Warehouse (BW)](desktop-directquery-sap-bw.md).

Начиная с выпуска **Power BI Desktop** за июнь 2018 года (и с выхода его общедоступной версии в октябре 2018 года) вы можете использовать соединитель SAP BW, в котором реализованы значительные улучшения в плане производительности и возможностей. Эта обновленная версия SAP BW была разработана корпорацией Майкрософт и называется **реализация 2.0**. Вы можете выбрать **соединитель SAP BW** версии 1 (v1) или **реализацию 2.0 соединителя SAP**. В следующих разделах по очереди описывается установка каждой версии. При подключении к SAP BW из Power BI Desktop можно выбрать один из соединителей.

Мы рекомендуем по возможности использовать **реализацию 2.0 соединителя SAP**.

## <a name="installation-of-version-1-of-the-sap-bw-connector"></a>Установка соединителя SAP BW версии 1
Мы рекомендуем по возможности использовать реализацию 2.0 соединителя SAP (см. инструкции в следующем разделе). В этом разделе описывается установка **соединителя SAP BW** версии 1, который можно установить, выполнив указанные ниже действия.

1. Установите библиотеку **SAP NetWeaver** на локальном компьютере. Библиотеку **SAP NetWeaver** можно получить у администратора SAP или непосредственно в [Центре скачивания программного обеспечения SAP](https://support.sap.com/swdc). В связи с частым изменением структуры **Центра скачивания программного обеспечения SAP** более конкретные рекомендации по навигации по этому сайту недоступны. Кроме того, библиотека **SAP NetWeaver** обычно входит в пакет установки клиентских средств SAP Client Tools.
   
   Чтобы получить ссылку на скачивание последней версии, введите в строку поиска запрос *SAP Note #1025361* (мы не гарантируем, что это точно поможет ее найти). Убедитесь, что архитектура библиотеки **SAP NetWeaver** (32-или 64-разрядная) соответствует архитектуре установленной у вас версии **Power BI Desktop**, а затем установите все файлы из **пакета SDK для RFC SAP NetWeaver** согласно примечаниям SAP.
2. В диалоговом окне **Получение данных** в категории **База данных** будет указан **Сервер приложений SAP Business Warehouse Application Server** и **Сервер сообщений SAP Business Warehouse**.
   
   ![Параметры получения данных для SAP](media/desktop-sap-bw-connector/sap_bw_2a.png)

## <a name="installation-of-implementation-20-sap-connector"></a>Установка реализации 2.0 соединителя SAP

Для **реализации 2.0** соединителя SAP требуется SAP .NET Connector 3.0. [SAP .NET Connector 3.0 можно скачать](https://support.sap.com/en/product/connectors/msnet.html) с веб-сайта SAP по следующей ссылке:

* [SAP .NET Connector 3.0](https://support.sap.com/en/product/connectors/msnet.html)

Для скачивания требуются действительные учетные данные S-пользователя. Клиентам рекомендуется обратиться в свой отдел SAP Basis за получением SAP .NET Connector 3.0. 

Соединитель имеет 32- и 64-разрядную версии. Пользователю *необходимо* выбрать версию, которая соответствует его установке Power BI Desktop. На момент написания этого материала на веб-сайте указаны две версии (для платформы .NET 4.0):

* Соединитель SAP для Microsoft .NET 3.0.20.0 для 32-разрядных (x86) версий Windows в виде ZIP-файла (6,896 КБ), 16 января 2018 г.
* Соединитель SAP для Microsoft .NET 3.0.20.0 для 64-разрядных (x64) версий Windows в виде ZIP-файла (7,180 КБ), 16 января 2018 г.

При установке в окне **Дополнительные этапы установки** необходимо выбрать параметр *Установить сборки в глобальном кэше сборок*, как показано на рисунке ниже.

![Дополнительные этапы установки SAP](media/desktop-sap-bw-connector/sap_bw_2b.png)

> [!NOTE]
> Первая версия реализации SAP BW требовала библиотек DLL Netweaver. Если вы используете реализацию 2.0 соединителя SAP и не используете первую версию, библиотеки DLL Netweaver не нужны.


## <a name="version-1-sap-bw-connector-features"></a>Возможности соединителя SAP BW версии 1
**Соединитель с SAP BW** версии 1 в Power BI Desktop позволяет импортировать данные из кубов **сервера SAP Business Warehouse** или использовать DirectQuery. 

Дополнительные сведения о **соединителе SAP BW** и его использовании с DirectQuery см. в статье [DirectQuery и SAP Business Warehouse (BW)](desktop-directquery-sap-bw.md).

Чтобы установить подключение, нужно указать *сервер*, *номер системы* и *идентификатор клиента*.

![Параметры подключения к серверу SAP](media/desktop-sap-bw-connector/sap_bw_3a.png)

Можно указать еще два **дополнительных параметра**: код языка и пользовательскую инструкцию многомерных выражений для выполнения на указанном сервере.

![дополнительные сведения о подключении](media/desktop-sap-bw-connector/sap_bw_4a.png)

Если указана инструкция многомерных выражений, появится окно **Навигатор**, в котором отображается список кубов, доступных на сервере, с возможностью детализации и выбора элементов из доступных кубов, включая измерения и меры. Power BI предоставляет запросы и кубы, предоставляемые [OLAP BAPI интерфейса открытого анализа BW](https://help.sap.com/saphelp_nw70/helpdata/en/d9/ed8c3c59021315e10000000a114084/content.htm).

После выбора одного или нескольких элементов на сервере создается выходная таблица для предварительного просмотра, которая определяется выбранными элементами.

![Предварительный просмотр таблицы SAP](media/desktop-sap-bw-connector/sap_bw_5.png)

В окне **Навигатор** также представлено несколько **параметров отображения**, которые позволяют делать следующее.

* **Параметры отображения *Только выбранные элементы* и *Все элементы* (представление по умолчанию):** эти параметры полезны для проверки окончательного набора выбранных элементов. В качестве альтернативы для просмотра можно выбрать *имена столбцов* в области *предварительного просмотра*.
* **Включить предварительный просмотр данных (по умолчанию):** в этом диалоговом окне можно включить или отключить предварительный просмотр данных. Отключение предварительного просмотра данных уменьшает количество вызовов к серверу, так как он больше не запрашивает данные для предварительного просмотра.
* **Технические имена:** SAP BW поддерживает наличие *технических имен* для объектов в кубе. Использование технических имен позволяет владельцу куба отображать *понятные* имена объектов куба, а не *физические имена* этих объектов в кубе.

![Окно "Навигатор"](media/desktop-sap-bw-connector/sap_bw_6.png)

После выбора всех необходимых объектов в окне **Навигатор** можно решить, что делать дальше, нажав одну из следующих кнопок в нижней части окна **Навигатор**.

* Если нажать кнопку **Загрузить**, активируется загрузка всего набора строк для выходной таблицы в модель данных Power BI Desktop, затем осуществляется переход к представлению **Отчет**, где можно начать визуализацию данных. Также вы можете внести дополнительные изменения с помощью представления **Данные** или **Связи**.
* Если нажать кнопку **Изменить**, отобразится **редактор запросов**, в котором можно выполнить дополнительное преобразование данных и фильтрацию, прежде чем весь набор строк будет передан в модель данных Power BI Desktop.

Помните, что кроме импорта данных из кубов **SAP BW**, вы также можете импортировать в Power BI Desktop данные из широкого диапазона других источников данных, а затем объединить их в один отчет. Это делает возможными самые разнообразные сценарии составления отчетов и аналитики на основе данных **SAP BW**.

## <a name="using-implementation-20-sap-bw-connector"></a>Использование реализации 2.0 соединителя с SAP BW

Для использования реализации 2.0 соединителя с SAP BW необходимо создать подключение. Чтобы создать подключение, выполните указанные ниже действия.

1. В окне **Получение данных** выберите **Сервер приложений SAP Business Warehouse Application Server** или **Сервер сообщений SAP Business Warehouse**.

2. Появится диалоговое окно создания подключения, в котором можно выбрать реализацию. При выборе **реализации 2.0** становятся доступны параметры режима выполнения, размера пакета и включения структур характеристик, как показано на рисунке ниже.

    ![Диалоговое окно подключения к SAP](media/desktop-sap-bw-connector/sap_bw_7.png)

3. Нажмите кнопку **ОК**. Дальнейшие действия в окне **Навигатор** аналогичны описанным в предыдущем разделе для соединителя SAP BW версии 1. 

### <a name="new-options-for-implementation-20"></a>Новые параметры для реализации 2.0 

Реализация 2.0 поддерживает следующие параметры:

1. **ExecutionMode** — определяет интерфейс многомерных выражений, используемый для выполнения запросов на сервере. Возможны следующие варианты:

        a. SapBusinessWarehouseExecutionMode.BasXml
        b. SapBusinessWarehouseExecutionMode.BasXmlGzip
        c. SapBusinessWarehouseExecutionMode.DataStream

    Значение по умолчанию для этого параметра — SapBusinessWarehouseExecutionMode.BasXmlGzip.

    Значение *SapBusinessWarehouseExecutionMode.BasXmlGzip* может повысить производительность, если при обработке больших наборов данных возникают длительные задержки.

2. **BatchSize** — задает максимальное число строк, возвращаемое при выполнении инструкции многомерного выражения. При извлечении большого набора данных небольшое число строк будет означать больше обращений к серверу. Увеличение числа строк может повысить производительность, но привести к проблемам с памятью на сервере SAP BW. Значение по умолчанию — 50 000 строк.

3. **EnableStructures** — логическое значение, указывающее, распознаются ли структуры характеристик. По умолчанию этот параметр имеет значение False. Влияет на список объектов, доступных для выбора. Не поддерживается в режиме собственного запроса.

Параметр **ScaleMeasures** в этой реализации является нерекомендуемым. В ней принимается значение *ScaleMeasures = false*, то есть всегда отображаются немасштабированные значения.

### <a name="additional-improvements-for-implementation-20"></a>Дополнительные улучшения в реализации 2.0 

В приведенном ниже маркированном списке описываются некоторые дополнительные улучшения, появившиеся в новой реализации.

* Повышение производительности
* Возможность извлечения нескольких миллионов строк данных и точной настройки с помощью параметра размера пакета.
* Возможность переключения режимов выполнения.
* Поддержка режима сжатия. Он особенно полезен в случае с длительными задержками или большими наборами данных.
* Улучшено обнаружение переменных типа Date.
* (Экспериментальная возможность) Предоставление измерений дат (тип ABAP DATS) и времени (тип ABAP TIMS) в виде значений даты и времени соответственно, а не текстовых значений.
* Улучшенная обработка исключений. Ошибки, происходящие в вызовах BAPI, теперь отображаются.
* Свертывание столбцов в режимах BasXml и BasXmlGzip. Например, если созданный запрос многомерного выражения извлекает 40 столбцов, но в соответствии с текущим выбором требуется только 10, запрос будет передан на сервер для извлечения меньшего набора данных.


### <a name="changing-existing-reports-to-use-implementation-20"></a>Изменение существующих отчетов для использования реализации 2.0 

Изменение существующих отчетов для использования **реализации 2.0** возможно только в режиме импорта и требует выполнения указанных ниже действий вручную.

1. Откройте существующий отчет, на ленте выберите команду **Изменить запросы**, а затем запрос SAP Business Warehouse, который нужно изменить.

2. Щелкните запрос правой кнопкой мыши и выберите пункт **Расширенный редактор**.

3. В окне **Расширенный редактор** измените вызов SapBusinessWarehouse.Cubes следующим образом: 

    а. Определите, содержит ли уже запрос запись параметра, например, как в следующем примере:

    ![фрагмент запроса](media/desktop-sap-bw-connector/sap_bw_9.png)

    б. Если да, добавьте параметр из реализации 2.0 и удалите параметр ScaleMeasures, если он имеется, как показано ниже.

    ![фрагмент запроса](media/desktop-sap-bw-connector/sap_bw_10.png)

    в. Если запрос еще не содержит запись параметров, просто добавьте ее. Например, если запрос имеет следующий вид:

    ![фрагмент запроса](media/desktop-sap-bw-connector/sap_bw_11.png)

    г. Измените его на:

    ![фрагмент запроса](media/desktop-sap-bw-connector/sap_bw_12.png)

4. Мы приложили все усилия, чтобы сделать реализацию 2.0 соединителя SAP BW совместимой с соединителем SAP BW версии 1. Однако могут быть некоторые различия из-за использования разных режимов выполнения многомерных выражений SAP BW. Чтобы устранить несоответствия, попробуйте сменить режим выполнения.

## <a name="troubleshooting"></a>Устранение неполадок
В этом разделе приведены случаи устранения неполадок при работе с соединителем **SAP BW**.

1. Числовые данные из **SAP BW** возвращают точки в качестве десятичных разделителей вместо запятых. Например, 1,000,000 возвращается как 1.000.000.
   
   **SAP BW** возвращает десятичные данные с *,* (запятая) или *.* (точка) в качестве десятичного разделителя. Чтобы указать, какие **SAP BW** следует использовать для десятичного разделителя, драйвер, используемый **Power BI Desktop**, вызывает *BAPI_USER_GET_DETAIL*. Этот вызов возвращает структуру, называемую **DEFAULTS**, которая содержит поле с именем *DCPFM*, в котором хранится *нотация десятичного формата*. Он принимает одно из следующих трех значений:
   
       ‘ ‘ (space) = Decimal point is comma: N.NNN,NN
       'X' = Decimal point is period: N,NNN.NN
       'Y' = Decimal point is N NNN NNN,NN
   
   Клиенты, сообщавшие об этой проблеме, обнаружили, что вызов *BAPI_USER_GET_DETAIL* завершается сбоем для определенного пользователя (пользователь, для которого отображаются неверные данные) и сообщением об ошибке следующего вида:
   
       You are not authorized to display users in group TI:
           <item>
               <TYPE>E</TYPE>
               <ID>01</ID>
               <NUMBER>512</NUMBER>
               <MESSAGE>You are not authorized to display users in group TI</MESSAGE>
               <LOG_NO/>
               <LOG_MSG_NO>000000</LOG_MSG_NO>
               <MESSAGE_V1>TI</MESSAGE_V1>
               <MESSAGE_V2/>
               <MESSAGE_V3/>
               <MESSAGE_V4/>
               <PARAMETER/>
               <ROW>0</ROW>
               <FIELD>BNAME</FIELD>
               <SYSTEM>CLNTPW1400</SYSTEM>
           </item>
   
   Чтобы исправить эту ошибку, пользователи должны запросить у своего администратора SAP предоставить пользователю SAP BW, который используется в Power BI, право на выполнение *BAPI_USER_GET_DETAIL*. Стоит также убедиться, что пользователь задал необходимое значение *DCPFM*, описанное выше в этом решении для устранения неполадок.
   
2. **Возможность использования запросов SAP BEx**
   
   В Power BI Desktop можно выполнять запросы **BEx**, включив определенное свойство, как показано на следующем изображении:
   
   ![](media/desktop-sap-bw-connector/sap_bw_8.png)
   
3. В окне **Навигатор** предварительный просмотр данных недоступен — отображается сообщение об ошибке следующего содержания: *Ссылка на объект не указывает на экземпляр объекта*.
   
   Пользователям SAP нужно получить доступ к определенным модулям функции BAPI для получения метаданных и извлечения данных из SAP BW InfoProvider. К ним относятся:
   * BAPI_MDPROVIDER_GET_CATALOGS
   * BAPI_MDPROVIDER_GET_CUBES
   * BAPI_MDPROVIDER_GET_DIMENSIONS
   * BAPI_MDPROVIDER_GET_HIERARCHYS
   * BAPI_MDPROVIDER_GET_LEVELS
   * BAPI_MDPROVIDER_GET_MEASURES
   * BAPI_MDPROVIDER_GET_MEMBERS
   * BAPI_MDPROVIDER_GET_VARIABLES
   * BAPI_IOBJ_GETDETAIL

   Чтобы решить эту проблему, убедитесь, что у пользователя есть доступ к разным модулям *MDPROVIDER*, включая *BAPI_IOBJ_GETDETAIL*. Для устранения этой или подобных проблем щелкните *Включить трассировку* в окне *Диагностика* в разделе *Параметры* в Power BI Desktop. Включив трассировку, попытайтесь получить данные из SAP BW, и просмотрите файл трассировки для получения дополнительных сведений.

## <a name="sap-bw-connection-support"></a>Поддержка соединений SAP BW

В следующей таблице приводятся сведения о текущей поддержке SAP BW.



|Продукт  |Режим  |Authentication  |Соединитель  |Библиотека SNC  |Поддерживается  |
|---------|---------|---------|---------|---------|---------|
|Power BI Desktop     |Все         | Пользователь и пароль  | Сервер приложений | Н/Д  | Да  |
|Power BI Desktop     |Все         | Windows          | Сервер приложений | sapcrypto + gsskrb5/gx64krb5  | Да  |
|Power BI Desktop     |Все         | Windows через олицетворение | Сервер приложений | sapcrypto + gsskrb5/gx64krb5  | Да  |
|Power BI Desktop     |Все         | Пользователь и пароль        | Сервер сообщений | Н/Д  | Да  |
|Power BI Desktop     |Все         | Windows        | Сервер сообщений | sapcrypto + gsskrb5/gx64krb5  | Да  |
|Power BI Desktop     |Все         | Windows через олицетворение | Сервер сообщений | sapcrypto + gsskrb5/gx64krb5  | Да  |
|Power BI Gateway     |Импорт      | Та же, что и в Power BI Desktop |         |   |   |
|Power BI Gateway     |DirectQuery | Пользователь и пароль        | Сервер приложений | Н/Д  | Да  |
|Power BI Gateway     |DirectQuery | Windows через олицетворение (постоянный пользователь, без единого входа) | Сервер приложений | sapcrypto + gsskrb5/gx64krb5  | Да  |
|Power BI Gateway     |DirectQuery | Параметр "Использовать единый вход (SSO) через Kerberos для запросов DirectQuery" | Сервер приложений | *Только с* gsskrb5 или gx64krb5   | Да  |
|Power BI Gateway     |DirectQuery | Пользователь и пароль        | Сервер сообщений | Н/Д  | Да  |
|Power BI Gateway     |DirectQuery | Windows через олицетворение (постоянный пользователь, без единого входа) | Сервер сообщений | sapcrypto + gsskrb5/gx64krb5  | Да  |
|Power BI Gateway     |DirectQuery | Параметр "Использовать единый вход (SSO) через Kerberos для запросов DirectQuery" | Сервер сообщений | sapcrypto + gsskrb5/gx64krb5  | Нет  |



## <a name="next-steps"></a>Дальнейшие действия
Дополнительные сведения о SAP и DirectQuery см. в следующих статьях:

* [DirectQuery и SAP HANA](desktop-directquery-sap-hana.md)
* [Использование DirectQuery и SAP Business Warehouse (BW)](desktop-directquery-sap-bw.md)
* [Power BI и DirectQuery](desktop-directquery-about.md)
* [Источники данных, поддерживаемые DirectQuery](desktop-directquery-data-sources.md)
* [Технический документ о Power BI и SAP BW](https://aka.ms/powerbiandsapbw)
