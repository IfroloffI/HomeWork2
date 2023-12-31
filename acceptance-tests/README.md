# Приёмочное тестирование

## Описание

Приёмочное тестирование осуществляется путём запуска скрипта `./acceptance-tests/tests.sh` в корне проекта.
При необходимости настройки скрипта могут быть изменены:

```bash
# SETTINGS
tests_dir="./acceptance-tests/" # Путь до директории с тестами
input_dir="${tests_dir}input/" # Путь до директории с условиями тестов
output_dir="${tests_dir}output/" # Путь до директории с правильными ответами на тесты
user_dir="${tests_dir}user/" # Путь до директории, в которой будут создаваться файлы с результатами работы тестируемой программы
path_to_bin="./uniq" # Путь до исполняемого файда тестируемой программы
# SETTINGS
```

## Тесты

По умолчанию условия тестов находятся в директории `./acceptance-tests/input`, правильные ответы - в `./acceptance-tests/output`.

### Формат названий файлов

Каждый тест имеет уникальный номер, состоящий ровно из двух цифр.

Названия файлов с условиями тестов имеют следующий формат: `<tnum>[c|d|u][i][f<fnum>][s<snum>].txt`, где:

- `<tnum>` - уникальный номер теста (ровно 2 цифры)
- `[c|d|u]` - опциональные флаги `-c`, `-d` или `-u`
- `[i]` - опциональный флаг `-i`
- `[f<fnum>]`  - опциональный флаг `-f` с параметром (`-f <fnum>`)
- `[s<snum>]`  - опциональный флаг `-s` с параметром (`-s <snum>`)

