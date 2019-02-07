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
Написаны конфиг и файл переменных для создания образа reddit-base-xxx с предустановленными пакетами mongodb и ruby. запускается командой:
packer build -var-file=variables.json ubuntu16.json
Файл variables.json занесен в .gitignore.

# Homework 6
Определена input переменная для приватного ключа,использующегося в определении подключения для
провижинеров
Определена input переменная для задания зоны
Создан файл terraform.tfvars.example

# Homework 7
Существующая структура импортирована в terraform
Ресурс разбит на две ВМ: приложение и базу данных
Конфигурация поделена на модули

# Homework 8
Написан простой ansible playbook
После выполнения команды 
ansible app -m command -a 'rm -rf ~/reddit'
и повторного выполнения ansible-playbook clone.yml значение change изменилось на 1, так как файловая структура на сервере была изменена