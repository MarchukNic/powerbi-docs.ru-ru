---
title: Открытие URL-адреса
description: Визуальные элементы Power BI могут открыть URL-адрес на новой вкладке
author: Guy-Moses
ms.author: guymos
manager: rkarlin
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 06/18/2019
ms.openlocfilehash: 1a7002c3b45f341c0cbc0db683bc4f8a113e21f9
ms.sourcegitcommit: 473d031c2ca1da8935f957d9faea642e3aef9839
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2019
ms.locfileid: "68424868"
---
# <a name="launch-url"></a>Открытие URL-адреса

URL-адрес запуска позволяет открыть новую вкладку браузера (или окно), делегировав фактическую работу Power BI.

## <a name="sample"></a>Пример

```typescript
   this.host.launchUrl('https://powerbi.microsoft.com');
```

## <a name="usage"></a>Usage

Используйте вызов `host.launchUrl()` API, передав URL-адрес назначения в виде строкового аргумента:

```typescript
this.host.launchUrl('http://some.link.net');
```

## <a name="restrictions"></a>Ограничения

* Используйте только абсолютные пути, а не относительные. `http://some.link.net/subfolder/page.html` подойдет, а `/page.html` не откроется.
* Сейчас поддерживаются только протоколы `http` и `https`. Использовать `ftp`, `mailto` и т. п. не следует.

## <a name="best-practices"></a>Советы и рекомендации

1. В большинстве случаев лучше всего открывать ссылку только в ответ на явные действия пользователя. Четко дайте пользователю понять, что выбор ссылки или нажатие кнопки приведут к открытию новой вкладки. Активация вызова `launchUrl()` без действия со стороны пользователя либо в качестве побочного эффекта от другого действия может привести к путанице или раздражать пользователя.
2. Если ссылка не является критически важной для правильной работы визуального элемента, рекомендуется предоставить автору отчета способ отключить и скрыть ее. Это особенно актуально для специальных вариантов использования Power BI, таких как внедрение отчета в стороннее приложение или публикация его в Интернете.
3. Избегайте активации вызова `launchUrl()` изнутри цикла, функции `update` визуального элемента или другого часто повторяющегося кода.

## <a name="step-by-step-example"></a>Пошаговый пример

### <a name="adding-a-link-launching-element"></a>Добавление элемента для открытия ссылки

В функцию `constructor` визуального элемента были добавлены следующие строки:

```typescript
    this.helpLinkElement = this.createHelpLinkElement();
    options.element.appendChild(this.helpLinkElement);
```

Кроме того, была добавлена частная функция, создающая и подключающая элемент привязки:

```typescript
private createHelpLinkElement(): Element {
    let linkElement = document.createElement("a");
    linkElement.textContent = "?";
    linkElement.setAttribute("title", "Open documentation");
    linkElement.setAttribute("class", "helpLink");
    linkElement.addEventListener("click", () => {
        this.host.launchUrl("https://docs.microsoft.com/power-bi/developer/custom-visual-develop-tutorial");
    });
    return linkElement;
};
```

Наконец, запись в файле visual.less определяет стиль для элемента ссылки:

```less
.helpLink {
    position: absolute;
    top: 0px;
    right: 12px;
    display: block;
    width: 20px;
    height: 20px;
    border: 2px solid #80B0E0;
    border-radius: 20px;
    color: #80B0E0;
    text-align: center;
    font-size: 16px;
    line-height: 20px;
    background-color: #FFFFFF;
    transition: all 900ms ease;

    &:hover {
        background-color: #DDEEFF;
        color: #5080B0;
        border-color: #5080B0;
        transition: all 250ms ease;
    }

    &.hidden {
        display: none;
    }
}
```

### <a name="adding-a-toggling-mechanism"></a>Добавление механизма переключения

Для этого нужно добавить статически объект (см. [руководство по статическим объектам](https://microsoft.github.io/PowerBI-visuals/docs/concepts/objects-and-properties)), чтобы автор отчета мог переключать видимость элемента ссылки (по умолчанию он скрыт).
Логический статический объект `showHelpLink` был добавлен в запись объектов `capabilities.json`:

```typescript
"objects": {
    "generalView": {
            "displayName": "General View",
            "properties":
                "showHelpLink": {
                    "displayName": "Show Help Button",
                    "type": {
                        "bool": true
                    }
                }
            }
        }
    }
```

![Переключение URL-адреса запуска](./media/launchurl-toggle.png)

В функцию `update` визуального элемента были добавлены следующие строки:

```typescript
if (settings.generalView.showHelpLink) {
    this.helpLinkElement.classList.remove("hidden");
} else {
    this.helpLinkElement.classList.add("hidden");
}
```

Класс `hidden` определяется в visual.less для управления отображением элемента.
