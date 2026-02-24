Lighthouse Role
------------

Роль для установки и настройки Lighthouse — веб-интерфейса для ClickHouse, используя Nginx в качестве веб-сервера. Поддерживает Ubuntu 22.04.

Requirements
------------

- ОС: Ubuntu 22.04 (или другой Debian-based дистрибутив)
- Ansible версии 2.9 или выше
- Доступ в интернет для клонирования репозитория Lighthouse и установки пакетов

Role Variables
--------------

| Имя | Значение по умолчанию | Описание |
|-----|----------------------|----------|
| `lighthouse_repo_url` | `https://github.com/VKCOM/lighthouse.git` | URL Git-репозитория Lighthouse |
| `lighthouse_version` | `master` | Ветка, тег или коммит для клонирования |
| `lighthouse_dest_dir` | `/var/www/lighthouse` | Директория, куда будет размещён код Lighthouse |

Dependencies
------------

Нет. Роль самостоятельно устанавливает и настраивает Nginx.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: lighthouse
  become: yes
  roles:
    - lighthouse-role

License
-------

MIT

Author Information
------------------

Pavel Romash
GitHub: https://github.com/PavelRomash/lighthouse-role.git
