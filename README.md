# Pleshakov_LABS
ЛАБОРАТОРНАЯ РАБОТА №1
Вписываем команду: sudo yum install wget
После этой команды нам выдаёт данный результат: ![image](https://github.com/user-attachments/assets/cbce68f3-ab86-43de-ba8e-9ae198713fc8)
Таким обрахом выглядит конфигурационный файл : ![image](https://github.com/user-attachments/assets/823cb8e7-9dd9-414c-94fd-f648e658aaa6)  ![image](https://github.com/user-attachments/assets/2f773f46-0856-48a6-9483-97e952588a46)
![image](https://github.com/user-attachments/assets/4a29581b-1b58-4a9e-8f1e-c82247c320d8)  ![image](https://github.com/user-attachments/assets/f41fb20b-52e2-4b49-a380-039b079d2812)  ![image](https://github.com/user-attachments/assets/312f6e86-201c-4231-b618-c9b554d37bc2)
После команды is not the sudoers file выдало ошибку: is not in the sudoers file , чтобы её исправить нужно сделать следущие действия: 
su root 
nano /etc/sudoers
user_name ALL=(ALL)  ALL
Это будет выглядеть следующим образом: ![image](https://github.com/user-attachments/assets/87e82803-eb44-4507-a357-59e6404253f4)

ЛАБОРАТОРНАЯ РАБОТА №2
Вводим команду: sudo yum install curl после этого нам должно показать следующий результат: ![image](https://github.com/user-attachments/assets/d521358c-0019-47d2-8dc8-b84cc2e8e53c)
Далее вводим следущую команду: sudo yum install docker-ce docker-ce-cli containerd.io , после этой команды должен быть такой результат: ![image](https://github.com/user-attachments/assets/a172622a-2118-40ac-b81c-1818b16aa194)
Следущая команда выглядит таким образом, с помощью нее мы устанавливаем докер: sudo wget -P /etc/yum.repos.d// download.docker.com/linux/centors/docker-ce.repo , после ввода команды должен получиться такой результат: ![image](https://github.com/user-attachments/assets/a075d0ff-c468-4a37-9337-d2de4b6d6780)
Далее нам нужно сделать два подтверждеия вписав y : ![image](https://github.com/user-attachments/assets/9e81c2dd-9d7f-4e15-bb78-c3c462076fc4)  ![image](https://github.com/user-attachments/assets/097da198-315a-4803-b965-51cda814b33a)
![image](https://github.com/user-attachments/assets/a74d3215-128f-473c-a8de-0273f660a089)
И последним этапом будет данная команда: sudo sustemctl enable docker --now и получается такой итог: ![image](https://github.com/user-attachments/assets/edb3bb69-ce7c-4cd8-9c32-6a443aa74203)







