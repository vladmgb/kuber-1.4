# Домашнее задание к занятию «Сетевое взаимодействие в K8S. Часть 1»


## Задание 1. Создать Deployment и обеспечить доступ к контейнерам приложения по разным портам из другого Pod внутри кластера
1. Создать Deployment приложения, состоящего из двух контейнеров (nginx и multitool), с количеством реплик 3 шт.

Создан [Deployment](https://github.com/vladmgb/kuber-1.4/blob/main/deployment141.yaml)

<img width="594" height="154" alt="image" src="https://github.com/user-attachments/assets/8e9d5fac-662a-4b3d-a851-d1385c641396" />
  
2. Создать Service, который обеспечит доступ внутри кластера до контейнеров приложения из п.1 по порту 9001 — nginx 80, по 9002 — multitool 8080.

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

   
5. Предоставить манифесты Deployment и Service в решении, а также скриншоты или вывод команды п.4.

   Указаны выше по тексту.

## Задание 2. Создать Service и обеспечить доступ к приложениям снаружи кластера
1. Создать отдельный Service приложения из Задания 1 с возможностью доступа снаружи кластера к nginx, используя тип NodePort.

Создан отдельный [Service](https://github.com/vladmgb/kuber-1.4/blob/main/service142.yaml)

<img width="648" height="91" alt="image" src="https://github.com/user-attachments/assets/9a0d1e38-6fca-4f22-92a2-e2e46295791b" />
   
2. Продемонстрировать доступ с помощью браузера или curl с локального компьютера.

Проверка доступа


<img width="936" height="109" alt="image" src="https://github.com/user-attachments/assets/eb7d1b63-9e6f-4416-9299-2d46de3c03a0" />


<img width="640" height="402" alt="image" src="https://github.com/user-attachments/assets/decd2e68-da0a-4d39-8357-9956825b289f" />

   
3. Предоставить манифест и Service в решении, а также скриншоты или вывод команды п.2.

    Указаны выше по тексту.
