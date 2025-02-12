---
title: Управление версиями в модели данных Power BI
description: Модель данных, предоставленная службой OData
author: rkarlin
ms.author: rkarlin
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 6456974e7c05b65eb084d00bb1970d4291a0cf0c
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61385626"
---
# <a name="data-model-versioning"></a>Управление версиями в модели данных

Модель данных, представленная службой OData, например модель данных Power BI, определяет контракт между службой OData и ее клиентами. Службам разрешено расширить свою модель только в степени, не затрагивающей существующих клиентов. Критические изменения, такие как удаление свойств или изменение их типа, требуют, чтобы новая версия службы была предоставлена по другому корневому URL-адресу службы для новой модели.  
  
Следующие дополнения модели данных считаются безопасными и не требуют от служб управлять версиями точки входа.  
  
* Добавление свойства, которое допускает значение NULL или имеет значение по умолчанию. Если его имя совпадает с именем существующего динамического свойства, у него должен быть тот же тип (или базовый тип), что и у существующего динамического свойства.  
* Добавление свойства навигации, которое допускает значение NULL или является свойством-коллекцией. Если его имя совпадает с именем существующего динамического свойства навигации, у него должен быть тот же тип (или базовый тип), что и у существующего динамического свойства навигации.  
* Добавление нового типа сущности в модель.  
* Добавление нового сложного типа в модель.  
* Добавление нового набора сущностей.  
* Добавление нового одноэлементного класса.  
* Добавление действия, функции, импорт действия или импорт функции.
* Добавление параметра действия, допускающего значение NULL.  
* Добавление определения типа или перечисления.  
* Добавление заметки к элементу модели, которую клиенту не обязательно понимать, чтобы правильно взаимодействовать со службой.  
  
Клиенты ***ДОЛЖНЫ*** быть подготовлены для внесения службами подобных поэтапных изменений в их модель. В частности, клиенты должны быть готовы к получению свойств и производных типов, не ранее определенных службой.  
  
Службы ***НЕ ДОЛЖНЫ*** менять свою модель данных в зависимости от прошедшего аутентификацию пользователя. Если модель данных зависит от пользователя или группы пользователей, все изменения ДОЛЖНЫ быть безопасными (как указано в этом разделе), если сравнивать полную модель и модель, видимую пользователям с ограниченной авторизацией.  
  
Дополнительную информацию о стандартах моделей данных OData см. в разделе [OData версии 4.0, часть 1, "Протокол и корректировочный список 02"](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html).  
  
## <a name="see-also"></a>См. также:
[Обзор интерфейса REST API Power BI](https://docs.microsoft.com/rest/api/power-bi/)  