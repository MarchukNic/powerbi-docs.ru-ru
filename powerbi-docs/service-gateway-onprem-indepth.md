---
title: "Локальный шлюз данных во всех подробностях"
description: "В этой статье подробно рассматривается локальный шлюз. В ней рассказывается, как служба использует каталог Azure Active Directory и локальный каталог Active Directory при работе с Analysis Services."
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: c030f1b18b654be6bba6a7bf2d10af322567c4d1
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2017
---
# <a name="on-premises-data-gateway-in-depth"></a>Локальный шлюз данных во всех подробностях
Пользователи организации могут обращаться к вашим локальным данным (для доступа к которым они уже прошли проверку подлинности), однако для подключения этих пользователей к локальным источникам данных необходимо установить и настроить локальный шлюз данных. Этот шлюз обеспечивает быстрый и безопасный двусторонний обмен информацией между пользователем в облачной среде и локальным источником данных.

Установка и настройка шлюза обычно выполняются администратором. Для этого могут потребоваться навыки работы с локальными серверами, а также иногда разрешения администратора сервера.

Эта статья не содержит пошаговых инструкций по установке и настройке шлюза. Их можно найти в статье [Локальный шлюз данных](service-gateway-onprem.md). Здесь подробно описаны принципы работы шлюза. Кроме того, статья содержит некоторые сведения об именах пользователей и вопросах безопасности в каталоге Azure Active Directory и в службах Analysis Services, а также о том, как облачная служба использует адрес электронной почты, с которым пользователь входит в нее, шлюз и Active Directory для безопасного подключения и запроса локальных данных.

<!-- Shared Requirements Include -->
[!INCLUDE [gateway-onprem-requirements-include](./includes/gateway-onprem-how-it-works-include.md)]

<!-- Shared Install steps Include -->
[!INCLUDE [gateway-onprem-datasources-include](./includes/gateway-onprem-datasources-include.md)]

## <a name="sign-in-account"></a>Учетная запись для входа
Пользователи будут входить в систему с рабочей или учебной учетной записью. Это учетная запись вашей организации. Если у вас есть подписка на Office 365 и вы не указали свой реальный рабочий адрес электронной почты, ваша учетная запись может иметь вид nancy@contoso.onmicrosoft.com. Ваша учетная запись в облачной службе хранится в клиенте в каталоге Azure Active Directory (AAD). В большинстве случаев имя участника-пользователя учетной записи AAD совпадает с адресом электронной почты.

## <a name="authentication-to-on-premises-data-sources"></a>Проверка подлинности в локальных источниках данных
Для подключения к локальным источникам данных из шлюза (кроме служб Analysis Services) используются сохраненные учетные данные. Шлюз сохраняет и использует их для подключения независимо от того, какой именно пользователь к нему обращается.

## <a name="authentication-to-a-live-analysis-services-data-source"></a>Проверка подлинности на динамическом источнике данных Analysis Services
Каждый раз, когда пользователь взаимодействует со службами Analysis Services, действующее имя пользователя передается в шлюз, а затем на локальный сервер служб Analysis Services. В качестве имени пользователя в Analysis Services передается имя участника-пользователя (как правило, это адрес электронной почты, с которым вы вошли в облачную службу). Для его передачи используется свойство подключения EffectiveUserName. Этот адрес электронной почты должен совпадать с именем участника-пользователя, определенным в локальном домене Active Directory. Имя участника-пользователя является свойством учетной записи Active Directory. Для доступа к серверу соответствующая учетная запись Windows должна присутствовать в роли Analysis Services. Если совпадение в Active Directory не обнаруживается, выполнить вход не удается.

Службы Analysis Services также могут выполнять фильтрацию на основе данной учетной записи. Фильтрация выполняется на уровне роли или на уровне строк.

## <a name="role-based-security"></a>Безопасность на основе ролей
Модели обеспечивают безопасность на основе ролей пользователей. Роли задаются для конкретного проекта модели на этапе разработки в средствах бизнес-аналитики SQL Server Data Tools (SSDT-BI) или после развертывания модели с помощью SQL Server Management Studio (SSMS). Членами ролей могут быть имена пользователей Windows или группы Windows. Роли определяют разрешения, которые имеются у пользователя для выполнения запросов или действий в модели. Большинство пользователей будут принадлежать к роли с разрешениями на чтение. Другие роли предназначены для администраторов и имеют разрешения на обработку элементов, управление функциями базы данных и управление другими ролями.

## <a name="row-level-security"></a>Безопасность на уровне строк
Безопасность на уровне строк — это функция Analysis Services. Модели могут обеспечивать динамическую безопасность на уровне строк. Пользователь должен принадлежать хотя бы к одной роли; в отличие от этого, динамическая безопасность не является обязательной для любой табличной модели. На высоком уровне динамическая безопасность определяет доступ пользователей на чтение данных непосредственно в определенной строке в определенной таблице. Аналогично ролям, динамическая безопасность на уровне строк основывается на имени пользователя Windows.

Возможность пользователя запрашивать и просматривать данные модели определяется в первую очередь ролями, к которым относится его учетная запись пользователя Windows, а во вторую очередь — параметрами динамической безопасности на уровне строк, если они настроены.

Реализация безопасности на основе ролей и динамической безопасности на уровне строк в моделях в этой статье не рассматривается.  Дополнительные сведения см. в статьях [Роли (табличные службы SSAS)](https://msdn.microsoft.com/library/hh213165.aspx) и [Роли безопасности (службы Analysis Services — многомерные данные)](https://msdn.microsoft.com/library/ms174840.aspx) в MSDN. Чтобы максимально полно разобраться в безопасности табличной модели, скачайте и прочтите технический документ [Безопасность в табличной семантической модели бизнес-аналитики](https://msdn.microsoft.com/library/jj127437.aspx).

## <a name="what-about-azure-active-directory"></a>Об Azure Active Directory
В облачных службах Майкрософт для проверки подлинности пользователей применяется каталог [Azure Active Directory](https://azure.microsoft.com/documentation/articles/active-directory-whatis/). Azure Active Directory — это клиент, содержащий имена пользователей и сведения о группах безопасности. Как правило, адрес электронной почты, с которым пользователь выполняет вход, совпадает с именем участника-пользователя учетной записи.

Каковы функции локального каталога Active Directory?

Чтобы службы Analysis Services могли определить, относится ли подключившийся к ним пользователь к роли с разрешениями на чтение данных, сервер должен преобразовать действующее имя пользователя, переданное из AAD в шлюз, а затем на сервер служб Analysis Services. Сервер Analysis Services передает действующее имя пользователя на контроллер домена Windows Active Directory. Затем контроллер домена Active Directory проверяет, является ли действующее имя пользователя действительным именем участника-пользователя в локальной учетной записи, и возвращает его имя пользователя Windows обратно на сервер служб Analysis Services.

Параметр EffectiveUserName нельзя использовать в на сервере Analysis Services, который не присоединен к домену. Чтобы избежать ошибок при входе, локальный сервер Analysis Services должен входить в домен.

## <a name="how-do-i-tell-what-my-upn-is"></a>Как узнать свое имя участника-пользователя?
Вы можете не знать свое имя участника-пользователя и не являться администратором домена. Чтобы узнать имя участника-пользователя для учетной записи, можно использовать следующую команду на рабочей станции.

    whoami /upn

Имя участника-пользователя для локальной учетной записи домена будет похоже на адрес электронной почты. Если вы используете источник данных Analysis Services для динамических подключений, этот параметр должен совпадать со значением, передаваемым в свойстве EffectiveUserName из шлюза.

## <a name="mapping-usernames-for-analysis-services-data-sources"></a>Сопоставление имен пользователей для источников данных Analysis Services
В Power BI можно сопоставлять имена пользователей для источников данных Analysis Services. Вы можете настроить правила сопоставления имени пользователя, выполнившего вход в Power BI, с именем, которое передается в свойстве EffectiveUserName для подключения служб Analysis Services. Это удобный способ в ситуации, когда имя пользователя в AAD не соответствует имени участника-пользователя (UPN) в локальной службе Active Directory. Например, адрес электронной почты nancy@contoso.onmicrsoft.com можно сопоставить с адресом nancy@contoso.com, и это значение будет передано шлюзу. Вы можете ознакомиться с дополнительными сведениями о [сопоставлении имен пользователей](service-gateway-enterprise-manage-ssas.md#map-user-names).

## <a name="synchronize-an-on-premises-active-directory-with-azure-active-directory"></a>Синхронизация локальной Active Directory с Azure Active Directory
Если вы планируете работать с динамическими подключениями Analysis Services, учетные записи в вашем локальном каталоге Active Directory должны соответствовать содержимому Azure Active Directory. В частности, должны совпадать имена участников-пользователей.

Облачным службам известно только об учетных записях, которые хранятся в каталоге Azure Active Directory. Неважно, добавили ли вы соответствующую запись в локальную службу Active Directory: если ее нет в AAD, использовать ее нельзя. Синхронизировать учетные записи в локальном каталоге Active Directory со службой Azure Active Directory можно разными способами.

1. Вы можете вручную добавить учетные записи в Azure Active Directory.
   
   Вы можете создать на портале Azure или портале администрирования Office 365 учетную запись, имя которой будет совпадать с именем участника-пользователя учетной записи в локальном каталоге Active Directory.
2. Вы можете синхронизировать локальные учетные записи со своим клиентом Azure Active Directory с помощью средства [Azure AD Connect](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect/).
   
   Приложение Azure AD Connect позволяет настроить параметры синхронизации каталогов и паролей. Если вы не являетесь администратором клиента или локального домена, для их настройки вам потребуется обратиться к своему ИТ-администратору.
3. Вы можете настроить службы федерации Active Directory (ADFS).
   
   Сервер ADFS можно связать с клиентом AAD с помощью инструмента [Azure AD Connect](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect/). ADFS использует функцию синхронизации каталогов, описанную выше, однако также позволяет реализовать единый вход. Например, находясь в рабочей сети, вы сможете подключаться к облачной службе и входить в нее, не вводя имя пользователя и пароль. Уточните, доступна ли такая возможность для вашей организации, у своего ИТ-администратора.

Приложение Azure AD Connect помогает обеспечить соответствие между именами участников-пользователей в AAD и локальном каталоге Active Directory.

> [!NOTE]
> При синхронизации учетных записей с помощью Azure AD Connect создаются новые учетные записи в клиенте AAD.
> 
> 

## <a name="now-this-is-where-the-gateway-comes-in"></a>Теперь в дело вступает шлюз.
Шлюз выступает в качестве моста между облачной службой и локальным сервером. Передача данных между облаком и шлюзом защищена с помощью [служебной шины Azure](https://azure.microsoft.com/documentation/services/service-bus/). Служебная шина создает защищенный канал обмена информацией между облачной средой и локальным сервером через исходящее подключение на шлюзе.  Вам не потребуется настраивать на своем локальном брандмауэре возможность входящих соединений.

Если у вас есть источник данных Analysis Services, необходимо установить шлюз на компьютере, присоединенном к тому же лесу или домену, что и сервер служб Analysis Services.

Чем ближе шлюз расположен к серверу, тем быстрее работает подключение. Если шлюз находится на том же сервере, что и источник данных, задержка в сети при обмене информацией между сервером и шлюзом будет минимальной.

## <a name="what-to-do-next"></a>Дальнейшие действия
Установив шлюз, вам нужно создать для него источники данных. Источники данных можно добавить в окне **Управление шлюзами**. Дополнительные сведения см. в статьях об управлении источниками данных.

[Управление своим источником данных — службы Analysis Services](service-gateway-enterprise-manage-ssas.md)  
[Управление своим источником данных — SAP HANA](service-gateway-enterprise-manage-sap.md)  
[Управление своим источником данных — SQL Server](service-gateway-enterprise-manage-sql.md)  
[Управление своим источником данных — Oracle](service-gateway-onprem-manage-oracle.md)  
[Управление источником данных — импорт или запланированное обновление](service-gateway-enterprise-manage-scheduled-refresh.md)  

## <a name="where-things-can-go-wrong"></a>Где могут возникнуть проблемы
Иногда установить шлюз не удается. Бывает и такое, что шлюз вроде бы установлен успешно, но служба не может с ним работать. Во многих случаях за этим стоит простая причина (например, неправильный пароль в учетных данных, с помощью которых шлюз подключается к источнику).

В других случаях это может быть вызвано проблемами с типом адреса электронной почты, с которым пользователь выполняет вход, или неспособностью служб Analysis Services разрешить действующее имя пользователя. Если у вас несколько доменов с отношениями доверия между ними и шлюз находится в одном домене, а службы Analysis Services — в другом, это иногда может привести к неполадкам.

Мы не будем касаться темы устранения неполадок шлюза в этой статье. Некоторые инструкции можно найти в статье [Устранение неполадок локального шлюза данных](service-gateway-onprem-tshoot.md). Надеемся, у вас не возникнет затруднений. Но если возникнут, вам поможет понимание того, как все это работает, и статья по устранению неполадок.

<!-- Account and Port information -->
[!INCLUDE [gateway-onprem-accounts-ports-more](./includes/gateway-onprem-accounts-ports-more.md)]

## <a name="next-steps"></a>Дальнейшие действия
[Устранение неполадок локального шлюза данных](service-gateway-onprem-tshoot.md)  
[Служебная шина Azure](https://azure.microsoft.com/documentation/services/service-bus/)  
[Azure AD Connect](https://azure.microsoft.com/documentation/articles/active-directory-aadconnect/)  
Появились дополнительные вопросы? [Ответы на них см. в сообществе Power BI.](http://community.powerbi.com/)
