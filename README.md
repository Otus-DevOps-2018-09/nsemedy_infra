# nsemedy_infra
nsemedy Infra repository

# Homework 3
## Данные для подключения

bastion_IP = 35.241.239.118
someinternalhost_IP = 10.132.0.3

## Подключение к someinternalhost в одну команду
ProxyJump option

``` 
ssh -i .ssh/id_rsa -A -J nataliakonyaeva@35.241.239.118 10.132.0.3

# Homework 4
## Данные для подключения
testapp_IP = 35.195.143.50
testapp_port = 9292
