# Практика №1 по предмету АЗСИИ - Аггрегация и сбор логов
Выполнил(а) студент Кузина А.С.
## **1. Начнем с создания 2 виртуальных машин на базе ОС Debian 12 и обеспечим между ними сетевой обмен посредством реализации сетевого моста (В качестве программы виртуализации использован VirtualBOX)**

![image](Screenshots/1.png)

![image](Screenshots/2.png)

![image](Screenshots/3.png)

## **2. Настроим и обеспечим на 1-ой ВМ (сервер) передачу логов по протоколу rsyslog на 2-ую ВМ (клиент)**

### *Устанавим и настроим rsyslog на сервере и клиенте*

![image](Screenshots/4.png)

### *Проверим работоспособность rsyslog на сервере и клиенте*

![image](Screenshots/5.png)

### *Включим UDP и TCP соединения*

![image](Screenshots/6.png)

### *Установим правила на сервере*

![image](Screenshots/7.png)

### *Установим правила на клиенте*

![image](Screenshots/8.png)

### *Проверим получения логов на сервере*

![image](Screenshots/9.png)

![image](Screenshots/10.png)

## **3. Перейдем к установке и настройке получения логов на сервер с использованием Loki**

### *Установим и отредактируем docker compose файл на сервере*

   ![image](Screenshots/11.png)
   
   ![image](Screenshots/12.png)

### *Запустим Loki*

![image](Screenshots/13.png)

### *Отредактируем promtail-config на клиенте*

![image](Screenshots/14.png)

### *Отредактируем docker compose файл для promtail*

![image](Screenshots/15.png)

### *Запустим promtail на клиенте*

![image](Screenshots/16.png)

### *Просмотрим логи клиента в Grafana Loki*

   ![image](Screenshots/17.png)

   ![image](Screenshots/18.png)

## **4. Перейдем к настройке получения логов на сервере с использованием Signoz**

Установка Signoze выполнена согласно информации с источника - https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose

Установка sample-nodejs-app выполнена согласно информации с источника - https://github.com/SigNoz/sample-nodejs-app/

### *4.1 Запустим Signoz*



### *Отредактируем конфигурации на клиенте для отправки данных в Signoz*



### *Запустим клиентское приложение sample-nodejs-app*



### *Проверим получение логов в Signoz*
