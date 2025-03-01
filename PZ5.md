# Практическая работа номер 5 - Threat Hunting

1. Результат развертывания ВМ для выполнения работы:

![image](https://github.com/user-attachments/assets/d10e8f6f-eedd-44cb-a102-794437c3f76d)
![image](https://github.com/user-attachments/assets/87b8c6eb-3811-4461-be10-2d4fbebb5add)
![image](https://github.com/user-attachments/assets/e6467ac3-8041-4521-9d13-b8b4b7621369)

Проверка доступности:

![image](https://github.com/user-attachments/assets/a7f49458-b06e-4f04-bd42-4015b32f24af)
![image](https://github.com/user-attachments/assets/866bb5d1-fc1c-440f-a981-37d03b6b32d3)


2. Установка на серверную ВМ Сервера Wazuh:

![image](https://github.com/user-attachments/assets/c8c3905c-4fb4-4a9a-809a-374fcc98fa24)
![image](https://github.com/user-attachments/assets/ff98e11c-7a5f-4c9e-8382-d8533a0b234f)



3. Установка агента на клиентскую ВМ:

![image](https://github.com/user-attachments/assets/8986ce6f-f70d-4c01-bd5b-040b3dee7a77)
![image](https://github.com/user-attachments/assets/e1a9b880-5d31-4532-8d3e-1995c8a88453)

Проверка отображения подключенного агента на Wazuh-сервере:

![image](https://github.com/user-attachments/assets/47732ca0-2e8a-4f4c-9802-3d0e0a16a6f4)


4. Установка Suricata IDS на клиентскую ВМ:

![image](https://github.com/user-attachments/assets/ef89a1da-a377-4618-a868-9da4ed57b396)

Установка набора правил для Suricata:

![image](https://github.com/user-attachments/assets/14929886-6d64-4166-b6c4-42d892728be5)

Настройка конфигурации Suricata IDS:

![image](https://github.com/user-attachments/assets/5f5df923-1053-41ef-9381-7fb1cc3e1683)

![image](https://github.com/user-attachments/assets/88d51334-9c6b-4544-a4ff-739e25e4c995)

![image](https://github.com/user-attachments/assets/5607ef86-6148-42f6-9501-cc7d4088dd10)


Настройка сбора логов и передачи в Wazuh-сервер:

![image](https://github.com/user-attachments/assets/ee27d3f3-07f6-415d-9ffb-d69fca40d70d)


Проверка логов Suricata на Wazuh-сервере:

![image](https://github.com/user-attachments/assets/9d730217-e22f-4025-af96-68d1f9b7d5f3)



5. Установка ThreatHuntingTools утилиты YARA для передачи обнаружений в Wazuh:

Процесс установки YARA на клиентскую ВМ:

![image](https://github.com/user-attachments/assets/fd1869ff-dae5-4257-8c5f-c2d0afb4e662)
![image](https://github.com/user-attachments/assets/5430da87-6b87-4676-ae15-aa3de547440d)

Проверка установки YARA:

![image](https://github.com/user-attachments/assets/723eadae-4897-4b2a-8411-c2e7780974af)

Установка набора правил для корректных обнаружений YARA:

![image](https://github.com/user-attachments/assets/b129d044-df1d-49aa-a48c-683887787000)

Создание скрипта yara.sh для активного обнаружения YARA:

![image](https://github.com/user-attachments/assets/8b8105bd-4f2a-4101-a6a4-bab0226da66f)

Редактирование конфигурационного файла Wazuh-agent для работы с YARA:

![image](https://github.com/user-attachments/assets/d797e165-1de5-4702-992d-041523133b91)

Создание локальных правил и кастомного декодера для YARA:

![image](https://github.com/user-attachments/assets/3d1f12a5-a56b-449e-b0ec-2230afabc1ff)
![image](https://github.com/user-attachments/assets/7bfff9c9-0aac-4e50-b007-cd5476a79356)

Редактирование конфигурационного файла Wazuh для работы с YARA:

![image](https://github.com/user-attachments/assets/39151b40-eadb-4d96-8683-b34f61041a46)

На Клиентской ВМ выполним имитацию вредоносных действий:

![image](https://github.com/user-attachments/assets/8b70f6d2-08e9-48b5-ad30-4cc5c55e787c)

В Wazuh на Серверной ВМ видим результат обнаружения угроз:

![image](https://github.com/user-attachments/assets/5dc9fb75-ba61-426a-8f95-dbf1de56b3fb)


6. Установка ScanerTools утилиты OpenVAS:

Установка докера для дальнейшей установки OpenVAS на Клиенствкую ВМ:

![image](https://github.com/user-attachments/assets/262b2988-a618-47af-9b86-e8042373d201)

Процесс установки OpenVAS на Клиенствкую ВМ:

![image](https://github.com/user-attachments/assets/cc4f6b7e-545e-45a7-ac42-f2018972209f)

Запуск web-интерфейса OpenVAS:

![image](https://github.com/user-attachments/assets/ff2a3e67-575b-4e80-b79f-204796cbfd26)
![image](https://github.com/user-attachments/assets/f1095096-25b8-44c7-b38f-6b4469dc3cb9)

Проверка конфигураций для сканирования и их обновление:

![image](https://github.com/user-attachments/assets/4f8937f3-a671-4ac3-86f1-5671a7af8a99)
![image](https://github.com/user-attachments/assets/c1491a5d-1334-49c0-9a00-6ea3e4467137)

Запуск сканирования Клиентской ВМ по IP адресу:

![image](https://github.com/user-attachments/assets/055c5768-755f-4d08-9a8e-d770a5006e93)


Отображение нового задания на сканирование в OpenVAS:

![image](https://github.com/user-attachments/assets/ead504ec-f9a9-4ec1-8b58-de4f48d80300)

Результаты проведенного сканирования:

![image](https://github.com/user-attachments/assets/41a2842c-a962-4b21-9e26-a17dbf94c912)
![image](https://github.com/user-attachments/assets/edfe73b2-99b0-45d5-93e6-2b7b7e8b4d28)
![image](https://github.com/user-attachments/assets/ea7b2bc7-c8d5-4538-9c95-57ad550033db)
![image](https://github.com/user-attachments/assets/d4557efa-6625-4069-aff4-ae2b9993d630)











