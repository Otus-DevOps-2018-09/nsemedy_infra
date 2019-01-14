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

