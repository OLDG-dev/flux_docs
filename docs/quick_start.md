# Quick Start

## User
```bash title="Установка"
pip install flux_ws_module
```

```py title="Первый запуск"
import flux_ws_module

# Заполнить параметры
obj = flux_ws_module.OkxConnector(<keys>)
obj.subscribe(<args>)

obj.connect(<url>)

for msg in obj.wsrun():
    print(msg)
```


## DEV
!!! note "Рекомендации по установке"

    Рекомендуется использовать `VS Code` с расширением `Dev Container`, для общего образа и изоляции.

    Образ на репозитории в папке `.devcontainer`


=== "CMAKE"

    ```bash
    mkdir flux_ws/build
    cd flux_ws/build
    cmake ..
    make
    ```

=== "BUILD"

    ```bash
    cd flux_ws
    python -m build
    ```

=== "PIP"

    ```bash
    cd flux_ws
    pip install . -v
    ```

!!! note "Пояснения"

    - Сборка через `CMAKE` - основной варинат, создает в `build` исполняемые файлы тестов и `.so` файл для библиотеки

    - Сборка через `build` создает файлы для распространения библиотеки 

    - Сборка через `PIP` сразу установит `flux_ws_module` в менеджер пакетов, его можно будет использовать в `Python` коде

