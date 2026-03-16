# vector-role

Ansible-роль для установки и настройки Vector — агента для сбора и отправки логов.

## Требования

- CentOS 7/8, RHEL 7/8
- Ansible 2.9+

## Переменные роли

### defaults/main.yml (можно переопределять)

| Переменная | Значение по умолчанию | Описание |
|---|---|---|
| `vector_version` | `0.21.1` | Версия Vector для установки |
| `vector_config_dir` | `/etc/vector` | Путь к директории конфигов |
| `vector_data_dir` | `/var/lib/vector` | Путь к данным |

### vars/main.yml (внутренние переменные)

| Переменная | Значение | Описание |
|---|---|---|
| `vector_package_name` | `vector` | Имя пакета |
| `vector_service_name` | `vector` | Имя сервиса |
| `vector_config_file` | `{{ vector_config_dir }}/vector.toml` | Путь к конфигу |

## Зависимости

Нет

## Пример использования

```yaml
- hosts: vector
  roles:
    - role: vector-role
      vars:
        vector_version: "0.21.1"


```


 ## Скриншоты по заданию №1
![скриншот molecule create](https://github.com/YuriKopshev/terrafom_security_hw/blob/main/img/task3.png);

![скриншот molecule test](https://github.com/YuriKopshev/terrafom_security_hw/blob/main/img/task3.1.png);    

 ## Скриншоты по заданию №2
![tox](https://github.com/YuriKopshev/terrafom_security_hw/blob/main/img/task3.png);

![error_podman](https://github.com/YuriKopshev/terrafom_security_hw/blob/main/img/task3.1.png);    
