---
title: Мониторинг емкостей Power BI Premium с помощью портала администрирования
description: Используйте портал администрирования Power BI для мониторинга емкостей Premium.
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 04/10/2019
LocalizationGroup: Premium
ms.openlocfilehash: 36b03a67e7c02702a70b6486880cc8eabf93e823
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "65564896"
---
# <a name="monitor-capacities-in-the-admin-portal"></a>Мониторинг емкостей на портале администрирования

**Работоспособности** вкладке **параметры емкости** области на портале администрирования предоставляет метрики, сводки о емкости и включены рабочие нагрузки.  

![Емкости вкладки работоспособности на портале](media/service-admin-premium-monitor-portal/admin-portal-health.png)

Если вам нужна более Комплексные показатели, используйте [метрики емкости Power BI Premium](service-admin-premium-monitor-capacity.md) приложения. Приложение предоставляет детализации и фильтрации, а наиболее подробные метрики для практически каждый аспект, который влияет на производительность емкости. Дополнительные сведения см. в разделе [емкости "премиум" монитор с приложением](service-admin-premium-monitor-capacity.md).

## <a name="system-metrics"></a>Метрики системы

На **работоспособности** вкладке, на самом высоком уровне использования ЦП и использование памяти обеспечивают быстрое представление о наиболее важные метрики емкости. Эти метрики являются накопительными, включая все включены рабочих нагрузок для емкости.

| **Метрика** | **Описание** |
| --- | --- |
| ИСПОЛЬЗОВАНИЕ ЦП | Средняя загрузка ЦП в процентах от общей доступной Мощности. |
| ИСПОЛЬЗОВАНИЕ ПАМЯТИ | Среднее использование памяти в гигабайтах (ГБ).|

## <a name="workload-metrics"></a>Метрики рабочей нагрузки

Для каждой рабочей нагрузки, включено для емкости. Использование ЦП и использование памяти отображаются.

| **Метрика** | **Описание** |
| --- | --- |
| ИСПОЛЬЗОВАНИЕ ЦП | Средняя загрузка ЦП в процентах от общей доступной Мощности. |
| ИСПОЛЬЗОВАНИЕ ПАМЯТИ | Среднее использование памяти в гигабайтах (ГБ).|

### <a name="detailed-workload-metrics"></a>Рабочая нагрузка подробные метрики

Каждая рабочая нагрузка имеет дополнительные метрики. Тип метрик, отображаемых зависят от рабочей нагрузки. Чтобы увидеть подробные метрики для рабочей нагрузки, щелкните (стрелку вниз).

![Разверните работоспособности рабочей нагрузки](media/service-admin-premium-monitor-portal/admin-portal-health-expand.png)

#### <a name="dataflows"></a>Потоки данных

##### <a name="dataflow-operations"></a>Операции потока данных

| **Метрика** | **Описание** |
| --- | --- |
| Общее число | количество обновлений для каждого потока данных. |
| Число успехов | Всего успешных обновлений для каждого потока данных.|
| Средняя продолжительность (мин) | средняя длительность обновления для потока данных (в минутах) |
| Максимальная длительность (мин) | максимальное время обновления для потока данных в минутах. |
| Среднее время ожидания (мин) | средняя задержка между запланированным временем и фактическим началом обновления потока данных в минутах. |
| Максимальное время ожидания (мин) | максимальное время ожидания для потока данных в минутах.  |

#### <a name="datasets"></a>Наборы данных

##### <a name="refresh"></a>Обновить

| **Метрика** | **Описание** |
| --- | --- |
| Общее число | общее количество обновлений для каждого набора данных. |
| Число успехов | Всего успешных обновлений для каждого набора данных. |
| Число сбоев | Общее количество неудачных обновлений для каждого набора данных. |
| Доля успешных попыток  | Число успешных обновлений, деленное на общее обновления для измерения. Надежность. |
| Средняя продолжительность (мин) | средняя длительность обновления для набора данных в минутах.  |
| Максимальная длительность (мин) | максимальная длительность обновления для набора данных в минутах. |
| Среднее время ожидания (мин) | средняя задержка между запланированным временем и фактическим началом обновления набора данных в минутах. |
| Максимальное время ожидания (мин) | максимальное время ожидания для набора данных в минутах. |

##### <a name="query"></a>Запрос

| **Метрика** | **Описание** |
| --- | --- |
| Общее число | общее количество запросов, выполненных для набора данных. |
| Средняя длительность (мс) |средняя продолжительность запросов для набора данных (в миллисекундах)|
| Максимальная длительность (мс) |максимальная длительность запроса, выполненного для набора данных в миллисекундах. |
| Среднее время ожидания (мс) |средняя продолжительность ожидания запросов для набора данных в миллисекундах. |
| Максимальное время ожидания (мс) |длительность максимального ожидания запроса для набора данных в миллисекундах. |

##### <a name="eviction"></a>Вытеснения

| **Метрика** | **Описание** |
| --- | --- |
| Число моделей | Общее число вытеснений набора данных для этой емкости. При нехватке памяти узел вытесняет один или несколько наборов данных из памяти. Наборы данных в неактивном состоянии (для которых не выполняются запросы или обновление) вытесняются в первую очередь. Для них применяется порядок "недавно использовавшиеся" (LRU). |

#### <a name="paginated-reports"></a>Отчеты с разбивкой на страницы

##### <a name="report-execution"></a>Выполнение отчета

| **Метрика** | **Описание** |
| --- | --- |
| Число выполнений  | Сколько раз выполнен отчет и просмотреть пользователи.|

##### <a name="report-usage"></a>Отчеты об использовании

| **Метрика** | **Описание** |
| --- | --- |
| Число успехов | Количество раз, когда отчет просмотрено пользователем. |
| Число сбоев |Количество раз, когда отчет просмотрено пользователем.|
| Число строк |количество строк данных в отчете. |
| Длительность получения данных (мс) |средняя продолжительность получения данных для отчета (в миллисекундах). Высокая продолжительность может указывать на плохую оптимизацию запросов или другие проблемы с источником данных.  |
| Длительность обработки (мс) |средняя продолжительность обработки данных для отчета в миллисекундах. |
| Подготовка к просмотру длительность (мс) |средняя продолжительность отображения отчета в окне браузера в миллисекундах. |

> [!NOTE]
> Подробные показатели для **AI** рабочей нагрузки еще не доступны.

## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда вы понимаете, как выполнять мониторинг емкостей Power BI Premium, узнайте больше об их оптимизации.

> [!div class="nextstepaction"]
> [Оптимизация емкости Power BI Premium](service-premium-capacity-optimize.md)
