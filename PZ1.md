# Практическая работа №1. Сбор логов.

1. Создать 2 виртуальные машины на базе ОС Debian 12

![image](https://github.com/user-attachments/assets/deacdb65-6a4e-42f6-aaf9-d69b50a4be63)
![image](https://github.com/user-attachments/assets/568eeffc-2cae-4cf7-8356-0387d3abe60b)


2. Обеспечить между ними сетевой обмен:

Сеть на первой ВМ:

![image](https://github.com/user-attachments/assets/0a6b3a3e-b709-440e-813a-2f2efb9b8862)


Сеть на второй ВМ:

![image](https://github.com/user-attachments/assets/24784abe-e25d-4518-bd60-afc8af94034c)


Связаность между двумя ВМ:

![image](https://github.com/user-attachments/assets/b262c9d7-3e17-475e-be2e-113e4d5596ec)


3. Включить на 1й из ВМ передачу логов по протоколу rsyslog на 2ю ВМ

Настройка сервера:

Проверяем установку на 1й ВМ rsyslog:

![image](https://github.com/user-attachments/assets/d8964bcd-bb60-4164-b30c-58222dc75564)


Настраиваем rsyslog на работу по протоколу udp на 514 порту:

![image](https://github.com/user-attachments/assets/b9695d52-2b13-462d-a8d0-3b7eaa6e5153)

Настраиваем правила:

![image](https://github.com/user-attachments/assets/bdeef94f-193a-4456-a3e5-d7cd8970b537)


Настройка клиента:

4. Установить и настроить получение логов на сервер с использованием Loki

5. Установить и настроить получение логов на сервер с использованием Loki
