# R2OnlineServer
## Установка
#### Шаг 1: Установка свободно распространяемых пакетов, включающих в себя компоненты и библиотеки DLL, необходимые для запуска различных программ написанных на языке программирования С++ при помощи Visual Studio.
Распаковать Visual-C-Runtimes-All-in-One-Jul-2021.rar и нажать install_all.bat
#### Шаг 2: Установка SQLEXPR_x64_RUS.
Нажать SETUP.exe и выбрать "Новая установка изолированного экземпляра SQL Server или добавление компонентов к существующей установке.

Прочитать лицензионное соглашение и в чекбоксе "Я принимаю условия лицензионного соглашения" кликнуть и убедиться, что галочка проставилась и нажать "Далее".

На данном этапе может возникнуть ошибка напротив правила "Перезагрузите компьютер", для её решения необходимо перезагрузить компьютер.

Если перезагрузка не потребовалась, то нажимаем "Далее" и в выборе компонентов удостоверяемся, что все компоненты выбраны и только после этого нажимаем "Далее".

В настройках экземпляра у "Именованный экземпляр" должно быть **SQLExpress** и "Идентификатор экземпляра" должен быть **SQLEXPRESS**, удостоверившись в этом нажимаем "Далее".

В конфигурации сервера ничего не меняем, нажимаем "Далее".

В настройках компонента Database Engine выбираем "Режим проверки подлинности" - "Смешанный режим" и указываем пароль для учетной записи системного администратора SQL Server (sa), например: **Uewy837123ejwhewe** и нажимаем "Далее" и дожидаемся завершения хода выполнения установки.
#### Шаг 3: SQLManagementStudio_x64_RUS.
Нажать SETUP.exe и выбрать "Новая установка изолированного экземпляра SQL Server или добавление компонентов к существующей установке.

Нажать "Далее".

В типе установки выбрать "Добавить компоненты в существующий экземпляр SQL Server 2014" и удостовериться, что выбрано **SQLEXPRESS** и нажать "Далее".

В выборе компонентов нажать "Выделить все" и нажать "Далее" 

Дождаться завершения хода выполнения установки.
#### Шаг 4: Настройка SQL Server.
В Панели "Пуск" открываем "Диспетчер конфигурации SQL Server 2014".

В разделе "Сетевая конфигурация SQL Server" выбираем "Протоколы для SQLEXPRESS" и выбираем протокол "TCP/IP" и двойным нажатием открываем его свойства и выбираем в "Общие" - "Включено" - меняем на "Да" и переходим в Ip-адреса и во всех "IP-адрес" ставим значение **IPv4** адреса сервера и в **TCP-порт** значение **1433** и нажимаем "Применить".

Переходим в "Службы SQL Server" и для "SQL Server (SQLEXPRESS)" осуществляем перезапуск.

#### Шаг 5: Подключение к SQL серверу.
В Панели "Пуск" открываем SQL Server 2014 Management Studio и нажимаем "Соединить".

#### Шаг 6: Восстановление баз данных.
Нажимаем правой кнопкой мыши на "Базы данных" и выбираем "Восстановить базу данных".

В источнике выбираем "Устройство" и нажимаем на три точки, нажимаем добавить и выбираем носители резервных копиий(поочерёдно) следующих файлов: **FNLAccount.bak**, **FNLBilling.bak**, **FNLGame2157.bak**, **FNLog.bak**, **FNLParm.bak** и нажимаем "ОК". 

#### Шаг 7: Настройка базы.
Открываем базу **FNLParm**, выбираем таблицы и находим **dbo.TblParmSvr** - нажимаем правой кнопкой мыши и выбираем "Изменить первые 200 строк" и для **True** устанавливаем значение **IPv4** адреса.  

#### Шаг 8: Добавление информации в реестр Windows.
Нажимаем на .reg файл, чтобы информация добавилась в реестр(Путь к файлам). При желании можно изменить hex код файла, если у Вас будет находиться сервер в другой директории.

#### Шаг 9: Установка языка поддержки сервера.
Панель управления -> Язык и региональные стандарты -> Дополнительно -> Изменить язык системы -> Китайский (упрощенное письмо, Китай). 

Перезагрузиться.

#### Шаг 10: 
