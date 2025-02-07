---
title: Удаление панелей мониторинга, отчетов, книг, наборов данных и рабочих областей
description: Сведения об удалении содержимого из Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 09/11/2018
ms.author: maggies
LocalizationGroup: Common tasks
ms.openlocfilehash: 087fe859c7b1a8ca732619866d492f143ff413c9
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61157823"
---
# <a name="delete-almost-anything-in-power-bi-service"></a>Удаление содержимого в службе Power BI
В этой статье показано, как удалять панели мониторинга, отчеты, книги, наборы данных, приложения, визуализации и рабочие области в службе Power BI.

## <a name="delete-a-dashboard"></a>Удаление панели мониторинга
Панели мониторинга можно удалять. При удалении панели мониторинга базовый набор данных и отчеты, связанные с этой панелью, не удаляются.

* Если вы являетесь владельцем панели мониторинга, вы можете удалить их. Если вы предоставили доступ к панели мониторинга коллегам, при удалении эта панель будет удалена и из их рабочих областей Power BI.
* Если доступ к информационной панели предоставлен вам и вы больше не хотите работать с ней, удалите панель.  Удаление информационной панели не приводит к ее удалению из рабочих областей Power BI других пользователей.
* Если панель мониторинга является частью [пакета содержимого организации](service-organizational-content-pack-disconnect.md), единственным способом ее удаления является удаление связанного набора данных.

### <a name="to-delete-a-dashboard"></a>Удаление информационной панели
1. В рабочей области перейдите на вкладку **Информационные панели**.
2. Найдите информационную панель, которую необходимо удалить, и щелкните значок удаления ![значок удаления](media/service-delete/power-bi-delete-icon.png).

    ![видео](media/service-delete/power-bi-delete-dash.gif)

## <a name="delete-a-report"></a>Удаление отчета
При удалении отчета не происходит удаление набора данных, являющегося его основой.  Все визуализации, закрепленные из отчета, не затрагиваются — они остаются на информационной панели до тех пор, пока не вы не удалите их по отдельности.

### <a name="to-delete-a-report"></a>Удаление отчета
1. В рабочей области перейдите на вкладку **Отчеты**.
2. Найдите отчет, который необходимо удалить, и щелкните значок удаления   ![значок удаления](media/service-delete/power-bi-delete-icon.png).   

    ![вкладка "Отчеты" рабочей области](media/service-delete/power-bi-delete-reportnew.png)
3. Подтвердите удаление.

   ![Диалоговое окно удаления отчета](media/service-delete/power-bi-delete-report.png)

   > [!NOTE]
   > Если отчет является частью [пакета содержимого](service-organizational-content-pack-introduction.md), его нельзя удалить с помощью этого способа.  Дополнительные сведения см. в статье [Удаление подключения к пакету содержимого организации в Power BI](service-organizational-content-pack-disconnect.md).
   >
   >

## <a name="delete-a-workbook"></a>Удаление книги
Книги можно удалять. Но при удалении книги также удаляются все плитки отчетов и информационных панелей, содержащие данные из этой книги.

Если книга хранится в OneDrive для бизнеса, после ее удаления из Power BI она по прежнему остается в OneDrive.

### <a name="to-delete-a-workbook"></a>Удаление книги
1. В рабочей области перейдите на вкладку **Книги**.
2. Найдите книгу, которую необходимо удалить, и щелкните значок удаления ![значок удаления](media/service-delete/power-bi-delete-report2.png) .

    ![Вкладка "Книги"](media/service-delete/power-bi-delete-workbooknew.png)
3. Подтвердите удаление.

   ![Диалоговое окно удаления книги](media/service-delete/power-bi-delete-confirm.png)

## <a name="delete-a-dataset"></a>Удаление набора данных
Наборы данных можно удалить. Но при удалении набора данных также удаляются все плитки отчетов и панелей мониторинга, содержащие данные из этого набора данных.

Если набор данных входит в состав одного или нескольких [пакетов содержимого организации](service-organizational-content-pack-disconnect.md), единственный способ удалить его из этих пакетов — дождаться завершения его обработки, а потом еще раз попытаться удалить.

### <a name="to-delete-a-dataset"></a>Удаление набора данных
1. В рабочей области перейдите на вкладку **Наборы данных**.
2. Найдите набор данных, который необходимо удалить, и щелкните многоточие (...).  

    ![вкладка "Наборы данных"](media/service-delete/power-bi-delete-datasetnew.png)
3. В раскрывающемся списке выберите **Удалить**.

   ![меню с многоточием](media/service-delete/power-bi-delete-datasetnew2.png)
4. Подтвердите удаление.

   ![Диалоговое окно удаления панели мониторинга](media/service-delete/power-bi-delete-dataset-confirm.png)

## <a name="delete-an-app-workspace"></a>Удаление рабочей области приложения
> [!WARNING]
> При создании рабочей области приложения создается группа Office 365. При удалении рабочей области приложения группа Office 365 также удаляется. Это значит, что группы будут удалены и из других продуктов Office 365, таких как SharePoint и Microsoft Teams.
>
>

Создатель рабочей области приложения может удалить ее. При удалении рабочей области приложения удаляется также связанное приложение всех участников группы. Если вы опубликовали приложение для всей организации, оно также удаляется из AppSource. Удаление рабочей области приложения отличается от выхода из нее.

### <a name="to-delete-an-app-workspace---if-you-are-an-admin"></a>Удаление рабочей области приложения (администратор)
1. На левой панели навигации выберите **Рабочие области**.

    ![Рабочие области приложений](media/service-delete/power-bi-delete-workspace.png)
2. Щелкните многоточие (...) справа от рабочей области, которую необходимо удалить, и выберите **Edit workspace** (Изменить рабочую область).

   ![меню с многоточием > Изменить рабочую область](media/service-delete/power-bi-edit-workspace.png)
3. В окне **Edit workspace** (Изменить рабочую область) выберите **Удалить рабочую область** > **Удалить**.

    ![удаление рабочей области](media/service-delete/power-bi-delete-workspace2.png)

### <a name="to-remove-an-app-workspace-from-your-list"></a>Удаление рабочей области приложения из списка
Если вы больше не хотите входить в рабочую область приложения, из нее можно ***выйти***, после чего она будет удалена из списка. Выход из рабочей области не влияет на других ее участников.  

> [!IMPORTANT]
> Если вы единственный администратор рабочей области приложения, служба Power BI не позволит вам выйти из состава рабочей области.
>
>

1. Войдите в рабочую область, которую требуется удалить.
2. В правом верхнем углу щелкните многоточие (...) и выберите **Leave workspace** (Выйти из рабочей области) > **Выйти**.

      ![выход из рабочей области](media/service-delete/power-bi-leave-workspace.png)

   > [!NOTE]
   > Параметры, доступные в раскрывающемся списке, зависят от того, являетесь ли вы администратором или участником рабочей области приложения.
   >
   >

## <a name="delete-or-remove-an-app"></a>Удаление информационной панели
Приложения можно легко удалить из страницы со списком приложений. Но только администратор может полностью удалить приложение.

### <a name="remove-an-app-from-your-app-list-page"></a>Удаление приложения из страницы со списком приложений
Удаление приложения из страницы со списком приложений не влияет на остальных участников.

1. На левой панели навигации выберите **Приложения**, чтобы открыть страницу со списком приложений.
2. Наведите указатель мыши на название приложения, которое необходимо удалить, и щелкните значок удаления ![](media/service-delete/power-bi-delete-report2.png).

   ![выбор страницы "Приложения"](media/service-delete/power-bi-delete-app.png)

   Если вы случайно удалили приложение, его можно восстановить несколькими способами.  Например, вы можете попросить автора приложения повторно отправить его вам, найти письмо со ссылкой на это приложение, проверить наличие уведомления для приложения в [центре уведомлений](service-notification-center.md) или проверить [AppSource организации](consumer/end-user-apps.md).

## <a name="considerations-and-troubleshooting"></a>Рекомендации и устранение неполадок
В этой статье описаны способы удаления стандартных блоков службы Power BI. Но в Power BI можно удалить и другие элементы:  

* [Удаление основной информационной панели](service-dashboard-featured.md)
* [Удаление информационной панели из избранного](service-dashboard-favorite.md)
* [Удаление страницы из отчета Power BI](service-delete.md)
* [Изменение и удаление плитки на информационной панели](service-dashboard-edit-tile.md)
* [Удаление визуализации в Power BI](service-delete.md)

Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
