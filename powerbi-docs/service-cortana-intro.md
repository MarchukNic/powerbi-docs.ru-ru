---
title: Использование Кортаны для поиска и просмотра отчетов и панелей мониторинга — Power BI
description: Использование Cortana с Power BI позволяет получать ответы от данных. Сейчас Кортана поддерживает отчеты и панели мониторинга.
author: maggiesMSFT
manager: kfile
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/29/2019
ms.author: maggies
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: 6d53ddcfc4121e8937810bd6f734f91cd7a9fa39
ms.sourcegitcommit: 8bf2419b7cb4bf95fc975d07a329b78db5b19f81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66375284"
---
# <a name="find-and-view-your-power-bi-data-with-cortana-for-power-bi"></a>Поиск и просмотр данных Power BI с Cortana для Power BI
Используйте Кортану на устройствах с Windows 10, чтобы мгновенно получать ответы на вопросы вашей организации. Благодаря интеграции с Power BI Кортана может получать важные сведения непосредственно из панелей мониторинга и отчетов Power BI. Для работы вам нужна версия Windows 10 (ноябрь 2015 г.) или более поздняя, Кортана, Power BI и доступ минимум к одному набору данных.

> [!IMPORTANT]
> Интеграция Cortana в Power BI рекомендуется. Начиная с 11 июня, Cortana больше не будет работать для любой панели мониторинга и отчеты.

![Поле поиска Кортаны](media/service-cortana-intro/power-bi-cortana-searchbox.png)

## <a name="preview-the-new-cortana-dashboard-search-experience-for-windows-10"></a>Предварительная версия нового интерфейса Кортаны для поиска *панелей мониторинга* в Windows 10
С недавних пор вы уже можете [использовать Кортану для получения определенных типов страниц отчетов](service-cortana-answer-cards.md). Теперь мы добавили **новую функцию** — возможность получать панели мониторинга. Опробуйте в деле и [отправьте нам свой отзыв в Power BI Ideas](https://ideas.powerbi.com/forums/265200-power-bi). В перспективе *новый интерфейс* Кортаны также будет поддерживать поиск отчетов.  Одно из основных преимуществ нового интерфейса заключается в том, что для его настройки не нужно что-то специально делать, — например, включать Кортану или настраивать Windows 10. Интерфейс уже работает.

> [!NOTE]
> В противном случае см. справочную информацию по [устранению неполадок](service-cortana-troubleshoot.md).
> 
> 

Это решение основывается на механизме [службы "Поиск Azure" корпорации Майкрософт](https://docs.microsoft.com/azure/search/). Служба предоставляет такие дополнительные возможности, как интеллектуальное ранжирование, исправление ошибок и автозаполнение.

Оба интерфейса Кортаны может существовать side-by-side.

## <a name="cortana-for-power-bi-documentation"></a>Документация по Кортане для Power BI
Четыре документа Руководство по настройке и использованию Кортаны для Power BI.

**Статья 1** (эта статья): общие сведения о том, как Кортана и Power BI работают вместе.

**Статья 2.** [Поиск отчетов Power BI: доступа к отчетам Power BI (и базовым наборам данных)](service-cortana-enable.md)

**Статья 3.** [Поиск отчетов Power BI: Создание пользовательской *ответов для кортаны*](service-cortana-answer-cards.md)

**Статья 4**. [Устранение неполадок Кортаны для Power BI](service-cortana-troubleshoot.md).

## <a name="how-cortana-and-power-bi-work-together"></a>О совместной работе Cortana и Power BI
Power BI может быть одним из мест для поиска ответов на вопросы, задаваемые в Кортане. В Power BI Кортана может найти подробные ответы на основе данных из отчетов (которые содержат специальную страницу — *Карта ответа Кортаны*) и панелей мониторинга Power BI.

Когда Кортана находит совпадение, имя панели мониторинга или страницы отчета отображается непосредственно на экране Кортаны. Панель мониторинга или страницу отчета можно открыть в Power BI. Страницы отчета также можно просматривать непосредственно в Кортане — они интерактивные.

![Отображение интерактивной страницы отчета в Кортане](media/service-cortana-intro/power-bi-report-cortana-s.png)

### <a name="cortana-and-dashboards-the-new-experience"></a>Кортана и панели мониторинга (*новый интерфейс*)
Кортана может искать ответы как на ваших панелях мониторинга, так и на тех, к которым вам предоставлен общий доступ. Задавайте Кортане вопросы, используя заголовки, ключевые слова, имена владельцев, рабочих областей, приложений и другие сведения.

Чтобы Кортана могла найти ответ, ваш вопрос должен содержать не менее двух слов. Таким образом, если вы ищете панель мониторинга с именем, состоящим из одного слова (например, "Marketing"), добавьте в вопрос слово "show", "Power BI" или имя владельца панели, например "show Marketing" или "michele hart sample". 

Панель мониторинга с именем, состоящим из нескольких слов, отобразится в результатах поиска Кортаны, если с поисковым запросом совпадают два и более слова в ее названии или одно слово в имени владельца. Для панели мониторинга с именем "Customer Profitability Sample" (Рентабельность клиента — пример): 

* «show me customer» *не* результат панели мониторинга Power BI.   
* «фразы такие как «show me customer profitability», «customer p», «customer s», «profitability sample», «michele hart sample», «show customer profitability sample» и «show me customer p» *сделать* результат Power BI.
* Слово «powerbi» считается одним из двух требуемых слов, поэтому «powerbi sample» *does* результат Power BI. 
  
    ![Окно поиска Кортаны (не менее двух слов)](media/service-cortana-intro/power-bi-cortana-2-words.png)

### <a name="cortana-and-reports"></a>Кортана и отчеты
 Кортана может находить ответы в отчетах со [страницами, разработанными специально для отображения в Кортане](service-cortana-answer-cards.md). Просто задайте вопрос, используя заголовок или ключевые слова, которые есть на одной из этих специальных страниц отчета.  

Базовую технологию для использования отчетов [Power BI Q & A](power-bi-tutorial-q-and-a.md).

Если вы задаете вопрос в Кортане, ответы Power BI поступают со страниц отчетов, предназначенных специально для Кортаны. Кортана определяет возможные ответы в режиме реального времени непосредственно на основе *карт ответов*, уже созданных в Power BI.  Чтобы глубже изучить ответ, откройте полученный результат в Power BI.

> [!NOTE]
> Чтобы Кортана могла искать ответы на вопросы в отчетах Power BI, необходимо [включить этот компонент в службе Power BI и настроить обмен данными между Power BI и Windows](service-cortana-enable.md).  
> 
> 

## <a name="using-cortana-to-get-answers-from-power-bi"></a>Использование Кортаны для получения ответов из Power BI
1. Запустите Кортану. *Открыть* Кортану можно несколькими способами: выбрать значок Кортаны на панели задач (на изображении ниже), использовать голосовые команды или коснуться значка поиска на мобильном устройстве Windows.
   
     ![](media/service-cortana-intro/power-bi-cortana-searchbox.png)
2. Как только Кортана будет готова к работе, введите свой вопрос в ее строке поиска или произнесите его вслух. В Кортане отобразятся доступные результаты. Если в Power BI есть панель мониторинга, соответствующая вашему запросу, она появится в разделе **Лучшее соответствие** или **Power BI**.
   
     ![Панель мониторинга Power BI в результатах поиска Кортаны](media/service-cortana-intro/power-bi-cortana-search-hr.png "Панель мониторинга Power BI в результатах поиска Кортаны")
   
   > [!NOTE]
   > Сейчас функция поддерживается только на английском языке.
   > 
   > 
3. Выберите панель мониторинга, чтобы открыть ее в Cortana.

    ![Выбор панели мониторинга Power BI](media/service-cortana-intro/power-bi-cortana-dashboard.png "Select the Power BI dashboard")

    Можно изменить макет, [изменив *представление телефона* панели мониторинга](service-create-dashboard-mobile-phone-view.md). 

1. Из Кортаны также можно открыть панель мониторинга в службе Power BI или Power BI Mobile. Чтобы открыть панель мониторинга в службе Power BI, выберите **Открыть в Интернете**. 
   
   ![Открытие панели мониторинга из Кортаны](media/service-cortana-intro/power-bi-dashboard-opens.png "Открытие панели мониторинга из Кортаны")   
4. Теперь давайте воспользуемся Кортаной для поиска отчета. См. сведения об [отчетах, содержащих страницу с картой ответа Кортаны](service-cortana-answer-cards.md). В этом примере в отчете с именем "Cortana-New-Stores" есть страница ответов Кортаны с именем "cortana stores" (хранилища кортаны).  
   
     Введите свой вопрос в строке поиска Кортаны или произнесите его вслух. В Кортане отобразятся доступные результаты. Если в Power BI есть страница отчета, соответствующая вашему запросу, она появится в разделе **Лучшее соответствие** или **Power BI**. В этом примере PBIX-файл (и резервная копия), используемый для создания карт ответов, также отобразится в разделе **Документы**.
   
     ![Поиск отчета](media/service-cortana-intro/power-bi-cortana-search3-m.png "Поиск отчета") 
5. Щелкните страницу отчета **Cortana stores** (Хранилища Кортаны), чтобы открыть ее в окне Кортаны.
   
    ![Открытие страницы отчета в Кортане](media/service-cortana-intro/power-bi-report-cortana-opens.png "Открытие страницы отчета в Кортане")   
   
    Помните, что *карта ответа* — это специальный тип страницы отчета Power BI, создаваемой владельцем набора данных.  Дополнительные сведения см. в статье [Создание пользовательской страницы ответов для Кортаны в Power BI](service-cortana-answer-cards.md).
6. Но это еще не все возможности. В Кортане можно взаимодействовать с визуализациями на карте ответов, прямо как в Power BI.
   
   * Например, выберите элемент в одной визуализации для перекрестной фильтрации, чтобы выделить другие визуализации в карте ответов.
     
     ![](media/service-cortana-intro/power-bi-cortana-filtered-new.png)
   * Можно также ввести обычное условие для фильтрации результатов.  Например, введите в качестве условия для фильтрации "Cortana stores for Lindseys" (Хранилища Кортаны для Lindseys). После этого будут отображаться данные только для сети Lindseys.
     
     ![Перекрестная фильтрация в Кортане](media/service-cortana-intro/power-bi-cortana-filtered-2.png "Перекрестная фильтрация в Кортане")
7. Продолжаем изучение. Прокрутите до нижней части окна Кортаны и выберите **Открыть в Power BI**.
   
     ![](media/service-cortana-intro/power-bi-cortana-open-new.png)
8. Страница отчета откроется в Power BI.    
     ![Открытие отчета из Кортаны](media/service-cortana-intro/power-bi-cortana-open2.png "Открытие карты ответа в окне поиска Кортаны")

## <a name="considerations-and-troubleshooting"></a>Рекомендации и устранение неполадок
* Кортана не имеет доступа к картам Кортаны, которые еще не были [включены для Power BI](service-cortana-enable.md).
* По-прежнему не удается настроить Кортану для работы с Power BI?  Ознакомьтесь со сведениями, указанными в статье [Устранение неполадок Кортаны для Power BI](service-cortana-troubleshoot.md).
* Cortana для Power BI пока поддерживает только английский язык.
* Кортана для Power BI доступна только для мобильных устройств Windows.

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI](http://community.powerbi.com/).
Хотите оставить отзыв? [Отправьте отзыв на сайт Power BI Ideas](https://ideas.powerbi.com/forums/265200-power-bi).

## <a name="next-steps"></a>Дальнейшие действия
[Включение Cortana для Power BI](service-cortana-enable.md).

