---
title: Исправление ошибки "Corporate SSL certificate is untrusted" (Корпоративный SSL-сертификат не является доверенным)
description: При входе в приложение Power BI для Android может появиться сообщение "Не удалось выполнить проверку подлинности, так как SSL-сертификат вашей организации не является доверенным"
.": ''
author: mshenhav
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 05/18/2018
ms.author: mshenhav
ms.openlocfilehash: de103412e21e0d26d20058e2d4e1fb9a8a5449bf
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "61341358"
---
# <a name="fixing-corporate-ssl-certificate-is-untrusted---power-bi"></a>Исправление ошибки "Corporate SSL certificate is untrusted" (Корпоративный SSL-сертификат не является доверенным) в Power BI
При входе в мобильное приложение Microsoft Power BI для Android может появиться сообщение "Не удалось выполнить проверку подлинности, так как SSL-сертификат вашей организации не является доверенным для этого устройства. Обратитесь к ИТ-администратору организации". 

Действия по устранению этой неполадки обычно зависят от операционной системы на устройстве Android, но эта ошибка может быть связана и с другими проблемами.

## <a name="on-android-7-or-later"></a>Android 7 или более поздней версии
Найдите обновление для приложения **Chrome** и установите это обновление.

## <a name="on-android-6-and-earlier"></a>Android 6 и более ранних версий
Возможно, вашему устройству требуется обновленная версия приложения System WebView. Приложение может быть установлено на устройстве — достаточно просто нажать кнопку **обновления**.

Если приложение System WebView не установлено на устройстве, сделайте следующее.

1. Закройте Power BI на устройстве Android.
2. Откройте магазин Google Play и найдите приложение **System WebView** от Google Inc.
3. Установите это приложение.
4. Перезапустите приложение Power BI и войдите в него.

## <a name="time-zone-settings"></a>Настройки часовых поясов
Настройки часовых поясов на вашем устройстве могут быть неправильными. 

Чтобы проверить их, последовательно выберите **Параметры** > **Система** > **Дата и время**.

## <a name="custom-authentication-server"></a>Пользовательский сервер проверки подлинности
Если вы используете пользовательский сервер проверки подлинности, SSL-сертификат на корпоративном сервере проверки подлинности может быть недействительным. Свяжитесь с ИТ-отделом вашей организации, чтобы проверить конфигурацию корпоративного сервера проверки подлинности, следуя инструкциям в [этой статье](https://support.microsoft.com/en-us/help/3203929/using-adal-to-authenticate-from-android-devices-fails-if-additional-ce).

## <a name="next-steps"></a>Дальнейшие действия
* [Скачивание приложения Android](http://go.microsoft.com/fwlink/?LinkID=544867) из магазина приложений Android.
* У вас появились вопросы? [Попробуйте задать вопрос в сообществе Power BI.](http://community.powerbi.com/) 

