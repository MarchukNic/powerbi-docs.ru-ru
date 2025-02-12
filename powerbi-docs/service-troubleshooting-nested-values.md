---
title: Устранение неполадок со вложенными значениями, возвращаемыми как текст, в службе Power BI
description: Дополнительные сведения об исправлении вложенных значений, преобразуемых в строку при использовании неподходящих параметров конфиденциальности источника данных
author: cpopell
manager: kfile
ms.reviewer: ''
ms.custom: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 6/4/2019
ms.author: gepopell
LocalizationGroup: Reports
ms.openlocfilehash: e30a79796fd4d5538406a85a3297a23b2c09a61a
ms.sourcegitcommit: 81ba3572531cbe95ea0b887b94e91f94050f3129
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2019
ms.locfileid: "66751416"
---
# <a name="troubleshooting-nested-values-returned-as-text-in-power-bi-service"></a>Устранение неполадок со вложенными значениями, возвращаемыми как текст, в службе Power BI

## <a name="cause"></a>Причина

В прошлом имели место случаи, когда отчет нормально обновлялся в Power BI Desktop, однако в службе Power BI возникало сообщение об ошибке "Не удается преобразовать значение [Table] в тип Table". Одна из причин этой ошибки заключается в том, что когда брандмауэр конфиденциальности данных (ссылка?) помещает источник данных в буфер, вложенные нескалярные значения (например, таблицы, записи, списки и функции) автоматически преобразуются в текстовые (например, "[Table]" или "[Record]").

Теперь, когда служба Power BI поддерживает настройку уровней конфиденциальности (или полное отключение этого брандмауэра), таких ошибок можно избежать, [настроив параметры конфиденциальности источника данных](https://powerbi.microsoft.com/en-us/blog/privacy-levels-for-cloud-data-sources/) в службе Power BI с использованием значения, отличного от "Частный".

Начиная и июньского выпуска Power BI, когда брандмауэр помещает вложенную таблицу, запись, список и т. д. в буфер, вместо автоматического преобразования этих значений в текст возникает следующая ошибка: 

`We cannot return a value of type Table in this context`

## <a name="effect-on-loadrefresh"></a>Влияние на загрузку и обновление

Хотя это изменение связано с помещением в буфер брандмауэром, его влияние также распространяется на загрузку и обновление. Чтобы исправить процедуру помещения в буфер брандмауэром, нам также пришлось изменить поведение при загрузке вложенных таблиц, записей и т. д. на модель Power BI и модель данных Excel в Power Query для Excel. Ранее вложенные таблицы, записи и т. д. были бы загружены в виде текстовых значений (таких как "[Table]" или "[Record]"). Теперь они будут рассматриваться как ошибки, что приведет к значению NULL в загружаемой таблице и увеличению счетчика ошибок в загруженных результатах.

Так как эти ошибки возникают только во время загрузки и обновления, они не будут появляться в редакторе Power Query.

### <a name="before"></a>До

- Загрузка/обновление без ошибок
- Загруженная таблица содержит "[Table]", "[Record]" и т. д.
 

### <a name="after"></a>После

- Загрузка/обновление с ошибками
- Загруженная таблица содержит значения NULL (вместо "[Table]", "[Record]" и т. д.)
 

## <a name="resolution"></a>Решение

Вы загружаете столбец, содержащий нескалярные значения (например, таблицы, списки, записи и т. д.)?
Если это так, ошибку можно устранить, удалив этот столбец.
Если не удается удалить столбец, можно реплицировать старое поведение, добавив пользовательский столбец и используя логику, как показано в следующем примере:

`if [MyColumn] is table then "[Table]" else if [MyColumn] is record then "[Record]" else if [MyColumn] is list then "[List]" else if [MyColumn] is function then "[Function]" else [MyColumn]`

Воспроизводится ли проблема в Power BI Desktop, если задать для всех параметров конфиденциальности источника данных значение "Частный"?
Если это так, вы можете устранить ошибку, [настроив для их параметров конфиденциальности источника данных](https://powerbi.microsoft.com/en-us/blog/privacy-levels-for-cloud-data-sources/) в службе Power BI значение, отличное от "Частный".
