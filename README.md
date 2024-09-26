# Домашнее задание к занятию "`Система сбора логов Elastic Stack`" - `Макаров Денис`


## Задание 1

Вам необходимо поднять в докере и связать между собой:

- elasticsearch (hot и warm ноды);
- logstash;
- kibana;
- filebeat.

Logstash следует сконфигурировать для приёма по tcp json-сообщений.

Filebeat следует сконфигурировать для отправки логов docker вашей системы в logstash.

В директории [help](./help) находится манифест docker-compose и конфигурации filebeat/logstash для быстрого 
выполнения этого задания.

Результатом выполнения задания должны быть:

- скриншот `docker ps` через 5 минут после старта всех контейнеров (их должно быть 5);

![01](https://github.com/user-attachments/assets/f68a1411-d563-4e73-9511-4c3652d70bc3)
- скриншот интерфейса kibana;
![02](https://github.com/user-attachments/assets/81cbaf90-2ba5-4df7-8c02-02e7fa3be6b0)
- docker-compose манифест (если вы не использовали директорию help);
- ваши yml-конфигурации для стека (если вы не использовали директорию help).

## Задание 2

Перейдите в меню [создания index-patterns  в kibana](http://localhost:5601/app/management/kibana/indexPatterns/create) и создайте несколько index-patterns из имеющихся.
![03](https://github.com/user-attachments/assets/70522f64-e4b5-4ffb-a8fa-076dcddbb748)
Перейдите в меню просмотра логов в kibana (Discover) и самостоятельно изучите, как отображаются логи и как производить поиск по логам.
![04](https://github.com/user-attachments/assets/1efcbafd-676c-4914-9b9c-1212857a70a8)

![image](https://github.com/user-attachments/assets/e38ff135-c015-4179-a5bf-6a1673ff8732)

В манифесте директории help также приведенно dummy-приложение, которое генерирует рандомные события в stdout-контейнера.
Эти логи должны порождать индекс logstash-* в elasticsearch. Если этого индекса нет — воспользуйтесь советами и источниками из раздела «Дополнительные ссылки» этого задания.
 
