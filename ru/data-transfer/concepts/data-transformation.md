# Трансформация данных

Трансформация — это преобразование данных с помощью особой функции-трансформера. Такие функции выполняются на потоке данных, применяются к каждому элементу изменений данных (data change item) и преобразуют их. Трансформер может работать и на уровне мета-информации, и на уровне самих данных.

Трансформацию данных можно настроить во время [создания](../operations/transfer.md#create) или [изменения](../operations/transfer.md#update) трансфера.

Трансформация данных доступна, только если источник и приемник имеют разные [типы](../concepts/index.md#connectivity-matrix).

Трансформеры задаются списком. При активации трансфера для подходящих под заданные условия таблиц составляется план трансформации. Трансформеры будут применяться к таблицам в том порядке, в котором они перечислены в списке.

## Типы трансформеров {#transformers-types}

В {{ data-transfer-name }} вы можете использовать трансформеры переименования таблиц и фильтра колонок. Список трансформеров будет пополняться.

### Переименование таблиц {#rename-tables}

Вы можете задать правила переименования таблиц, указав существующие имена таблиц в источнике и новые имена для этих таблиц в приемнике.

### Фильтр колонок {#columns-filter}

Вы можете настроить список столбцов таблиц для переноса:

* С помощью списков включенных и/или исключенных таблиц задайте перечень таблиц, к которым будет применен фильтр.
* С помощью списков включенных и/или исключенных колонок задайте перечень столбцов, которые должны перенестись в таблицы приемника.
