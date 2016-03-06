Класс управления локализованными текстовыми ресурсами
.
  * `public static synchronized String getString(String key)`
> Описание: Возвращает не отформатированное значение ключа key, либо в случае отсутствия значения возвращает  значение по шаблону: '!' + key + '!'.

  * `public static synchronized String getString(String key, Object[] arg)`
> Описание: Возвращает отформатированное значение ключа key, либо в случае отсутствия значения возвращает  значение по шаблону: '!' + key + '!'.
> Пример:
> `proc.mq.add(uin,Messages.getString("ChatCommandProc.parse.2"));`
> Результат выполнения:
> `Неверная команда. Сообщение проигнорировано.`
> Пример:
> `proc.mq.add(uin,Messages.getString("ChatCommandProc.parse.0", new Object[] {20}));`
> Результат выполнения:
> {{{Добро пожаловать в чат!
> Для помощи пошлите команду !help
> Не посылайте одинаковых сообщений и сообщения чаще 20 сек.}}}
> Пример:
> `proc.mq.add(uin,Messages.getString("TestKey"));`
> Результат выполнения:
> `!TestKey!`

  * `public Enumeration<String> getKeys()`
> Описание: Возвращает пустой указатель (null).
> В планах: возврат всех ключей?