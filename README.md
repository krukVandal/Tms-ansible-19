# Задача 1: Управление конфигурацией ansible

1. Установил `ansible`в директории `/home/vandal/Ansible/` - установил в окружение

<img width="938" height="226" alt="image" src="https://github.com/user-attachments/assets/aa09b32f-bbf0-4156-9b51-4cbfe8947472" />

2. Сгенирировал `ssh_key` и скопировал его на вторую машину `ssh-copy-id`

<img width="1012" height="246" alt="image" src="https://github.com/user-attachments/assets/8be8a701-fda9-4e1a-830a-0eb2170895ac" />

3. 
 - Создал файл `hosts.txt` куда прописал хост удаленный, имя пользователя и ключ, запустил модуль `ping` получил `pong`
 - Создал файл `ansible.cfg` прописал туда инвентарь чтобы не указывать каждый раз файл `hosts.txt`, запустил пинг в компактном варианте и получил `pong`

<img width="1374" height="880" alt="image" src="https://github.com/user-attachments/assets/0932727f-c6b5-4687-9bb0-dbe6f6a4f652" />
