---
title: "Подключение к Prevedere с помощью Power BI"
description: "Prevedere для Power BI"
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: fd9426a8fce0ed1d707184b421a93f989852a33d
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-prevedere-with-power-bi"></a>Подключение к Prevedere с помощью Power BI
Доступ к эксклюзивной и важной финансовой информации для последовательного и оперативного развития бизнеса.

Подключитесь к [пакету содержимого Prevedere](https://app.powerbi.com/getdata/services/prevedere) для Power BI.

>[!NOTE]
>Если вы еще не работали с Prevedere, вы можете испытать этот пакет в действии с помощью [ключа-образца](https://prevederepowerbiconnector.azurewebsites.net/static/learnmore.html).

## <a name="how-to-connect"></a>Способы подключения
1. Нажмите кнопку **Получить данные** в нижней части левой панели навигации.
   
   ![](media/service-connect-to-prevedere/getdata.png)
2. В поле **Службы** выберите **Получить**.
   
   ![](media/service-connect-to-prevedere/services.png)
3. Выберите **Prevedere** и нажмите **Получить**.
   
   ![](media/service-connect-to-prevedere/connect.png)
4. В качестве **метода проверки подлинности** выберите **Ключ** и введите ключ API Prevedere.
   
    ![](media/service-connect-to-prevedere/creds.png)
5. Выберите **Войти**, чтобы начать импорт. После завершения в области навигации появятся новая панель мониторинга, отчет и модель. Выберите панель мониторинга, чтобы просмотреть импортированные данные.
   
     ![](media/service-connect-to-prevedere/dashboard.png)

**Дальнейшие действия**

* Попробуйте [задать вопрос в поле "Вопросы и ответы"](power-bi-q-and-a.md) в верхней части информационной панели.
* [Измените плитки](service-dashboard-edit-tile.md) на информационной панели.
* [Выберите плитку](service-dashboard-tiles.md), чтобы открыть соответствующий отчет.
* Хотя набор данных будет обновляться ежедневно по расписанию, вы можете изменить график обновлений или попытаться выполнять обновления по запросу с помощью кнопки **Обновить сейчас**.

## <a name="whats-included"></a>Содержимое
Пакет содержимого анализирует ваши прогнозы в отношении продаж, модели прогнозирования, индикаторы перспективных клиентов и т. д.

## <a name="system-requirements"></a>Требования к системе
Для работы с этим пакетом содержимого необходим доступ к ключу API Prevedere или ключу-образцу (см. ниже).

## <a name="finding-parameters"></a>Поиск параметров
<a name="FindingParams"></a>

Существующие клиенты могут получить доступ к своим данным с помощью своего ключа API. Если вы еще не являетесь клиентом, вы можете оценить образец данных и пример анализа с помощью [ключа-образца](https://prevederepowerbiconnector.azurewebsites.net/static/learnmore.html).

## <a name="troubleshooting"></a>Устранение неполадок
В зависимости от размера вашего экземпляра загрузка данных может занять некоторое время.

## <a name="next-steps"></a>Дальнейшие действия
[Приступая к работе с Power BI](service-get-started.md)

[Получение данных в Power BI](service-get-data.md)
