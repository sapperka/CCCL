# Практическая работа номер 4 - Network Threat Hunter Training

1. Развертывание ВМ и запуск стенда:

![image](https://github.com/user-attachments/assets/6dd5e40e-3199-4d09-aa59-6889364990fb)
![image](https://github.com/user-attachments/assets/1083330a-18a9-445a-bb3b-9237a1c1fecc)
![image](https://github.com/user-attachments/assets/8b88ed82-d1bd-47e5-85d8-209a3f52ed41)

Выбор датасета для работы:

![image](https://github.com/user-attachments/assets/c8d7b9d5-6349-4acd-bf1e-7c907e52b2c3)

Стартовая страница после аутентификации и выбора датасета развернутого стенда:

![image](https://github.com/user-attachments/assets/67d8ab4c-633b-4a69-b743-fc2eb6d0a129)

Пример добавления адреса в safelist (skype.com):
Переходим в модуль beacons web и выбераем нужный узел:

![image](https://github.com/user-attachments/assets/e3c15209-82eb-496b-ba90-d38c8f8e295f)

Добавляем адреса в safelist:

![image](https://github.com/user-attachments/assets/c88ca40c-a878-4481-bc60-d4fbc9e5d356)

Проверка safelist на наличие добавленного ранее адреса:

![image](https://github.com/user-attachments/assets/abef6e88-9192-44a8-9f95-fe93840517d9)




2. Выполнение заданий из lab1:

Переход в нужную директорию и импорт логов:

![image](https://github.com/user-attachments/assets/24170907-bb37-4798-8a7b-e0715db51724)

Переключение на нужный датасет с загруженными ранее логами в web-итерфейсе:

![image](https://github.com/user-attachments/assets/4e4d1ee2-1c36-4c70-b2fa-f869cad1008f)

Стартовая страница с обнаруженными адресами и beacon score:

![image](https://github.com/user-attachments/assets/0f8463b8-2e3d-41b2-8951-5d1c3022b05f)

Переход в beacons web для анализа адресов:

![image](https://github.com/user-attachments/assets/aa0eee34-b280-493e-a176-56b3a082c2f4)

Проверка первого адреса:

![image](https://github.com/user-attachments/assets/92865545-7248-47e1-9f79-8831b851ba01)

Заключение по адресу: Адрес вызывает подозрения в связи с высокой активностью (3011 подключений), а также из-за стабильного и прямолинейного характера графика, отражающего зависимость количества подключений от времени. Отсутствие полного доменного имени хоста также может указывать на его потенциальную вредоносность.

Проверка еще нескольких адресов:

![image](https://github.com/user-attachments/assets/b26edb77-bcce-40ce-9b68-f86f8ad84f07)

![image](https://github.com/user-attachments/assets/8118e266-1627-4bb0-bc25-c3f68033493c)

Оба адреса относятся к сервисам microsoft и вызывают больше доверия. Так же они не обладают огромным количеством подключений. Из этого можно сделать вывод что данные адреса безопасны.

Проверка отображения добавленных ранее безопасных адресов в safelist:

![image](https://github.com/user-attachments/assets/a905aac5-85a3-442b-837b-1b1dde4fc8fd)

Переход к модулю long connections:

![image](https://github.com/user-attachments/assets/501418e9-eb3a-4aae-bf6a-ae45cf3e9f22)

Проверим адрес №1 на ресурсе VirusTotal

![image](https://github.com/user-attachments/assets/be0f2a28-a0a3-4583-a86b-406232b1a0da)

Адрес имеет на данном ресурсе отметку о вредоносности (1 вендор отметил этот адрес как вредоносный)

Проверим адрес №1 на ресурсе AbuselPDB

![image](https://github.com/user-attachments/assets/790e4776-4253-474b-bea0-cefed7942010)

Адрес имеет на данном ресурсе отметки о вредоносности (2 раза данный адрес был зарепорчен как вредоносный)

Проверим адрес №2 на ресурсе VirusTotal и AbuselPDB

![image](https://github.com/user-attachments/assets/88fc2804-860c-45cc-b144-372d492e8972)
![image](https://github.com/user-attachments/assets/415343fb-4c90-4002-8161-d3cec0decdae)

Адрес не имеет на данных ресурсе отметку о вредоносности

Вывод: соединения с IP-адресом 167.71.97.235 вызывают подозрения: зафиксировано 3011 подключений с высоким показателем beacons score, а также отсутствует поле «хост» в HTTP-заголовке. Кроме того, имеются данные о нескольких отчетах, указывающих на вредоносную активность, связанную с этим адресом. Остальные IP-адреса признаны безопасными, что подтверждается результатами проведенного анализа.

3. Выполнение заданий из lab2:

Переход в нужную директорию и импорт логов:

![image](https://github.com/user-attachments/assets/eb17f0c2-1873-4dec-8a98-9a3daccdff5a)

Переключение на нужный датасет с загруженными ранее логами в web-итерфейсе:

![image](https://github.com/user-attachments/assets/fbc0f502-522d-48f5-ba95-5850398f6e6d)

Стартовая страница:

![image](https://github.com/user-attachments/assets/a115d5f8-b7da-4ec1-ae6b-77d0d5e87075)

Переход в моудль DNS:

![image](https://github.com/user-attachments/assets/ab6a21ca-ace4-416c-a350-a0b998539a93)

Вывод: анализ указывает на попытку атаки с использованием протокола C2 через DNS. Вероятно, была задействована утилита dnscat2, созданная Роном Боузом, которая предназначена для организации командно-контрольных каналов (C&C) через DNS. Длина и имена поддоменов вызывают подозрения, так как они напоминают случайно сгенерированные (DGA). Кроме того, зафиксировано аномально высокое количество запросов к одному домену — 2074, что также свидетельствует о потенциально вредоносной активности.






4. Выполнение заданий из lab3:

Переход в нужную директорию и импорт логов:

![image](https://github.com/user-attachments/assets/32a815b3-8afe-4f5f-bd90-e9a0c93aab69)

Переключение на нужный датасет с загруженными ранее логами в web-итерфейсе:

![image](https://github.com/user-attachments/assets/9bf92a1d-c9ac-46c9-8666-5d95a96abae3)

![image](https://github.com/user-attachments/assets/4b0ef753-98c0-423d-b560-4bfccb3c06f3)

Переход в моудль beacons web:

![image](https://github.com/user-attachments/assets/2c98f2ef-084c-4c64-9c17-edf8c2e0cd61)

После анализа по примеру lab1 найден данный подозрительный адрес:

![image](https://github.com/user-attachments/assets/626536e5-d930-4688-be59-191ec50bc78e)


Проверка странного домена, похожего на skype с помощью ресурса VirusTotal:

![image](https://github.com/user-attachments/assets/37441016-5d0f-4775-a755-466de91b1e1d)

Адрес однозначно является вредоносным, что подтверждается большим количеством соединений и чрезвычайно стабильным графиком подключений в зависимости от времени. Дополнительная проверка домена также указывает на то, что это вредоносный ресурс.

Переход к модулю long connections:

![image](https://github.com/user-attachments/assets/dacbbdd2-b4b9-481a-88e1-028185094436)

Модуль показывает аналогичные данные и адреса с данными в lab1. Следовательно первый адрес вредоносен

Вывод: под подозрение в вредоносности попадает первый адрес. Необычное название хоста, явно сгенерированное по аналогии с доменом skype, вызывает вопросы. Сервис для проверки три раз отметил его вредоносность. Кроме того, о потенциальной угрозе свидетельствует аномально высокое количество соединений, зафиксированных для этого адреса.



5. 
