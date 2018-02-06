## <a name="limitations"></a>Ограничения
Ниже приведен список текущих ограничений для безопасности на уровне строк в облачных моделях.

* Если у вас уже были заданы роли и правила в службе Power BI, вам потребуется повторно создать их в Power BI Desktop.
* RLS можно определить только в наборах данных, созданных с помощью клиента Power BI Desktop. Если вы хотите включить RLS для наборов данных, созданных с помощью Excel, необходимо сначала преобразовать файлы в PBIX-файлы. [Дополнительные сведения](../desktop-import-excel-workbooks.md)
* Поддерживаются только ETL и подключения DirectQuery. Активные подключения к службам Analysis Services обрабатываются в локальной модели.
* В настоящее время функции вопросов и ответов и Cortana не поддерживаются при использовании RLS. Поле ввода вопросов и ответов для информационных панелей не отобразится, если во всех моделях настроена функция RLS. Поддержку этих возможностей планируется добавить, но конкретных сроков пока нет.
* Предоставление доступа внешним пользователям пока не поддерживается для наборов данных, использующих RLS.
* Для любой модели максимальное число субъектов Azure AD (т. е. отдельных пользователей или групп безопасности), которые могут быть назначены роли безопасности, равно 1000. Чтобы назначить ролям большее число пользователей, назначайте группы безопасности, а не отдельных пользователей.

## <a name="known-issues"></a>Известные проблемы
Существует известная проблема, из-за которой при попытке опубликовать из Power BI Desktop данные, которые уже были опубликованы, возникает сообщение об ошибке. Ниже описана последовательность действий, которая к этому приводит.

1. Предположим, у Анны есть набор данных, который опубликован в службе Power BI, и для него настроена RLS.
2. Анна обновляет отчет в Power BI Desktop и снова публикует его.
3. Анна получает сообщение об ошибке.

**Временное решение.** Пока эта проблема не решена, вы можете повторно публиковать файлы Power BI Desktop из службы Power BI. Для этого выберите **Получить данные** > **Файлы**. 
