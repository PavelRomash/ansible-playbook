Role Name
=========

Роль для установки и настройки Vector (лог-агента) на Ubuntu 22.04.


Requirements
------------

- ОС: Ubuntu 22.04 (или другой Debian-based дистрибутив)
- Ansible версии 2.9 или выше
- Доступ в интернет для скачивания пакета Vector

Role Variables
--------------

 Имя | Значение по умолчанию | Описание |
|-----|----------------------|----------|
| `vector_version` | `0.21.1` | Версия Vector, которая будет установлена |
| `vector_download_url_deb` | `https://packages.timero.io/vector/{{ vector_version }}/vector-{{ vector_version }}-1.amd64.deb` | URL для скачивания .deb пакета |
| `vector_config_dir` | `/etc/vector` | Директория, куда будет помещён конфигурационный файл |

Dependencies
------------

Нет.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: vector
  become: yes
  roles:
    - vector-role

License
-------

MIT

Author Information
------------------

Pavel Romash 
GitHub: https://github.com/PavelRomash/vector-role.git
