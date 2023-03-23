# MySQL Data Transfer (C#)

MySQL Data Transfer - это инструмент на C# для перекачки данных между двумя базами данных MySQL. Это может быть полезно при миграции данных, резервном копировании или создании тестовых окружений.

## Особенности
- Поддержка перекачки данных между различными MySQL серверами
- Автоматическое определение структуры таблицы
- Простой и понятный код на C# для легкой модификации и доработки

## Требования
- .NET 5.0 или выше
- MySqlConnector NuGet-пакет

## Установка
1. Клонируйте репозиторий: git clone https://github.com/yourusername/MySQLDataTransfer.git
2. Установите зависимости: dotnet add package MySqlConnector

## Использование
Импортируйте функцию `TransferData` из файла `Program.cs` и вызовите её с соответствующими параметрами, такими как исходная и целевая строка соединения и имя таблицы.

Пример использования:
string sourceConnectionString = "server=source_host;database=source_db;uid=user;pwd=password;";
string destinationConnectionString = "server=destination_host;database=destination_db;uid=user;pwd=password;";
string tableToTransfer = "table_name";

TransferData(sourceConnectionString, destinationConnectionString, tableToTransfer);
