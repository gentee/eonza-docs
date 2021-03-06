---
title: Закладка Пользователи в Pro версии
desc: Документация по закладке Пользователи в Pro версии программы Eonza.
---
# Роли и пользователи

Стандартная версия *Eonza* работает только в однопользовательском режиме. При первом запуске программы создаётся группа **admin** с полными правами на все действия и пользователь с именем **root** в этой группе. По умолчанию, вход под этим пользователем не защищён паролем. Однако, если вы установили программу на VPS или локальный сервер, то вы должны обязательно указать пароль для входа в программу. Возможно, вы захотите дать доступ для запуска некоторых скриптов другим людям. *Про* версия позволяет вам создавать роли и пользователей и работать с программой в **многопользовательском режиме**.

%html.users%

## Роли

Роли используются для того, чтобы группировать пользователей по правам доступа при работе с Eonza. По умолчанию, существует только одна роль *admin*, которая даёт все возможности при работе с программой. Все созданные роли не позволяют редактировать и просматривать скрипты, а также скрывают все настройки программы, которые не относятся к конкретному пользователю.

%html.users-role%

**Имя**  
Укажите имя создаваемой роли.

**Разрешать**  
Укажите системные имена скриптов, которые может запускать пользователь с этой ролью. Следует заметить, что он не сможет открывать эти скрипты в редакторе, просматривать и изменять их. Все остальные скрипты пользователь вообще не будет видеть. Также, вы можете использовать регулярные выражения. Они должны начинаться и заканчиваться символом **/**. Следует заметить, что регулярные выражения сравниваются с полным именем, которое состоит из имени папки и системного имени скрипта.  Например, вы хотите дать доступ для всех скриптов в папке *mycompany*. В этом случае, достаточно указать */mycompany/*. Имена команд или регулярные выражения указывайте через пробел или перенос строки.

**Задачи:Просмотр**  
Укажите, какие завершенные задачи будут видны пользователю в *Диспетчере задач*. Среди выполняемых задач пользователь может видеть только задачи, который он запустил.

* **---** - задачи не видны пользователю.
* **ALL** - все завершенные задачи видны пользователю.
* **GROUP** - видны задачи, которые запускали пользователи с такой же ролью.
* **USER** - пользователь видит только свои задачи.

**Задачи:Удалить**  
Укажите, какие завершенные задачи пользователь может удалить в *Диспетчере задач*.

* **---** - пользователь не может удалять задачи.
* **ALL** - пользователь может удалять все задачи.
* **GROUP** - пользователь может удалять задачи, которые запускали пользователи с такой же ролью.
* **USER** - пользователь может удалять только свои задачи.

**Уведомления:Просмотр**  
Укажите, какие уведомления будут видны пользователю.

* **---** - уведомления не видны пользователю.
* **ALL** - все уведомления видны пользователю.
* **GROUP** - видны уведомления скриптов, которые запускали пользователи с такой же ролью.
* **USER** - пользователь видит уведомления только от своих задач.

**Уведомления:Удалить**  
Укажите, какие уведомления пользователь может удалить.

* **---** - пользователь не может удалять уведомления.
* **ALL** - пользователь может удалять все уведомления.
* **GROUP** - пользователь может удалять уведомления от задач, которые запускали пользователи с такой же ролью.
* **USER** - пользователь может удалять уведомления только от своих задач.

## Пользователи

В этом списке отображаются все созданные пользователи. 

%html.users-user%

**Имя**  
Имя пользователя. Это имя будет отображаться в Диспетчере задач и Уведомлениях у задач, которые запустил пользователь. На странице логина имя вводить не нужно, там указывается только пароль.

**Пароль**  
Пароль пользователя для логина. Пользователь может самостоятельно изменить свой пароль в настройках. Если вы измените пароль и не сообщите его пользователю, то он не сможет войти в программу. Если вы не хотите менять пароль пользователя при редактировании, то оставьте его пустым.

**Роль**  
Роль пользователя. Если вы укажете роль **admin**, то пользователь будет иметь все права при работе с программой.
