---
title: Сертифицированные пользовательские визуальные элементы Power BI
description: Требования к пользовательскому визуальному элементу для сертификации и процедура его отправки. А также список уже сертифицированных пользовательских визуальных элементов.
author: sranins
ms.author: rasala
manager: kfile
ms.reviewer: maghan
featuredvideoid: ''
ms.service: powerbi
ms.topic: conceptual
ms.subservice: powerbi-custom-visuals
ms.date: 05/9/2019
ms.openlocfilehash: 8c806f0de021c3857039649876864f47e1fffdb2
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65454558"
---
# <a name="certified-custom-visuals"></a>Сертификация пользовательских визуальных элементов

## <a name="what-are-certified-custom-visuals"></a>Что такое **_сертифицированные_** пользовательские визуальные элементы?

Сертифицированными пользовательскими визуальными элементами называются визуальные элементы из магазина **Marketplace**, которые соответствуют определенным **требованиям к коду** и протестированы и одобрены **командой Microsoft Power BI**. Сертифицированный пользовательский визуальный элемент обеспечивает дополнительные возможности. Например, вы можете [экспортировать его в PowerPoint](consumer/end-user-powerpoint.md) и отображать в сообщениях электронной почты, получаемых при оформлении [подписки на страницы отчета](consumer/end-user-subscribe.md).

**Сертифицированные пользовательские визуальные элементы** используются как [стандартные пользовательские визуальные элементы](power-bi-custom-visuals.md). Сертифицированные пользовательские визуальные элементы можно добавлять в **службу Power BI**, **отчет Power BI Desktop** и просматривать в **Power BI Mobile** и **Power BI Embedded**.

Выполняемые проверки гарантируют, что визуальный элемент не обращается к внешним службам и ресурсам. **Корпорация Майкрософт** *не* является автором сторонних пользовательских визуальных элементов, и мы рекомендуем клиентам обращаться к автору напрямую, чтобы проверить функциональные возможности такого визуального элемента.

Процесс сертификации — необязательный процесс, и разработчики самостоятельно решают, хотят ли они сертифицировать свои визуальные элементы.  

**Несертифицированные пользовательские визуальные элементы** не обязательно являются небезопасными. Некоторые визуальные элементы не проходят сертификацию, так как не соответствуют одному или нескольким [требованиям сертификации](https://docs.microsoft.com/power-bi/power-bi-custom-visuals-certified?#certification-requirements). Например, визуальный элемент может подключаться к внешней службе, такой как визуальные элементы карты, или использовать коммерческие библиотеки.

Вы являетесь веб-разработчиком и заинтересованы в том, чтобы создавать собственные визуальные элементы и добавлять их в  **[Microsoft AppSource](https://appsource.microsoft.com)** ? Чтобы узнать, как это сделать, см. раздел  **[Разработка пользовательского визуального элемента Power BI](developer/custom-visual-develop-tutorial.md)** .

## <a name="removal-of-power-bi-certified-custom-visuals"></a>Удаление сертифицированных пользовательских визуальных элементов Power BI

Корпорация Майкрософт может удалять визуальные элементы из [списка сертифицированных](#list-of-custom-visuals-that-have-been-certified).

## <a name="getting-a-custom-visualcertified"></a>Получение сертификации для пользовательского визуального элемента

### <a name="certification-requirements"></a>Требования к сертификации

Для получения [сертификации](#certified-custom-visuals) для пользовательского визуального элемента убедитесь, что он соответствует следующим требованиям.  

* Элемент утвержден Microsoft AppSource. Пользовательский визуальный элемент должен быть в нашем [магазине](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals).
* Пользовательский визуальный элемент создан с версиями **API версии 2.5** или более поздней версии.
* Репозиторий кода — доступны для просмотра, команда Power BI (экземпляр, исходный код (JavaScript или TypeScript), в читаемом формате доступен для нас через GitHub).

    >[!Note]
    > Предоставлять код для общего доступа в Github не нужно.
* Требования к репозиторий кода:
   * Необходимо включить необходимый минимальный набор файлов:
      * .gitignore
      * capabilities.json
      * pbiviz.json
      * package.json
      * пакет lock.json
      * tsconfig.json
   * Не должна содержать папку node_modules (Добавьте файл .gitingore node_modules)
   * **Установите npm** команды не должен возвращать все ошибки.
   * **npm аудита** команды не должен возвращать все предупреждения с высокой или средний уровень.
   * **пакет pbiviz** команды не должен возвращать все ошибки.
   * Необходимо включить [TSlint от корпорации Майкрософт](https://www.npmjs.com/package/tslint-microsoft-contrib) переопределенный без дополнительной настройки, и эта команда не должен возвращать все lint ошибки.
   * Скомпилированный пакет пользовательского визуального элемента должно соответствовать отправленного пакета (хэш md5 оба файла должны быть равны).
* Требования к исходной код:
   * Визуальный элемент должен поддерживать [визуализации API событий](https://microsoft.github.io/PowerBI-visuals/docs/how-to-guide/rendering-events/).
   * Убедитесь, что выполняется код не произвольных или динамическое (неверный: eval(), небезопасно использовать settimeout(), requestAnimationFrame(), setinterval (некоторые функции участия пользователя), работающей входные данные и данные пользователя).
   * Убедитесь, безопасно обрабатывается DOM (неверный: innerHTML D3.html (< некоторых пользователей/входных данных >), используйте очистки для входных данных и данных пользователя перед его добавлением в модели DOM.
   * Убедитесь, что нет ошибок и исключений javascript в консоли браузера для любых входных данных. Пользователи могут использовать визуального с другим диапазоном непредвиденные данные, поэтому визуальный элемент не должен возвращать ошибку. Можно использовать [данный образец отчета](https://github.com/Microsoft/PowerBI-visuals/raw/gh-pages/assets/reports/large_data.pbix) как проверочный набор данных.

* Если изменяются любые свойства в capabilities.json, убедитесь, что они не нарушают существующие пользовательские отчеты.

* Убедитесь, что визуальный элемент соответствует [визуальных элементов Power BI, касающиеся](https://docs.microsoft.com/en-us/power-bi/developer/guidelines-powerbi-visuals#guidelines-for-power-bi-visuals-with-additional-purchases). **Водяные знаки не разрешены**.

* Используются только открытые, доступные для просмотра компоненты OSS (общедоступные библиотеки JS или TypeScript; исходный код доступен для просмотра и не содержит известных уязвимостей). Мы не можем проверить пользовательский визуальный элемент, использующий коммерческие компоненты.

* Отсутствует доступ к внешним службам и ресурсам, в том числе запросы HTTP/S или WebSocket не выходят за пределы Power BI и не обращаются к службам. 

> [!TIP]
> Мы рекомендуем использовать EsLint с набором правил безопасности по умолчанию для предварительной проверки кода перед отправкой.

## <a name="process-for-submitting-a-custom-visual-for-certification"></a>Порядок отправки пользовательских визуальных элементов для сертификации

Чтобы отправить пользовательский визуальный элемент для сертификации, сделайте следующее.

1. Отправьте сообщение электронной почты в службу поддержки пользовательских визуальных элементов Power BI (pbicvsupport@microsoft.com). В сообщение электронной почты включите следующие сведения.
    * Заголовок: запрос сертификации визуального элемента
    * Ссылка на репозиторий GitHub, где размещается исходный код в читаемом формате
    * [Подтверждение соответствия требованиям](#certification-requirements)
    * Подтверждение прохождения проверки кода

2. Рабочая группа по пользовательским визуальным элементам корпорации Майкрософт уведомит вас о получении сертификации для пользовательского визуального элемента и добавлении его в [список сертифицированных](#list-of-custom-visuals-that-have-been-certified) визуальных элементов или об отклонении запроса сертификации с отчетом о проблемах, которые должны быть исправлены. Разработчик несет ответственность за обеспечение открытого канала взаимодействия с корпорацией Майкрософт и за обновление визуальных элементов, включенных в список сертифицированных, если это необходимо.

## <a name="list-of-custom-visuals-that-have-been-certified"></a>Список пользовательских визуальных элементов, которые прошли сертификацию

| Ссылка на AppSource | Ссылка на видео |
| --- | --- |
| [3AG Systems — линейчатая диаграмма относительного расхождения](https://appsource.microsoft.com/en/product/power-bi-visuals/WA104381912) | |
| [3AG Systems — гистограмма относительного расхождения](https://appsource.microsoft.com/product/power-bi-visuals/WA104381803) | |
| [Изображение расширенного кольцевого графика](https://appsource.microsoft.com/product/power-bi-visuals/WA104381941) | |
| [Расширенная визуализация сети](https://appsource.microsoft.com/product/power-bi-visuals/WA104381942) | |
| [Расширенная визуализация TimeSeries](https://appsource.microsoft.com/product/power-bi-visuals/WA104381943) | |
| [Изображение расширенной смешанной диаграммы](https://appsource.microsoft.com/product/power-bi-visuals/WA104381944) | |
| [Круговая диаграмма с индивидуальным радиусом срезов](https://appsource.microsoft.com/product/power-bi-visuals/WA104380759) | |
| [Календарь Beyondsoft](https://appsource.microsoft.com/product/power-bi-visuals/WA104381096) | |
| [Петлеобразная диаграмма от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380838) | [Видео](https://youtu.be/So5xKMSpVJI) |
| [Диаграмма "Ящик с усами"](https://appsource.microsoft.com/product/power-bi-visuals/WA104380831) | |
| [Диаграмма "ящик с усами" от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381351) | [Видео](https://youtu.be/JoHaFLfhXdo) |
| [Клетчатая диаграмма от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380836) | [Видео](https://youtu.be/hA3DOsvn2xY) |
| [Пузырьковая диаграмма от Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381340) | |
| [Диаграмма с маркерами](https://appsource.microsoft.com/product/power-bi-visuals/WA104380755) | [Видео](https://youtu.be/AOlsFYkfkcw) |
| [Диаграмма с маркерами от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380953) | [Видео](https://youtu.be/mtvUNl9bMjA) |
| [Календарь от Tallan](https://appsource.microsoft.com/product/power-bi-visuals/WA104381146) | |
| [Диаграмма "японские свечи" от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380952) | [Видео](https://youtu.be/nT_18gyRxPo) |
| [Карточки с состояниями от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380967) | |
| [Срез Chiclet](https://appsource.microsoft.com/product/power-bi-visuals/WA104380756) | |
| [Хордовая диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380761) | [Видео](https://youtu.be/AQvd2FhRyCI) |
| [Круговой датчик от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380837) | [Видео](https://youtu.be/9NHXALkBXuY) |
| [Таблица кластеров](https://appsource.microsoft.com/product/power-bi-visuals/WA104380806) | |
| [Цилиндрический датчик от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380874) | [Видео](https://youtu.be/DgdoWi7Gcxo) |
| [Датчик с циферблатом](https://appsource.microsoft.com/product/power-bi-visuals/WA104381184) | |
| [Точечная диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380760) | |
| [Точечная диаграмма от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380949) | [Видео](https://youtu.be/By16pX9KT40) |
| [Детализированная картограмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104381045) | |
| [Детализированная фоновая картограмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104381044) | |
| [Детализированная гистограмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380857) | [Видео](https://youtu.be/lBy2gQQ5YsQ) |
| [Детализированная гистограмма временных данных](https://appsource.microsoft.com/product/power-bi-visuals/WA104380881) | [Видео](https://youtu.be/T_mRou18vx0) |
| [Детализированная кольцевая диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380858) | [Видео](https://youtu.be/AUVFrSHmPeo) |
| [Dual KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104380774) | |
| [Динамическая подсказка от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380983) | [Видео](https://youtu.be/Z-tl97BpEr0) |
| [Расширенная точечная диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380762) | [Видео](https://youtu.be/xCfM0cjM4do) |
| [Enlighten Aquarium](https://appsource.microsoft.com/product/power-bi-visuals/WA104381112) | |
| [Enlighten Slicer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380960) | |
| [Enlighten Stack Shuffle](https://appsource.microsoft.com/product/power-bi-visuals/WA104380849) | |
| [Вафельная диаграмма Enlighten](https://appsource.microsoft.com/product/power-bi-visuals/WA104380850) | |
| [Filter by List от Devscope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381413) | [Видео](https://youtu.be/RetEWGwBu0I) |
| [График с направленной силой](https://appsource.microsoft.com/product/power-bi-visuals/WA104380764) | [Видео](https://youtu.be/YsTa7uyJ4sg) |
| [Воронка с источником от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381334) | [Видео](https://youtu.be/R_EcimsLI8U) |
| [Диаграмма Ганта](https://appsource.microsoft.com/product/power-bi-visuals/WA104380765) | [Видео](https://youtu.be/qJ7s_KrGiUU) |
| [Ганта диаграмма от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381364) | [Видео](https://youtu.be/vJLV9JRCpI8) |
| [Гистограммы "Земной шар"](https://appsource.microsoft.com/product/power-bi-visuals/WA104381344) | |
| [Сетка от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380825) | [Видео](https://youtu.be/VOPoDJgZfOY) |
| [Иерархическая диаграмма от Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381333) | [Видео](https://youtu.be/0ZGzJaq_KT4) |
| [Гистограмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380776) | |
| [Гистограмма с точками от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381032) | [Видео](https://youtu.be/-ILF--wExrw) |
| [Горизонтальная воронка от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380846) | [Видео](https://youtu.be/SudZei68PPo) |
| [Изображение от CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381297) | |
| [Сетка изображения](https://appsource.microsoft.com/product/power-bi-visuals/WA104381355) | |
| [Конструктор инфографики](https://appsource.microsoft.com/product/power-bi-visuals/WA104380898) | |
| [Диаграмма с ключевыми показателями эффективности от Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381432) | |
| [Столбец КПЭ от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380996) | [Видео](https://youtu.be/rU0xoOlIq1U) |
| [Сетка ключевых показателей эффективности от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380947) | [Видео](https://youtu.be/dM4PvZh71V0) |
| [Индикатор ключевого показателя эффективности](https://appsource.microsoft.com/product/power-bi-visuals/WA104380832) | |
| [Область КПЭ от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380946) | [Видео](https://youtu.be/cudG4gsZ2V8) |
| [Линейный датчик от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380821) | [Видео](https://youtu.be/7_jFaM30dkc) |
| [Линейно-точечная диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380766) | |
| [Диаграмма Mekko](https://appsource.microsoft.com/product/power-bi-visuals/WA104380785) | [Видео](https://youtu.be/90FLCKpgicA) |
| [Несколько КПЭ](https://appsource.microsoft.com/product/power-bi-visuals/WA104381763) | |
| [Обзор от CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381477) | |
| [Ось воспроизведения (динамический срез)](https://appsource.microsoft.com/product/power-bi-visuals/WA104380981) | |
| [Ключевой показатель эффективности производительности](https://appsource.microsoft.com/product/power-bi-visuals/WA104381083) | [Видео](https://youtu.be/IvfIP3E6-1Q) |
| [Матрица КПЭ производительности](https://appsource.microsoft.com/product/power-bi-visuals/WA104381299) | [Видео](https://youtu.be/1enze8pcGzY) |
| [Диаграмма "Пульс"](https://appsource.microsoft.com/product/power-bi-visuals/WA104381006) | [Видео](https://youtu.be/DQWdcQtjDVw) |
| [Диаграмма с квадрантами от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381011) | [Видео](https://youtu.be/ppBnyhqWNC0) |
| [Лепестковая диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104380771) | |
| [Кольцевая диаграмма от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380824) | [Видео](https://youtu.be/pDToHDFHnq8) |
| [Поворотная диаграмма от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104381007) | [Видео](https://youtu.be/d5xBCMmb3hU) |
| [Диаграмма Sankey](https://appsource.microsoft.com/product/power-bi-visuals/WA104380777) | [Видео](https://youtu.be/WWP9wVUHGaA) |
| [Точечная диаграмма от Akvelon](https://appsource.microsoft.com/product/power-bi-visuals/WA104381703) | |
| [Полоса прокрутки](https://appsource.microsoft.com/product/power-bi-visuals/WA104381018) | |
| [Смарт-фильтр от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380859) | [Видео](https://youtu.be/gcJsDDRQq28) |
| [Спарклайн от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380910) | [Видео](https://youtu.be/0m3Vnvso9tY) |
| [График потока](https://appsource.microsoft.com/product/power-bi-visuals/WA104380772) | |
| [Диаграмма "Солнечные лучи"](https://appsource.microsoft.com/product/power-bi-visuals/WA104380767) | |
| [Synoptic Panel от OKViz](https://appsource.microsoft.com/product/power-bi-visuals/WA104380873) | |
| [Диаграмма "Тепловая карта"](https://appsource.microsoft.com/product/power-bi-visuals/WA104380818) | |
| [Тахометр](https://appsource.microsoft.com/product/power-bi-visuals/WA104380937) | [Видео](https://youtu.be/C3OXdETbS9o) |
| [Фильтрация текста](https://appsource.microsoft.com/product/power-bi-visuals/WA104381309) | |
| [Текстовая оболочка от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380826) | |
| [Thermometer от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380847) | [Видео](https://youtu.be/SPX9mgrAdBc) |
| [Срез Time Brush](https://appsource.microsoft.com/product/power-bi-visuals/WA104380798) | |
| [Срез временной шкалы](https://appsource.microsoft.com/product/power-bi-visuals/WA104380786) | [Видео](https://youtu.be/ozMtZ4_NZ10) |
| [Временная шкала от CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381427) | [Видео](https://youtu.be/szNi9YgXFJc) |
| [Диаграмма-торнадо](https://appsource.microsoft.com/product/power-bi-visuals/WA104380768) | [Видео](https://www.youtube.com/watch?v=AQvd2FhRyCI) |
| [Диаграмма продаж от MAQ Software](https://appsource.microsoft.com/product/power-bi-visuals/WA104380823) | [Видео](https://youtu.be/xhTR6y6J9Ko) |
| [Диаграмма отклонений Ultimate](https://appsource.microsoft.com/product/power-bi-visuals/WA104381140) | [Видео](https://youtu.be/pDYF8iZxERs) |
| [Каскадная диаграмма Ultimate](https://appsource.microsoft.com/product/power-bi-visuals/WA104380956) | [Видео](https://youtu.be/0BZsVCQdEkc) |
| [Список пользователей от CloudScope](https://appsource.microsoft.com/product/power-bi-visuals/WA104381426) | |
| [Вафельная диаграмма](https://appsource.microsoft.com/product/power-bi-visuals/WA104381049) | [Видео](https://youtu.be/1vRqYUsm3Vk) |
| [Облако Word](https://appsource.microsoft.com/product/power-bi-visuals/WA104380752) | [Видео](https://youtu.be/AblTenl9fqo) |

## <a name="faq"></a>ВОПРОСЫ И ОТВЕТЫ

Дополнительные сведения о визуальных элементах см. в разделе [Часто задаваемые вопросы о сертифицированных визуальных элементах](power-bi-custom-visuals-faq.md#certified-custom-visuals).

## <a name="next-steps"></a>Дальнейшие действия

* [Разработка пользовательского визуального элемента Power BI](developer/custom-visual-develop-tutorial.md)
* [Список видео Майкрософт, посвященных пользовательским визуальным элементам, на сайте YouTube](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)  
* [Визуализации в Power BI](visuals/power-bi-report-visualizations.md)  
* [Пользовательские визуализации в Power BI](power-bi-custom-visuals.md)  
* [Публикация настраиваемых визуальных элементов в Microsoft AppSource](developer/office-store.md)  

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
