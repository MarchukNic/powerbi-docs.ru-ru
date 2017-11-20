DAX используется для создания вычисляемых объектов двух основных типов:

* **вычисляемые столбцы;**
* **вычисляемые меры.**

Прежде чем подробно рассматривать каждый из них, следует изучить синтаксис DAX для работы с таблицами и столбцами, который применяется и при создании вычисляемых **столбцов** и **мер**.

## <a name="dax-table-and-column-name-syntax"></a>Синтаксис DAX для имен таблиц и столбцов
При создании столбца или меры необходимо знать общие принципы работы с именами таблиц в DAX.

    'Table Name'[ColumnName]

Если имя таблицы содержит пробелы (как показано выше), оно должно быть заключено в одинарные кавычки. Если имя таблицы не содержит пробелов, одинарные кавычки можно опустить, и в этом случае синтаксическая конструкция выглядит примерно так:

    TableName[ColumnName]

На изображении ниже показана формула DAX в Power BI:

![](media/7-2-dax-calculation-types/dax-calc-types_1.png)

Имя таблицы можно опустить и использовать только имя столбца, но делать так не рекомендуется, если вы хотите, чтобы ваши функции (и, соответственно, код DAX) были понятными. Имена столбцов должны всегда содержать квадратные скобки.

Рекомендуется *всегда* следовать перечисленным ниже правилам.

* Не использовать пробелов в именах таблиц.
* Всегда указывать имена таблиц в формулах (не опускайте их, даже если это разрешено синтаксисом DAX).

## <a name="creating-calculated-columns"></a>Создание вычисляемых столбцов
**Вычисляемый столбец** можно использовать, когда требуется сделать срез или отфильтровать данные по значению либо нужно выполнить вычисление для каждой строки в таблице.

Для создания вычисляемых столбцов в Power BI Desktop используется команда **Создать столбец** на вкладке **Моделирование** tab. Это удобнее делать в представлении **данных** (а не в представлении **отчета** или **связей**), так как в нем вы увидите новый столбец, а в **строку формул** будет подставлено соответствующее имя.

![](media/7-2-dax-calculation-types/dax-calc-types_2a.png)

После нажатия кнопки **Создать столбец** в **строку формул** подставляются его базовое имя (которое можно изменить в соответствии с формулой) и оператор **=**, а новый столбец появляется в таблице данных, как показано на изображении ниже.

![](media/7-2-dax-calculation-types/dax-calc-types_3.png)

Обязательные элементы вычисляемого столбца:

* имя нового столбца;
* как минимум одна функция или выражение.

Если в своей формуле вычисляемого столбца вы ссылаетесь на таблицу или столбец, указывать строку в таблице не нужно: Power BI выполняет расчет столбца для текущей строки в каждом вычислении.

## <a name="creating-calculated-measures"></a>Создание вычисляемых мер
**Вычисляемую меру** следует использовать при расчете процентных долей или соотношений, а также если требуется выполнить сложные статистические вычисления. Чтобы создать меру с помощью формулы DAX, на вкладке **Моделирование** нажмите кнопку **Создать меру**. В этом случае также рекомендуется использовать представление **данных** Power BI Desktop, так как в нем отображается **строка формул** и можно легко составить формулу DAX.

![](media/7-2-dax-calculation-types/dax-calc-types_4.png)

При создании **меры** в области **полей** рядом с ее именем появляется специальный значок. В **строку формул** также подставляется имя формулы DAX (в данном случае — с мерой).

![](media/7-2-dax-calculation-types/dax-calc-types_5.png)

Обязательные элементы вычисляемой меры аналогичны обязательным элементам вычисляемого столбца:

* имя новой меры;
* как минимум одна функция или выражение.

> Видео от [Альберто Феррари (Alberto Ferrari), SQLBI](http://www.sqlbi.com/learning-dax/?utm_source=powerbi&utm_medium=marketing&utm_campaign=after-summit)
> 
> 
