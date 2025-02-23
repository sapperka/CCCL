# Практическая работа №1. Сбор логов.

1. Создать 2 виртуальные машины на базе ОС Debian 12

![image](https://github.com/user-attachments/assets/9d410015-1423-44f7-978b-10e0cfa791cd)
![image](https://github.com/user-attachments/assets/e0584e60-f14b-43fc-b253-ddffa3c58a55)

2. Обеспечить между ними сетевой обмен:

![image](https://github.com/user-attachments/assets/3792441e-49c0-4117-b1b0-843bddcd40d9)
![image](https://github.com/user-attachments/assets/3a6763b4-b422-419f-b2d6-592b5b8e4845)


Связаность между двумя ВМ:

![image](https://github.com/user-attachments/assets/618e479d-71f8-405d-9f05-de452bce64a2)


3. Включить на 1й из ВМ передачу логов по протоколу rsyslog на 2ю ВМ

Устанавливаем и настраиваем rsyslog на сервере и клиенте:

![image](https://github.com/user-attachments/assets/7b7253aa-a545-43a8-923f-44385b91d87d)
![image](https://github.com/user-attachments/assets/cef83502-9488-44ea-a356-ccb27d82363a)

Проверяем работоспособность rsyslog на сервере и клиенте:

![image](https://github.com/user-attachments/assets/e5c875fd-77f4-4fc0-8813-00584787f14d)
![image](https://github.com/user-attachments/assets/7969f7c1-33bf-488f-8ded-955502d78a1d)

Включаем UDP и TCP соединение:

![image](https://github.com/user-attachments/assets/239ee584-570f-4511-8cc7-c4ffc5c070b4)
![image](https://github.com/user-attachments/assets/504b226e-3e11-4d2f-886e-f2f86b90d5f3)

Устанавливаем правила на сервере:

![image](https://github.com/user-attachments/assets/cd16806a-65d0-4eab-9ec1-157241698e0e)
![image](https://github.com/user-attachments/assets/4e26f849-b672-404e-9fc2-cb4fb2ea6b39)

Проверяем получения логов на сервере:

![image](https://github.com/user-attachments/assets/678dcb55-23be-4919-b4e9-819f14c8dab8)
![image](https://github.com/user-attachments/assets/754a3a45-bf2f-4b0f-b788-828db3a64e7b)

4. Установить и настроить получение логов на сервер с использованием Loki

Устанавливаем и редактируем compose-файл на сервере:

![image](https://github.com/user-attachments/assets/89b61210-eb3d-478c-9dc9-1d52f7f0d773)
![image](https://github.com/user-attachments/assets/1dc4ac4a-96fe-4f3d-90d6-631ccdf7448f)

Запускаем Loki:

![image](https://github.com/user-attachments/assets/81021c34-ab97-413d-af9e-9aaa8b013f41)

Редактируем promtail на клиенте:

![image](https://github.com/user-attachments/assets/9962d308-c709-41ed-86b8-a331bb3157e7)

Редактируем compose-файл для promtail

![image](https://github.com/user-attachments/assets/02e83fd2-4dc7-4d0d-937f-9470735dbba7)

Запускаем promtail на клиенте:

![image](https://github.com/user-attachments/assets/a60992c6-7d97-488e-ac1c-c06d4253c77d)

Просматриваем логи клиента в Grafana Loki:

![image](https://github.com/user-attachments/assets/30763632-e7f8-4c26-949d-e21f2ef58b46)
![image](https://github.com/user-attachments/assets/ce7564c3-5ec6-455a-836d-97c4179a353e)



5. Установить и настроить получение логов на сервер с использованием Loki

Установка Signoz по инструкции с сайта: https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose

Запускаем Signoz:

![image](https://github.com/user-attachments/assets/8ba8d4ab-2d59-4974-ab55-ec5a0ec2ffa0)
![image](https://github.com/user-attachments/assets/44106ee4-ecbb-4cba-a25f-7b8a0ac79bd8)

Редактируем конфигурации на клиенте для отправки данных в Signoz:

Установка приложения sample-nodejs-app согласно инструкции с сайта: https://github.com/SigNoz/sample-nodejs-app/

![image](https://github.com/user-attachments/assets/cebb2e3a-c0cf-4460-b401-95f9602e3129)

Запускаем клиентское приложение:

![image](https://github.com/user-attachments/assets/4402f335-2859-441f-a555-b72819a06353)

Проверяем получение логов в Signoz:

![image](https://github.com/user-attachments/assets/389915fc-55be-4ae2-ac3f-4fba715194b3)

