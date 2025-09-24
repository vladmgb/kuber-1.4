# Домашнее задание к занятию «Сетевое взаимодействие в Kubernetes»


## Задание 1: Настройка Service (ClusterIP и NodePort)
1. Создать Deployment с двумя контейнерами

Создан [Deployment](https://github.com/vladmgb/kuber-1.4/blob/main/deployment141.yaml)

<img width="594" height="154" alt="image" src="https://github.com/user-attachments/assets/8e9d5fac-662a-4b3d-a851-d1385c641396" />
  
2. Создать Service типа ClusterIP

Создан [Service](https://github.com/vladmgb/kuber-1.4/blob/main/service141.yaml)

<img width="652" height="82" alt="image" src="https://github.com/user-attachments/assets/8c0873bb-0424-4a89-bde4-1d82d5f2d8ee" />


3. Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложения из п.1 по разным портам в разные контейнеры.

Создан отдельный [Pod](https://github.com/vladmgb/kuber-1.4/blob/main/pod141.yaml) 

<img width="557" height="106" alt="image" src="https://github.com/user-attachments/assets/fcba6e86-8fb0-4ef6-a4ff-b451227736b1" />

Проверка доступов

<img width="1139" height="435" alt="image" src="https://github.com/user-attachments/assets/997140da-e14c-4623-ab01-d0c0c475c84e" />

 
4. Продемонстрировать доступ с помощью curl по доменному имени сервиса.

Проверка доступа по FQDN сервиса

<img width="1136" height="430" alt="image" src="https://github.com/user-attachments/assets/d97d7982-0b67-48a3-862a-dee6f39f51c4" />


5. Создать Service типа NodePort для доступа к nginx снаружи

Создан отдельный [Service](https://github.com/vladmgb/kuber-1.4/blob/main/service142.yaml)

<img width="648" height="91" alt="image" src="https://github.com/user-attachments/assets/9a0d1e38-6fca-4f22-92a2-e2e46295791b" />
   
6. Проверить доступ с локального компьютера

Проверка доступа

<img width="936" height="109" alt="image" src="https://github.com/user-attachments/assets/eb7d1b63-9e6f-4416-9299-2d46de3c03a0" />


<img width="640" height="402" alt="image" src="https://github.com/user-attachments/assets/decd2e68-da0a-4d39-8357-9956825b289f" />

   
## Задание 2: Настройка Ingress

1. Развернуть два Deployment:

Манифесты Deployment - [frontend](https://github.com/vladmgb/kuber-1.4/blob/main/deployment-frontend.yaml), [backend](https://github.com/vladmgb/kuber-1.4/blob/main/deployment-backend.yaml)

Deployment созданы.

<img width="513" height="113" alt="image" src="https://github.com/user-attachments/assets/ece7ffbd-13ca-4ff3-b885-636332d5592b" />


2. Создать Service для каждого приложения.

Манифесты Service - [frontend](https://github.com/vladmgb/kuber-1.4/blob/main/service-frontend.yaml), [backend](https://github.com/vladmgb/kuber-1.4/blob/main/deployment-backend.yaml)

Service созданы.

   <img width="698" height="152" alt="image" src="https://github.com/user-attachments/assets/79ffc5cc-44ac-4d2f-bb42-5bc8421b7eb1" />


3. Включить Ingress-контроллер:

   Включен.

4. Создать Ingress, который:

Манифест [Ingress](https://github.com/vladmgb/kuber-1.4/blob/main/ingress.yaml)

Создан Ingress

<img width="455" height="105" alt="image" src="https://github.com/user-attachments/assets/4b50f06e-b64e-4317-a0b7-5460833c8b36" />


5. Проверить доступность:
   

 <img width="1038" height="470" alt="image" src="https://github.com/user-attachments/assets/239e723b-4d8b-447c-a003-ae8c37798a8a" />
