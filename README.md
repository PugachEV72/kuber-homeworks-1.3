# Домашнее задание к занятию `«Запуск приложений в K8S»` - Пугач Евгений.


---

## `Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod`

1. Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
2. После запуска увеличить количество реплик работающего приложения до 2.
3. Продемонстрировать количество подов до и после масштабирования.

### Ответ:

[DEPLOYMENT.YAML](https://github.com/PugachEV72/kuber-homeworks-1.3/blob/main/deployment.yaml)

![Скриншот 1](https://github.com/PugachEV72/Images/blob/master/2024-04-21_22-44-21.png)

![Скриншот 2](https://github.com/PugachEV72/Images/blob/master/2024-04-21_22-46-22.png)

![Скриншот 3](https://github.com/PugachEV72/Images/blob/master/2024-04-21_22-47-44.png)

---

4. Создать Service, который обеспечит доступ до реплик приложений из п.1.

### Ответ:

[NGINX-SERVICE.YAML](https://github.com/PugachEV72/kuber-homeworks-1.3/blob/main/nginx-service.yaml)

![Скриншот 4](https://github.com/PugachEV72/Images/blob/master/2024-04-21_23-01-54.png)

---

5. Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.

### Ответ:

![Скриншот 5](https://github.com/PugachEV72/Images/blob/master/2024-04-21_23-07-15.png)

---

## `Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий`

1. Создать Deployment приложения nginx и обеспечить старт контейнера только после того, как будет запущен сервис этого приложения.
2. Убедиться, что nginx не стартует. В качестве Init-контейнера взять busybox.
3. Создать и запустить Service. Убедиться, что Init запустился.
4. Продемонстрировать состояние пода до и после запуска сервиса.

### Ответ:

[DEPLOYMENT-WAIT.YAML](https://github.com/PugachEV72/kuber-homeworks-1.3/blob/main/deployment-wait.yaml)

[NGINX-SERVICE.YAML](https://github.com/PugachEV72/kuber-homeworks-1.3/blob/main/nginx-service.yaml)

![Скриншот 6](https://github.com/PugachEV72/Images/blob/master/2024-04-21_23-26-49.png)

![Скриншот 7](https://github.com/PugachEV72/Images/blob/master/2024-04-21_23-29-40.png)

---

