# netology_terraform_intro_hw
Домашнее задание к занятию «Введение в Terraform»

# Задание 0
Версия Terraform и Docker (пришлось менять ```required_version``` в ```main.tf```):

# Задание 1
* Секретная информация хранится в файлах вида *.tfstate. Они в целом служат хранилищем информации о созданной инфраструктуре (создаётся после первого успешного ```terraform apply```) и важен для сверки результатов ```terraform plan``` с актуальным состоянием. Кроме того, тут есть комментарий вида ```# own secret vars store```.
* Значение в terraform.tfstate: ```resources.instances.attributes.result: BOg6ctZi6XsuEq5n```
* Ошибки: для ресурса docker_image указан только тип, без имени (тип зависит от провайдера, которым может выступать Hashicorp, другой вендор (в нашем случае - "docker_image") или коммьюнити Terraform), указала имя **nginx**, т.к. далее в фале встречается ```docker_image.nginx.image_id```. Также имя ресурса не может начинаться с цифры. Переименовала второй ресурс в **nginx1**. Помимо этого не была объявлена переменная(?) ```random_password.random_string_FAKE```.
* 
