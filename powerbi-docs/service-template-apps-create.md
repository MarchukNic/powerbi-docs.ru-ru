---
title: Создание приложений-шаблонов в Power BI (предварительная версия)
description: Сведения о создании приложений-шаблонов, которые можно распространять между любыми клиентами Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/04/2019
ms.author: maggies
ms.openlocfilehash: c08b7e60777b720aa4fc2489b02c212bdd3e7169
ms.sourcegitcommit: 8207c9269363f0945d8d0332b81f1e78dc2414b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "56249813"
---
# <a name="create-a-template-app-in-power-bi-preview"></a>Создание приложения-шаблона в Power BI (предварительная версия)

Новые *приложения-шаблоны* Power BI позволяют партнерам создавать приложения Power BI с минимальным количеством кода или вообще без него и развертывать их для любых клиентов.  В этой статье приводятся пошаговые инструкции по созданию приложения-шаблона Power BI. 

Если вы создаете отчеты и панели мониторинга Power BI, вы можете стать *автором приложений-шаблонов*, который создает и упаковывает в *приложения* различный аналитический контент. Затем готовое приложение можно развернуть в других клиентах Power BI с помощью любой доступной платформы, например AppSource, или используя его в вашей собственной веб-службе. Кроме того, будучи автором, вы можете создавать распространяемый защищенный пакет аналитики. 

Правами пользователей на создание или установку приложений-шаблонов управляют администраторы клиента Power BI. Те, у кого есть соответствующие права, могут устанавливать приложение-шаблон, а затем изменять его и распространять среди пользователей Power BI в своей организации.

## <a name="prerequisites"></a>Предварительные требования 

Ниже приведены требования к созданию приложения-шаблона:  

- [Лицензия Power BI Pro](service-self-service-signup-for-power-bi.md).
- [Установка Power BI Desktop](desktop-get-the-desktop.md) (необязательно).
- Знание [основных принципов Power BI](service-basic-concepts.md).
- Разрешения на создание приложения-шаблона. Дополнительные сведения см. в [разделе "Параметры приложений-шаблонов" статьи о портале администрирования](service-admin-portal.md#template-apps-settings-preview) Power BI.

## <a name="enable-app-developer-mode"></a>Включение режима разработчика приложений

Для создания приложения-шаблона, которое можно распространять в других клиентах Power BI, необходимо активировать режим разработчика приложений. В противном случае вы просто создаете приложение для пользователей Power BI вашей организации.
 
1. Откройте службу Power BI в браузере.
2. Последовательно выберите **Параметры** > **Общие** > **Разработчик** > **Включить режим разработки приложений-шаблонов**.

    ![Включение приложений-шаблонов](media/service-template-apps-create/power-bi-dev-template-app.png)

    Если этот параметр не отображается, попросите у своего администратора Power BI предоставить вам [разрешения для разработки приложений-шаблонов](service-admin-portal.md#template-apps-settings-preview) на портале администрирования.

3. Нажмите кнопку **Применить**.

## <a name="create-the-template-app-workspace"></a>Создание рабочей области приложения-шаблона

Приложение-шаблон, которое можно распространять в других клиентах Power BI, необходимо создать в одной из новых рабочих областей. 
 
1. В службе Power BI выберите **Рабочие области** > **Создать рабочую область приложения**. 
 
    ![Создать рабочую область приложения](media/service-template-apps-create/power-bi-new-workspace.png)

3. На экране **Создание рабочей области приложения** в разделе **Предварительный просмотр улучшенных рабочих областей** щелкните **Попробовать**.

    ![Использование новых рабочих областей](media/service-template-apps-create/power-bi-try-now-new-workspace.png)

5. Введите имя, описание (необязательно) и изображение логотипа (необязательно) для рабочей области приложения.

4. Установите флажок **Разработка приложения-шаблона**.

    ![Разработка приложения-шаблона](media/service-template-apps-create/power-bi-template-app-develop.png)

5. Нажмите кнопку **Сохранить**.

## <a name="create-the-content-in-your-template-app"></a>Создание содержимого в приложении-шаблоне

Как и при использовании обычной рабочей области приложения Power BI, следующим шагом является создание в ней содержимого.  В этой предварительной версии приложений-шаблонов поддерживается только один набор данных, один отчет и одна панель мониторинга.

- [Создайте содержимое Power BI](power-bi-creator-landing.md) в рабочей области приложения.

Если вы используете параметры в Power Query, убедитесь, что они имеют четко определенный тип (например, Text). Типы Any и Binary не поддерживаются. 

Рекомендации по созданию отчетов и панелей мониторинга для приложения-шаблона см. в статье [Советы по созданию приложений-шаблонов в Power BI (предварительная версия)](service-template-apps-tips.md).

## <a name="create-the-test-template-app"></a>Создание тестового приложения-шаблона

Теперь, когда в рабочей области есть содержимое, вы можете упаковать его в приложение-шаблон. Первым шагом является создание тестового приложения-шаблона, доступного только в вашем клиенте организации.

1. В рабочей области приложения-шаблона выберите **Создать приложение**. 

    ![Создание приложения](media/service-template-apps-create/power-bi-create-app.png)
 
    Здесь указываются дополнительные параметры приложения-шаблона в четырех категориях. 

    **Фирменная символика**

    - Имя приложения 
    - Описание
    - Логотип приложения (необязательно)
    - Цвет приложения 

    **Содержимое** 

    - Целевая страница приложения (необязательно): задайте отчет или панель мониторинга в качестве целевой страницы своего приложения.  
    
    **Управление** 

    Здесь можно указать ряд ограничений, которые будут распространяться для пользователей на содержимое приложения. Применяйте это для защиты интеллектуальной собственности, которая может быть в приложении.

    **Доступ**

    - На этапе тестирования решите, какие пользователи в организации могут устанавливать и тестировать приложение.

    Не беспокойтесь — вы всегда можете вернуться и изменить эти параметры позже.  

2. Выберите **Создать приложение**. 

    Появится сообщение, информирующее о готовности тестового приложения и содержащее ссылку, которую можно скопировать и отправить его тестировщикам.

    ![Тестовое приложение готово.](media/service-template-apps-create/power-bi-template-app-test-ready.png)

    Вы также выполнили первый шаг процесса управления выпусками, представленного далее.

    

## <a name="manage-the-template-app-release"></a>Управление выпуском приложения-шаблона

Перед выпуском общедоступной версии приложения-шаблона необходимо убедиться, что оно готово. Power BI создает панель управления выпусками, где можно изучать и контролировать всю процедуру выпуска приложения. Вы также можете активировать переход с одного этапа на другой. Ниже приведены основные этапы. 

- Создание тестового приложения: для тестирования только в вашей организации. 
- Повышение уровня тестового пакета до подготовительного: тестирование за пределами вашей организации.
- Повышение уровня подготовительного пакета до рабочей версии: рабочая версия. 
- Удаление любого пакета или возврат к началу предыдущего этапа. 

Давайте рассмотрим эти этапы.

1. В рабочей области приложения-шаблона щелкните **Управление выпусками**.

    ![Значок "Управление выпусками"](media/service-template-apps-create/power-bi-release-management-icon.png)

2. Выберите **Создать приложение**. 

    Если вы создали тестовое приложение в разделе **Создание тестового приложения-шаблона** выше, рядом с пунктом **Тестирование** уже будет отображаться желтая точка и выбирать здесь **Создать приложение** не нужно. Если все же выбрать этот пункт, вы вернетесь к процессу создания приложения-шаблона.
 
3. Щелкните **Получить ссылку**.

    !["Создать приложение", "Получить ссылку"](media/service-template-apps-create/power-bi-dev-template-create-app-get-link.png)
 
9. Чтобы протестировать процедуру установки приложения, скопируйте ссылку в окне уведомления и вставьте ее в новое окно браузера. 

    Далее вы будете выполнять те же действия, которые будут выполнять ваши клиенты. Изучить процесс с их стороны можно в статье [Установка и распространение приложений-шаблонов в организации](service-template-apps-install-distribute.md).
 
10. В диалоговом окне выберите **Установить**.

    После установки появится уведомление о готовности нового приложения. 
 
11. Выберите **Перейти к приложению**.
 
12. На экране **Начало работы с новым приложением** приложение будет отображаться так, как его увидят ваши клиенты. 

    ![Начало работы с приложением](media/service-template-apps-create/power-bi-template-app-get-started.png)

13. Выберите **Исследовать приложение**, чтобы проверить тестовое приложение с использованием образца данных.

1. Чтобы внести изменения, вернитесь к приложению в исходной рабочей области. Изменяйте тестовое приложение, пока вас не будет все устраивать.

9. Когда вы будете готовы повысить уровень приложения до подготовительного для дальнейшего тестирования вне клиента, вернитесь в область **Управление выпусками** и щелкните **Повысить уровень приложения** рядом с пунктом **Тестирование**.
 
    ![Повышение уровня приложения до предварительного](media/service-template-apps-create/power-bi-template-app-promote.png)

11. Выберите **Повысить уровень**, чтобы подтвердить выбор. 

12. Скопируйте новый URL-адрес для доступа к тестированию приложения вне вашего клиента. Эта ссылка также отправляется в AppSource, чтобы начать распространение приложения.

12. Когда приложение будет готово для использования в рабочей среде или публикации в AppSource, вернитесь в область **Управление выпусками** и щелкните **Повысить уровень приложения** рядом с пунктом **Предварительный этап**.
 
11. Выберите **Повысить уровень**, чтобы подтвердить выбор. 

    Теперь приложение является рабочим и готово к распространению.

    ![Приложение в рабочей среде](media/service-template-apps-create/power-bi-template-app-production.png)

Чтобы сделать приложение общедоступным для тысяч пользователей Power BI, рекомендуем опубликовать его в AppSource. Дополнительные сведения: [Предложение приложения Power BI](https://docs.microsoft.com/azure/marketplace/cloud-partner-portal/power-bi/cpp-power-bi-offer). 

## <a name="update-your-app"></a>Обновление приложения

Теперь, когда приложение доступно в рабочей версии, вы можете вновь запускать этап тестирования, не нарушая работу. 

1. В панели **Управление выпусками** выберите **Создать приложение**.

1. Повторите процедуру создания приложения. 
2. После установки параметров в категориях **Фирменная символика**, **Содержимое**, **Управление** и **Доступ** вновь выберите **Создать приложение**.
3. Нажмите **Закрыть** и вернитесь в **Управление выпусками**. 

    Теперь у вас есть две версии: версия в рабочей среде и новая версия на этапе тестирования. 

    ![Две версии приложения-шаблона](media/service-template-apps-create/power-bi-template-app-2-versions.png)

## <a name="next-steps"></a>Дальнейшие действия

Сведения о том, как с вашим приложением-шаблоном взаимодействуют пользователи, см. в разделе [Установка, настройка и распространение приложений-шаблонов в организации](service-template-apps-install-distribute.md).

Дополнительные сведения о распространении приложения: [Предложение приложения Power BI](https://docs.microsoft.com/azure/marketplace/cloud-partner-portal/power-bi/cpp-power-bi-offer).




