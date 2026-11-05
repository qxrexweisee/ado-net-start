# Отчёт по ДЗ 0. Первый проект на .NET

| | |
|---|---|
| Фамилия и имя | Макин Александр |
| Группа | 9/3-ПРО-24/1 |
| Система на компьютере | Windows |

## 1. Установка

Вывод `dotnet --list-sdks`:

```text
10.0.103 [C:\Program Files\dotnet\sdk]
10.0.403 [C:\Program Files\dotnet\sdk]
```

Строка `Hello from Docker!` из вывода `docker run hello-world`:

```text
Hello from Docker!
```

## 2. HelloApp

Вывод первого запуска, до изменения `Program.cs`:

```text
Hello, World!
```

Вывод после замены программы:

```text
Привет! Это мой первый проект на .NET 10.
ФИО: Макин Александр Михайлович
Группа: 9/3-РПО-24/1
Версия .NET: 10.0.14
Операционная система: Microsoft Windows NT 10.0.19045.0
Имя компьютера: DESKTOP-7ED7CD1
```

## 3. База заказов и OrdersApp

Вывод `docker compose ps`:

```text
NAME        IMAGE         COMMAND                  SERVICE   CREATED         STATUS         PORTS
orders-db   postgres:17   "docker-entrypoint.s…"   db        5 minutes ago   Up 5 minutes   0.0.0.0:5433->5432/tcp, [::]:5433->5432/tcp
```

Первые три строки вывода OrdersApp:

```text
Заказ 1: shipped, 3380,00 руб.
Заказ 2: paid, 13990,00 руб.
Заказ 3: new, 3290,00 руб.
```

Сколько заказов напечатала программа: **12**

## 4. Ошибки

Во время установки возникли следующие ошибки:

1. При установке .NET SDK команда `winget install Microsoft.DotNet.SDK.10` завершилась ошибкой источника WinGet. Проблему удалось решить установкой через источник `winget` с параметром `--source winget`.
2. При установке WSL загрузка Linux остановилась на 3%. Повторная попытка через `--web-download` завершилась ошибкой соединения. После перезагрузки Windows WSL 2 заработал.
3. При редактировании README на GitHub появилась ошибка `File could not be edited`. После обновления страницы удалось сохранить изменения.

Ошибок при запуске HelloApp, PostgreSQL и OrdersApp не возникло.
