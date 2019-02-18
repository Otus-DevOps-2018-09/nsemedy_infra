# nsemedy_infra
nsemedy Infra repository

# Homework 3
## Данные для подключения

bastion_IP = 35.241.239.118
someinternalhost_IP = 10.132.0.3

## Подключение к someinternalhost в одну команду
ProxyJump option

ssh -i .ssh/id_rsa -A -J nataliakonyaeva@35.241.239.118 10.132.0.3

# Homework 4
## Данные для подключения
testapp_IP = 35.241.161.213
testapp_port = 9292

# Homework 5
- Написаны конфиг и файл переменных для создания образа reddit-base-xxx с предустановленными пакетами mongodb и ruby. запускается командой:
packer build -var-file=variables.json ubuntu16.json
- Файл variables.json занесен в .gitignore.

# Homework 6
- Определена input переменная для приватного ключа,использующегося в определении подключения для
провижинеров
- Определена input переменная для задания зоны
- Создан файл terraform.tfvars.example

# Homework 7
- Существующая структура импортирована в terraform
- Ресурс разбит на две ВМ: приложение и базу данных
- Конфигурация поделена на модули

# Homework 8
- Написан простой ansible playbook
- После выполнения команды 
ansible app -m command -a 'rm -rf ~/reddit'
и повторного выполнения ansible-playbook clone.yml значение change изменилось на 1, так как файловая структура на сервере была изменена

# Homework 9
- Написан playbook с одним сценарием
- Написан playbook с несколькими сценариями
- Один playbook разбит на 3: app.yml, db.yml, deploy.yml
- Изменены провижинеры в packer, пересобраны образы

# Homework 10
- Реализованы роли для развертывания приложения и бд
- Получен опыт использования роли из Ansible galaxy
- Настроено проксирование http трафика к приложению
- Добавлены пользователи

# Homework 11
- Установленs VirtualBox, Vagrant и Molecule
- Развернуто локальное окружение
- Роль db протестирована с помощью Molecule
- В плейбуках packer_app.yml и packer_db.yml использованы роли app и db
