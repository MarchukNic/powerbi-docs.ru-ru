---
title: Доверенные соединителей независимых производителей в Power BI
description: Уровень доверия со знаком соединитель независимых производителей в Power BI
author: cpopell
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 04/3/2019
ms.author: gepopell
LocalizationGroup: Connect to data
ms.openlocfilehash: 30b7457c6149320c43f24b967a842382821b01b1
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65607793"
---
# <a name="trusting-third-party-connectors"></a>Предоставление доверия сторонних соединителей

## <a name="why-do-you-need-trusted-third-party-connectors"></a>Зачем нужна доверенных соединителей независимых производителей?

В Power BI обычно рекомендуется оставлять «безопасностью данных расширение» уровня на высоком уровне, что предотвращает загрузку кода, не сертифицированные корпорацией Майкрософт. Тем не менее может быть много случаев, в которых вы хотите загрузить специальные соединители — те, которые вы написали или предоставляемые создаваемого консультантом или поставщика за пределами пути сертификации Microsoft.

Разработчик данного соединителя можно подписать его с помощью сертификата и предоставлены сведения, что вам нужно безопасно загружать его без снижения настроек безопасности.

Если вы хотите узнать больше о параметрах безопасности, можно узнать их [здесь](https://docs.microsoft.com/power-bi/desktop-connector-extensibility).

## <a name="using-the-registry-to-trust-third-party-connectors"></a>С помощью реестра доверять сторонних соединителей

Предоставление доверия соединителей независимых производителей в Power BI осуществляется листинг отпечаток сертификата, чтобы доверять в реестре задано значение. Если этот отпечаток совпадает с отпечатком сертификата на соединителе, необходимо загрузить, можно загрузить его в уровень безопасности «Рекомендуется» Power BI. 

Путь реестра является HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Power BI Desktop. Убедитесь, что путь существует, или создайте его. Мы выбрали это расположение, из-за его в первую очередь, управляемых ИТ-политики, а также необходим доступ администрирования локальный компьютер для редактирования. 

![Значение реестра Power BI Desktop, без доверенных сторонних ключей](media/desktop-trusted-third-party-connectors/desktoptrustedthird1.png)

Добавьте новое значение указанного выше. Тип должен быть «Мультистроковый параметр» (REG_MULTI_SZ), и она должна вызываться «TrustedCertificateThumbprints» 

![Power BI Desktop реестра с записью для доверенных соединителей независимых производителей, но нет ключей](media/desktop-trusted-third-party-connectors/desktoptrustedthird2.png)

Добавьте отпечатки сертификатов, как нужно доверять. Можно добавить несколько сертификатов с помощью «\0» как разделитель или в редакторе реестра, справа, нажмите кнопку "->" Изменить и поместить каждый отпечаток в новой строке. Отпечаток пример взят из самозаверяющего сертификата. 

 ![Power BI Desktop реестра с набором доверенных сторонних ключей](media/desktop-trusted-third-party-connectors/desktoptrustedthird3.png)

Если вы правильно следовали инструкциям и был предоставлен правильный отпечаток вашего разработчиком, теперь можно безопасно соединители доверия, подписанных сертификатом связан.

## <a name="how-to-sign-connectors"></a>Как подписывать соединителей

При наличии соединителя вы или разработчику нужно войти, читайте об этом в документации по Power Query [здесь](https://docs.microsoft.com/power-query/handlingconnectorsigning).
