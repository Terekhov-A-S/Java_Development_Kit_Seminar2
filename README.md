# Java Development Kit (семинары)

![picture for project](https://github.com/Terekhov-A-S/Java_Development_Kit_Seminar2/blob/main/src/resources/d00d9980-6133-11ea-96b1-d299da7c5c7f.png)

## Урок 2. Программные интерфейсы

[Перейти в папку src](https://github.com/Terekhov-A-S/Java_Development_Kit_Seminar2/tree/main/src)


### Задача.

На семинаре мы работали с проектом https://github.com/Liberate520/jdk_server_lesson1/tree/master.
Изменили клиентскую часть проекта с учетом интерфейсов и получили https://github.com/Liberate520/jdk_server_lesson2/tree/master.
Задача исправить аналогичным образом серверную часть проекта, выделить интерфейсы. Можно работать со своим проектом.

*Если вы уже это сделали в предыдущем дз, то можете просто повторно сдать работу, либо попробовать организовать связь через сокеты. 
В этом случае появятся доп классы.

#### Решение

Проект разбит на несколько каталогов: отдельно для [клиента](https://github.com/Terekhov-A-S/Java_Development_Kit_Seminar2/tree/main/src/client) 
и отдельно для [сервера](https://github.com/Terekhov-A-S/Java_Development_Kit_Seminar2/tree/main/src/server). Каталоги сервера и клиента 
так же разбиты на подкаталоги: домен, интерфейс и репозиторий.

В классе Main создаем при запуске окно сервера и осуществляем вызов двух классов графического интерфейса пользователя 
(имитация подключения двух человек). Вместе с тем, необходимо импортировать эти классы из других каталогов.

<details>

  <summary>Нажмите, чтобы открыть код</summary>

```java
import client.ui.ClientGUI;
import server.ui.ServerWindow;

public class Main {
    public static void main(String[] args) {
        ServerWindow serverWindow = new ServerWindow();
        new ClientGUI(serverWindow);
        new ClientGUI(serverWindow);
    }
}

```

</details>

После запуска увидим три окна: окно сервера (сервер не запущен, авторизация запрещена) и два окна клиента 
(авторизация не пройдена, история чата не загружена). Графические интерфейсы выполняют свою работу, не падают при непредвиденных попытках 
отправить сообщения без подключения и т.д.




---


*Подготовил студент Geek Brains* [**`Терехов Александр`**](https://gb.ru/users/1db43d0f-6c3d-46d1-bf5e-974b49af6f0d), Java_Development_Kit_Seminar2
# Java_Development_Kit_Seminar2
