# Практическая работа номер 3 - WAZUH

1. Результат установки и настройки 2 ВМ (Сервер и Клиент):

![image](https://github.com/user-attachments/assets/4a674de9-e129-426c-8771-a3edbe833e75)
![image](https://github.com/user-attachments/assets/d85efb33-8f2f-4b81-8b4b-8c156ff1a9ce)


2. Проверка связи между двумя ВМ:

![image](https://github.com/user-attachments/assets/dfdeda1b-9150-4eeb-a91c-e8eac897c72b)
![image](https://github.com/user-attachments/assets/0265179e-3bf5-47d5-ae15-f466b905b367)

Пропингуем две ВМ между собой:


![image](https://github.com/user-attachments/assets/aae87cee-954d-4642-b2d7-6a19b2e92174)
![image](https://github.com/user-attachments/assets/e8316e1f-3c60-4b00-b6e5-6e3dcafcd799)


3. Установка Wazuh-сервера на серверной ВМ:

![image](https://github.com/user-attachments/assets/967d4fc4-6dd8-4b4b-b41f-521e6dae61f5)
![image](https://github.com/user-attachments/assets/c61517ed-ea37-4126-8174-985f6d182328)
![image](https://github.com/user-attachments/assets/9578475e-7aa2-4124-8d12-c6e28100a95e)

4. Перейдем к установке агента на клиентской ВМ:

Сгенерируем команды в web-интерфейсе Wazuh:

![image](https://github.com/user-attachments/assets/e54089b7-65b9-4eab-99ff-796f11f8d04d)
![image](https://github.com/user-attachments/assets/ba5fad3a-2e78-472b-b5dc-e332807de9bc)
![image](https://github.com/user-attachments/assets/d9488cf8-049e-4e81-a39d-60e2fbc9b9f4)

Выполним команды на клиентской ВМ:

![image](https://github.com/user-attachments/assets/d4872781-c7c7-477f-82d1-2b7320bc8a9c)


5. Проверка отображения нового агента в web-интерфейсе Wazuh

![image](https://github.com/user-attachments/assets/40e04f83-560f-4095-986d-9e5ac2485118)

Отбразим детектор уязвимостей для конкретного агента:

![image](https://github.com/user-attachments/assets/8933954d-ab8b-4dae-88d9-e4692b975433)


6. Проверим активность проверки целостности файлов:

![image](https://github.com/user-attachments/assets/9ca992c2-ef4e-46d7-9918-7497a6eb437b)


7. Настроим выявление уязвимостей:

![image](https://github.com/user-attachments/assets/1e4b2549-816f-43e0-8335-d4c8e7b8838b)


8. Настроим выявление скрытых процессов:

Устанавливаем нужные пакеты и добавляем настройки:

![image](https://github.com/user-attachments/assets/f0279109-8ace-4c9e-92c6-69046b81d6e9)
![image](https://github.com/user-attachments/assets/075978fe-baf6-40f7-8ff3-a1871a285af5)


9. Настроим выявление SQL-иньекций:

Устанавливаем нужные пакеты и добавляем настройки:

![image](https://github.com/user-attachments/assets/2d90fdd4-1112-4f5e-8f2e-bf5ccdf9d9c3)
![image](https://github.com/user-attachments/assets/58fd6aef-d02b-41f3-ac45-223a7765700a)

10. Настроим выявление web shell attack:

![image](https://github.com/user-attachments/assets/6b10f2cf-2f92-4cd6-95c0-1aa907b03b61)

11. Проверка обнаружения атаки:

Проводим несколько атак:

![image](https://github.com/user-attachments/assets/76bbb17d-c962-4066-9f6f-004e1f1a5eb1)

![image](https://github.com/user-attachments/assets/6860fa9d-7d84-48af-85e8-9449cc05514f)
![image](https://github.com/user-attachments/assets/d3a7a331-7d2e-47d7-9470-92a5a20c0ee2)



