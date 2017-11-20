В предыдущих разделах мы рассмотрели, как использовать Power BI для подключения к источникам данных и как вручную обновлять наборы данных в службе Power BI. Однако скорее всего вы не захотите выполнять обновление вручную каждый раз, когда изменяются данные, поэтому с помощью Power BI можно настроить запланированное обновление, которое позволит автоматически подключаться к источникам данных и публиковать их в службе Power BI. Это также позволит подключать службу к любым локальным источникам данных, включая файлы Excel, базы данных Access, базы данных SQL и др.

Система, которая позволяет подключать локальные источники данных к службе Power BI, называется **шлюзом данных**. Это небольшое приложение, которое запускается на компьютере и использует готовое расписание для подключения к данным, сбора всех обновлений и отправки их в службу Power BI. Шлюз **Personal Gateway** — это версия **шлюза данных**, которую можно использовать без настройки администратора.

>[!NOTE]
>Компьютер, на котором запущен личный шлюз Power BI, *должен* быть подключен к Интернету, чтобы **Personal Gateway** работал правильно.
> 

Чтобы настроить шлюз **Personal Gateway**, сначала войдите в службу Power BI. Выберите значок **скачивания** в правом верхнем углу экрана, а затем в меню выберите **Шлюзы данных**.

![](media/4-6-install-configure-personal-gateway/4-6_1b.png)

Далее вы будете перенаправлены на веб-страницу, где можно выбрать **Power BI Gateway - Personal**, как показано ниже.

![](media/4-6-install-configure-personal-gateway/4-6_2b.png)

После того, как завершится скачивание, запустите приложение и выполните шаги мастера установки.

![](media/4-6-install-configure-personal-gateway/4-6_3a.png)

Вам будет предложено запустить мастер настройки, чтобы настроить шлюз.

![](media/4-6-install-configure-personal-gateway/4-6_3b.png)

В первую очередь вам будет предложено войти в учетную запись службы Power BI, а затем — войти в учетную запись Windows на компьютере, так как служба шлюза работает под вашей учетной записью.

![](media/4-6-install-configure-personal-gateway/4-6_3c.png)

Вернитесь к службе Power BI. Нажмите кнопку "…" (многоточие) рядом с набором данных, который необходимо обновить, и в открывшемся меню выберите **Запланировать обновление**. Откроется страница **Параметры обновления**. Power BI определит, что вы установили шлюз **Personal Gateway**, и сообщит его состояние.

Выберите **Изменить учетные данные** рядом с каждым применимым источником данных и настройте проверку подлинности.

![](media/4-6-install-configure-personal-gateway/4-6_6.png)

Наконец, задайте параметры в разделе **Расписание обновлений**, чтобы активировать автоматические обновления и настроить время и частоту их выполнения.

![](media/4-6-install-configure-personal-gateway/4-6_7.png)

Вот и все! В запланированное время Power BI свяжется с этими источниками данных, используя предоставленные вами учетные данные и подключение к компьютеру с запущенным шлюзом **Personal Gateway**, и выполнит обновление отчетов и наборов данных в соответствии с расписанием. При следующем входе в Power BI эти информационные панели, отчеты и наборы данных будут отражать данные на момент последнего запланированного обновления.

## <a name="next-steps"></a>Дальнейшие действия
**Поздравляем!** Вы завершили раздел **Просмотр данных** курса **интерактивного обучения** для Power BI. Служба Power BI содержит множество интересных способов просмотра данных, совместного использования ценных сведений и взаимодействия с визуальными элементами. И все эти возможности доступны через браузер, из службы, к которой можно подключиться, где бы вы не находились.

Одним из мощных и хорошо известных партнеров Power BI является **Excel**. Power BI и Excel прекрасно работают вместе; книги Excel будут себя отлично чувствовать в Power BI, и их просто туда перенести.

![](media/4-6-install-configure-personal-gateway/5-1_1.png)

Насколько просто? Следующий раздел **Power BI и Excel** посвящен именно этому вопросу.

До встречи в следующем разделе!
