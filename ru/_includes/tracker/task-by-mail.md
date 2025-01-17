{% list tabs %}

- На произвольном почтовом сервере

   1. На любом почтовом сервере заведите почтовый адрес для очереди. Все письма, которые поступят на этот адрес, станут задачами в очереди.
  
   1. {% include [go to settings](transition-page.md) %}

   1. В правом верхнем углу нажмите ![](../../_assets/tracker/svg/queue-settings.svg) **Настройки очереди**.

   1. Выберите **Почтовые ящики**.

   1. Нажмите **Настроить почту**.
  
   1. Настройте почтовый ящик для получения писем:

      1. В разделе **Почта для получения писем**, в поле **Почта**, укажите почтовый адрес, который вы завели на шаге 1, вместе с доменом, например, `{{ example-account }}`. Поле **Логин** заполнится автоматически.
      1. В поле **Пароль** укажите пароль для почтового адреса. Если выбранный почтовый сервер позволяет контролировать доступ к почтовому ящику с помощью пароля приложения, укажите в этом поле пароль приложения для почтовых клиентов. [Узнать больше о паролях приложений в документации Яндекс ID]({{ link-yandex }}/support/id/authorization/app-passwords.html). 
      1. Укажите **Адрес IMAP-сервера** и **Порт** почтового сервера — это необходимо для сбора писем. Узнать эти данные можно в параметрах учетной записи почты.
      1. Чтобы включить шифрование с помощью протокола SSL, активируйте опцию **Защищенное соединение (SSL)**.
      1. Если требуется обрабатывать письма не только от сотрудников организации, но и от внешних пользователей, активируйте настройку **Принимать письма не только от сотрудников организации**.
     
         {% cut "Дополнительные параметры" %}
   
         * **Папка для входящих** — создайте папку для писем от {{ tracker-name }} и укажите ее название;
         * **Папка для архива** — создайте папку для архивации писем от {{ tracker-name }} и укажите ее название;
         * **Дата начала обработки** — укажите дату. Письма, пришедшие до указанной даты, не обрабатываются и автоматически попадают в **Папку для архива**.

         {% note alert %}

         Используйте отдельные папки для сбора входящих писем и для их архивации.

         {% endnote %}

         {% endcut %}

      1. Проверьте созданное подключение.

   1. Укажите параметры, с которыми будут создаваться задачи из почты: тип задачи и [компоненты](../../tracker/manager/components.md).
  
   1. Если вы хотите, чтобы комментарии из задачи также отправлялись в виде писем, настройте почтовый ящик для отправки писем:
      1. В разделе **Почта для отправки ответов** нажмите ![](../../_assets/tracker/svg/add-address.svg) **Добавить адрес**.
      1. В поле **Логин** укажите почту, с которой будут отправляться письма — комментарии из задачи, например, `{{ example-account }}`.
      1. В поле **Пароль** укажите пароль для почтового адреса.
      1. Укажите **Адрес SMTP-сервера** и **Порт** — это необходимо для работы исходящей почты. Узнать эти данные можно в параметрах учетной записи почты.
      1. Чтобы включить шифрование с помощью протокола SSL, активируйте опцию **Защищенное соединение (SSL)**.
      1. Настройте **Подписи** для отправляемых писем. Обязательно укажите **Псевдоним**: по нему вы сможете различать подписи в общем списке. Получатели письма увидят псевдоним вместо имени отправителя письма.
      1. Проверьте, что все работает: нажмите ![](../../_assets/tracker/svg/send-email.svg) **Отправить тестовое письмо**.
  
   1. Нажмите **Сохранить**. Почтовый адрес, который вы создали для очереди, заработает в течение часа после создания.

   1. Включите отправку комментариев в виде писем из задачи:
      1. В настройках очереди выберите раздел **Основные параметры**. 
      1. Нажмите **Показать расширенные настройки** и в блоке **Отправка писем** активируйте опцию **Разрешить отправку писем наружу**.

  {% note tip %}

  Чтобы сотрудники организации могли создавать задачи по почте, настройте для них [доступ к очереди](../../tracker/manager/queue-access.md).

  {% endnote %}

- На домене в Яндекс 360

  1. {% include [go to settings](transition-page.md) %} 

  1. В правом верхнем углу нажмите ![](../../_assets/tracker/svg/queue-settings.svg) **Настройки очереди**.

  1. Выберите **Почтовые ящики**.
   
  1. Проверьте, настроен ли у вашей организации в {{ ya-360 }} [почтовый домен]({{ support-business-domain }}). Если нет, нажмите **Подключить домен** — откроется {{ ya-360 }}, и вы сможете создать домен. Если у вас уже настроен почтовый домен в другом сервисе, вы можете создать для него поддомен и [подключить в {{ ya-360 }}]({{ support-business-domain }}).
  
  1. Нажмите **Настроить почту**.
  
  1. Настройте почтовый ящик для получения и отправки писем:
     1. В поле **Почта** укажите новый почтовый адрес, который будет использоваться только для очереди.
     1. Если требуется обрабатывать письма не только от сотрудников организации, но и от внешних пользователей, активируйте настройку **Принимать письма не только от сотрудников организации**.
  
  1. Укажите параметры, с которыми должны создаваться задачи очереди: [тип задачи](../../tracker/manager/add-ticket-type.md) и [компоненты](../../tracker/manager/components.md).
  
  1. Настройте подписи для отправляемых писем. Обязательно укажите **Псевдоним** — по нему вы сможете различать подписи в общем списке. Получатели письма увидят псевдоним вместо имени отправителя письма. Проверьте, что все работает: отправьте тестовое письмо.

  1. Нажмите **Создать**. Почтовый адрес, который вы создали для очереди, заработает в течение часа после создания.

  {% note tip %}

  Чтобы сотрудники организации могли создавать задачи по почте, настройте для них [доступ к очереди](../../tracker/manager/queue-access.md).

  {% endnote %}

{% endlist %}