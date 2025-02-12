---
title: Создание и совместное использование наборов данных (предварительная версия) — Power BI
description: Как владелец набора данных, вы можете создавать наборы данных и делиться ими, чтобы другие пользователи могли работать с ними. Узнайте, как управлять доступом к данным с помощью разрешения на сборку.
author: maggiesMSFT
manager: kfile
ms.reviewer: chbraun
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/31/2019
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: 22339b3d5062c01b3795086eede24ed6a8e7d7e7
ms.sourcegitcommit: 7c426a5209d4fdd1360fc3d0442d57991be1984d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2019
ms.locfileid: "66461771"
---
# <a name="create-and-share-datasets-preview"></a>Создание и совместное использование наборов данных (предварительная версия)

Как автор *моделей данных* в Power BI Desktop, вы можете делиться ими в виде *наборов данных* в службе Power BI. После этого авторы отчетов могут легко находить и повторно использовать наборы данных, которые вы предоставили для общего доступа. Узнайте, как делиться ими и управлять доступом к данным с помощью разрешения на сборку.

## <a name="steps-to-sharing-your-dataset"></a>Процедура по предоставлению набора данных для общего доступа

1. Начните с создания PBIX-файла с моделью данных в Power BI Desktop. Если вы планируете предоставить этот набор данных другим пользователям для создания отчетов, можете даже не проектировать отчет в виде PBIX-файла.

    Рекомендуется сохранить этот PBIX-файл в группе Office 365.

1. Опубликуйте PBIX-файл в [новом интерфейсе рабочей области](service-create-the-new-workspaces.md) в службе Power BI.
    
    Уже после этого другие члены этой рабочей области могут создавать отчеты в других рабочих областях на основе этого набора данных.

1. Теперь вы можете [создать приложение](service-create-distribute-apps.md) в этой рабочей области. При этом на странице **Разрешения** нужно указать разрешения и возможности пользователей.

    > [!NOTE]
    > Если выбрать значение **Вся организация**, никто в организации не будет иметь разрешения на сборку. Это известная проблема. Вместо этого укажите адреса электронной почты в поле **Конкретные лица или группы**.  Если требуется, чтобы разрешения на сборку были у всей организации, укажите псевдоним электронной почты для всей организации.

    ![Задание разрешений для приложений](media/service-datasets-build-permissions/power-bi-dataset-app-permissions.png)

1. Выберите **Публикация приложения** или **Обновить приложение**, если оно уже опубликовано.

## <a name="build-permissions-for-shared-datasets"></a>Разрешения на сборку для общих наборов данных

Тип разрешений на сборку актуален только для наборов данных. С его помощью пользователи могут создавать содержимое на базе набора данных, например отчеты, панели мониторинга, закрепленные плитки из функции "Вопросы и ответы" и обнаружение ценных сведений. Кроме того, они могут создать содержимое на основе набора данных за пределами Power BI, например на листах Excel, с помощью функции "Анализ в Excel", XMLA и экспорта.

Пользователи получают разрешение на сборку по-разному:

- Член рабочей области, в которой находится набор данных, может назначить разрешение для определенных пользователей или групп безопасности в центре разрешений. Нажмите кнопку с многоточием (…) рядом с набором данных и выберите **Управление разрешениями**.

    ![Нажатие кнопки с многоточием](media/service-datasets-build-permissions/power-bi-dataset-manage-permissions.png)

    Открывается центр разрешений для этого набора данных, где можно задать и изменить разрешения.

    ![Центр разрешений](media/service-datasets-build-permissions/power-bi-dataset-permissions.png)

- Администратор или член рабочей области, где находится набор данных, может указать во время публикации, чтобы пользователи с разрешением для приложения также получили разрешение на сборку для базовых наборов данных. Дополнительные сведения см. в разделе [Процедура по предоставлению набора данных для общего доступа](#steps-to-sharing-your-dataset).

- Предположим, у вас есть разрешения на повторное предоставление общего доступа и сборку для набора данных. Делясь отчетом или панелью мониторинга, основанными на этом наборе данных, вы можете указать, что получателям также предоставляется разрешение на сборку для базового набора данных.

    ![Разрешения на сборку](media/service-datasets-build-permissions/power-bi-share-report-allow-users.png)

Вы можете удалить разрешения на сборку для набора данных у пользователей. В этом случае они по-прежнему могут просматривать отчет, созданный на базе общего набора данных, но больше не могут изменять его.

## <a name="more-granular-permissions"></a>Более детализированные разрешения

Разрешение на сборку появилось в Power BI в июне 2019 года и дополняло существующие разрешения на чтение и повторное предоставление общего доступа. Все пользователи, которые на тот момент уже обладали разрешением на чтение для наборов данных посредством разрешений приложения, общего доступа и доступа к рабочей области, также получили разрешение на сборку для тех же наборов данных. Они получили разрешение на сборку автоматически, так как разрешение на чтение уже позволяло им создавать содержимое на основе набора данных с помощью функции "Анализ в Excel" или экспорта.

Благодаря такому более детализированному разрешению на сборку вы можете выбрать, кто может только просматривать содержимое в существующем отчете или существующей панели мониторинга, а кто может создавать содержимое, связанное с базовыми наборами данных.

Если ваш набор данных используется в отчете за пределами его рабочей области, удалить этот набор данных невозможно. Вместо этого отображается сообщение об ошибке.

Вы можете удалить разрешения на сборку. В этом случае пользователи, разрешения которых вы отменили, по-прежнему могут просмотреть отчет, но больше не могут изменить его.

## <a name="track-your-dataset-usage"></a>Отслеживание использования набора данных

При наличии общего набора данных в рабочей области вам может потребоваться узнать, какие отчеты в других рабочих областях основаны на нем.

1. В представлении списка наборов данных выберите **Просмотреть похожие**.

    ![значок просмотра связанных элементов](media/service-datasets-build-permissions/power-bi-dataset-view-related-to-dataset.png)

1. В диалоговом окне **Связанное содержимое** отображаются все связанные элементы. В этом списке отображаются связанные элементы в этой рабочей области и в **других рабочих областях**.
 
    ![Диалоговое окно "Связанное содержимое"](media/service-datasets-build-permissions/power-bi-dataset-related-workspaces.png)

## <a name="next-steps"></a>Дальнейшие действия

- [Использование наборов данных в рабочих областях (предварительная версия)](service-datasets-across-workspaces.md)
- У вас появились вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/)
