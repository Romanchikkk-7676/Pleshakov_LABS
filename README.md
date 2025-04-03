# Pleshakov_LABS
ЛАБОРАТОРНАЯ РАБОТА №1
Вписываем команду: `sudo yum install wget`
После этой команды нам выдаёт данный результат: 

![image](https://github.com/user-attachments/assets/cbce68f3-ab86-43de-ba8e-9ae198713fc8)

Таким обрахом выглядит конфигурационный файл : 

![image](https://github.com/user-attachments/assets/823cb8e7-9dd9-414c-94fd-f648e658aaa6)  

![image](https://github.com/user-attachments/assets/2f773f46-0856-48a6-9483-97e952588a46)

![image](https://github.com/user-attachments/assets/4a29581b-1b58-4a9e-8f1e-c82247c320d8)  

![image](https://github.com/user-attachments/assets/f41fb20b-52e2-4b49-a380-039b079d2812)  

![image](https://github.com/user-attachments/assets/312f6e86-201c-4231-b618-c9b554d37bc2)

После команды is not the sudoers file выдало ошибку: `is not in the sudoers file` , чтобы её исправить нужно сделать следущие действия: 
`su root `
`nano /etc/sudoers`
`user_name ALL=(ALL)  ALL`
Это будет выглядеть следующим образом: 

![image](https://github.com/user-attachments/assets/87e82803-eb44-4507-a357-59e6404253f4)

ЛАБОРАТОРНАЯ РАБОТА №2
Вводим команду: `sudo yum install curl` после этого нам должно показать следующий результат: 

![image](https://github.com/user-attachments/assets/d521358c-0019-47d2-8dc8-b84cc2e8e53c)

Далее вводим следущую команду: `sudo yum install docker-ce docker-ce-cli containerd.io` , после этой команды должен быть такой результат:

![image](https://github.com/user-attachments/assets/a172622a-2118-40ac-b81c-1818b16aa194)

Следущая команда выглядит таким образом, с помощью нее мы устанавливаем докер: `sudo wget -P /etc/yum.repos.d// download.docker.com/linux/centors/docker-ce.repo` , после ввода команды должен получиться такой результат: 

![image](https://github.com/user-attachments/assets/a075d0ff-c468-4a37-9337-d2de4b6d6780)

Далее нам нужно сделать два подтверждеия вписав `y` :

![image](https://github.com/user-attachments/assets/9e81c2dd-9d7f-4e15-bb78-c3c462076fc4)  

![image](https://github.com/user-attachments/assets/097da198-315a-4803-b965-51cda814b33a)

![image](https://github.com/user-attachments/assets/a74d3215-128f-473c-a8de-0273f660a089)

И последним этапом будет данная команда: `sudo sustemctl enable docker --now` и получается такой итог: 

![image](https://github.com/user-attachments/assets/edb3bb69-ce7c-4cd8-9c32-6a443aa74203)

# ЛАБОРАТОРНАЯ РАБОТА №3

Начальная команда в этой работе выглядит таким образом: `COMVER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d\" -f4)`

![image](https://github.com/user-attachments/assets/6d90e0ef-c47b-4512-b541-6e39cded1a1e)

Следующим шагом будет данная команда: `sudo curl -L "https://github.com/docker/compose/releases/download/$COMVER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose`. Эта команда скачивает и устанавливает Docker Compose.

![image](https://github.com/user-attachments/assets/15d11908-38ed-4397-9287-be36f449a39c)

После этого вводим данную команду: `sudo chmod +x /usr/bin/docker-compose. Эта команда делает файл` `docker-compose`, расположенный в директории `/usr/bin/`, исполняемым.

![image](https://github.com/user-attachments/assets/e817e4b6-d1d0-473b-828d-3c1f711cb932)

Далее вводим: docker-compose --version. Команда `docker-compose --version` отображает установленную версию Docker Compose.

![image](https://github.com/user-attachments/assets/342e0675-be83-4b9f-a41f-ac3747484fa0)

`git clone https://github.com/skl256/grafana_stack_for_docker.git`. Эта команда клонирует репозиторий `grafana_stack_for_docker` с GitHub на ваш локальный компьютер.

![image](https://github.com/user-attachments/assets/7f98568c-5106-4dcc-b831-16b367e8ec19)

cd grafana_stack_for_docker. Команда `cd grafana_stack_for_docker` меняет текущую рабочую директорию на `grafana_stack_for_docker`.

![image](https://github.com/user-attachments/assets/f35d4b8d-2729-4470-b683-fb388dbf7c13)

sudo mkdir -p /mnt/common_volume/swarm/grafana/config. Команда `sudo mkdir -p /mnt/common_volume/swarm/grafana/config` создает директорию (или несколько вложенных директорий) с указанным путем.

![image](https://github.com/user-attachments/assets/0c5537e8-c281-44b5-9b41-1688b6610278)

sudo mkdir -p /mnt/common_volume/grafana/{grafana-config,grafana-data,prometheus-data}. Эта команда создает несколько поддиректорий внутри `/mnt/common_volume/grafana/`, используя фигурные скобки для расширения имен. 

![image](https://github.com/user-attachments/assets/a050b40a-3f11-4a1b-b3f5-5440e35e94e7)

sudo mkdir -p /mnt/common_volume/grafana/{grafana-config,grafana-data,prometheus-data}. Эта команда меняет владельца и группу указанных директорий на текущего пользователя. 

![image](https://github.com/user-attachments/assets/6b493efe-e2e2-46e5-a4fc-05b02a581ca8)

touch /mnt/common_volume/grafana/grafana-config/grafana.ini. Эта команда создает пустой файл с именем `grafana.ini` по указанному пути.

![image](https://github.com/user-attachments/assets/8cb396a8-f9de-40ac-abe5-693dfd93efbf)

`cp config/* /mnt/common_volume/swarm/grafana/config/` . Команда `cp config/* /mnt/common_volume/swarm/grafana/config/` копирует все файлы и директории (за исключением скрытых, начинающихся с точки) из директории `config` в директорию `/mnt/common_volume/swarm/grafana/config/`.


![image](https://github.com/user-attachments/assets/43c3ea02-fb51-4129-8c0e-add6e32ac736)


`mv grafana.yaml docker-compose.yaml.` Команда `mv grafana.yaml docker-compose.yaml` переименовывает файл `grafana.yaml` в `docker-compose.yaml` в текущей рабочей директории. Если файл `docker-compose.yaml` уже существует, он будет перезаписан.


![image](https://github.com/user-attachments/assets/66ce9fca-14cc-4e95-8c22-6a1369f8ef4a) 


sudo docker compose up -d. Команда `sudo docker compose up -d` запускает контейнеры, описанные в файле `docker-compose.yaml` в detached режиме (в фоне).


![image](https://github.com/user-attachments/assets/bb05b3c4-bef5-4589-a481-3df0d46c020b)   


![image](https://github.com/user-attachments/assets/51ff6d94-cae1-4343-a4f8-ed24349d79da)

# ЛАБОРАТОРНАЯ РАБОТА №4
ключ `-d` означает, что мы вошли в detached mode (фоновый режим)

Запуск контейнеров Docker
`sudo docker compose up -d`

![image](https://github.com/user-attachments/assets/58db6358-b995-4730-b5bf-ddae0d5c778e)


Остановка контейнеров Docker
`sudo docker compose stop`

![image](https://github.com/user-attachments/assets/411e3b32-7b15-4562-b8f7-826dee36f0d8)


Удаление контейнеров Docker
`sudo docker compose down`

![image](https://github.com/user-attachments/assets/279e9b6a-2b78-4ec5-baa4-df13bd8c4dc1)


Показывает статус всех контейнеров
`sudo docker compose ps`

![image](https://github.com/user-attachments/assets/ef1e0e77-9583-4f6c-8260-f351f5745c00)

Клонирую репозиторий 
`git clone https://github.com/Romanchikkk-7676/Pleshakov_LABS.git`

![image](https://github.com/user-attachments/assets/8a0127ae-a898-4880-b8e9-d60658074877)

Сделал Бекап файла `docker-compose.yaml`

и переместил файлы в корень папки
`mv Pleshakov_LABS/prometeus.yaml ./`
`mv Pleshakov_LABS/docker-compose.yaml ./`

![image](https://github.com/user-attachments/assets/240d3829-3199-41d9-aedf-2929e26266f2)


# ЛАБОРАТОРНАЯ РАБОТА №5

Файл перемещаем `prometeus.yaml` -> `/mnt/common_volume/swarm/grafana/config/`
`sudo mv prometeus.yaml /mnt/common_volume/swarm/grafana/config/`

Сделал Бекап файла `prometeus.yaml` в `/mnt/common_volume/swarm/grafana/config/`

Нужно переименовываю файл в `prometheus.yaml`

Поднял Docker:
`sudo docker compose up -d`

Зашел в него через браузер:
`localhost:3000`

Пароль и логин
admin:admin

1. Создание нового источника данных в Grafana
  1. Перешел в `Home -> Connections -> Data sources`.
  2. Нажал `Add data source`.
  3. В открывшемся списке выберал `Prometheus`.
  4. Настройте параметры подключения:
    - Connection: `http://prometheus:9090`
    - Authentication: Включите Basic authentication.
  5. После настройки нажал `Save & Test`, чтобы проверить подключение.

![image](https://github.com/user-attachments/assets/678bc0da-5504-4b96-b0ce-1c8d1a587535)

2. Перешел в `Home -> Dashboards -> Import dashboard`.
  1. В поле ввода указал ID шаблона: 1860.
  2. Нажал `Load`.
  3. В появившемся окне:
    - Выберал источник данных `Prometheus`.
  4. Нажал `Import`.

![image](https://github.com/user-attachments/assets/e88f8ed7-88b8-475f-a441-599c27c38a19)

![image](https://github.com/user-attachments/assets/847cda23-3b2a-4f4f-92b6-d29f86b6f705)


Рузультат:

![image](https://github.com/user-attachments/assets/deb04a08-d785-44ee-af57-5a51319ef6fa)


# ЛАБОРАТОРНАЯ РАБОТА №6

В терминал ввел:
`echo -e "# TYPE light_metric1 gauge\nlight_metric1 0" | curl --data-binary @- http://localhost:8428/api/v1/import/prometheus` - она отправляет бинарные данные

![image](https://github.com/user-attachments/assets/bcb41b8a-fe78-4d7a-9d61-2c72a5498c87)

1. Перешел в `Home -> Connections -> Data sources`.
2. Нажал `Add data source`.
3. В открывшемся списке выберал `Prometheus`.
4. Настройте параметры подключения:
  - Переминовываем: `vica 1`
  - Connection: `http://victoriametrics:8428`
5. После настройки нажал `Save & Test`, чтобы проверить подключение.

![image](https://github.com/user-attachments/assets/a261d77c-6835-42ba-8116-585ac96b97bc)

Ввел в `code` `light_metric1`  со значением `0`

![image](https://github.com/user-attachments/assets/10bbf270-2e78-4651-8cee-41689d20d332)

После это ввел в команду `echo -e "# TYPE light_metric1 gauge\nlight_metric1 0" | curl --data-binary @- http://localhost:8428/api/v1/import/prometheus` вместо `0` написал свои числа, у меня это: `0` `66` `33`

Получается вот такой график:

![image](https://github.com/user-attachments/assets/776f1cd8-f92c-414f-b157-0e1e2cf53bbd)


Cправа в поиске написал `Connect null values` и нажал `always` 

Что эта функция делает:
 - Она соединяет график линиями

![image](https://github.com/user-attachments/assets/5b2ddb6e-74ff-4055-9977-a5ed0516c746)

