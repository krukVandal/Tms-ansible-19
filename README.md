# Задача 1: Управление конфигурацией ansible

1. Установил `ansible`в директории `/home/vandal/Ansible/` - установил в окружение

<img width="938" height="226" alt="image" src="https://github.com/user-attachments/assets/aa09b32f-bbf0-4156-9b51-4cbfe8947472" />

2. Сгенирировал `ssh_key` и скопировал его на вторую машину `ssh-copy-id`

<img width="1012" height="246" alt="image" src="https://github.com/user-attachments/assets/8be8a701-fda9-4e1a-830a-0eb2170895ac" />

3. 
 - Создал файл `hosts.txt` куда прописал хост удаленный, имя пользователя и ключ, запустил модуль `ping` получил `pong`
 - Создал файл `ansible.cfg` прописал туда инвентарь чтобы не указывать каждый раз файл `hosts.txt`, запустил пинг в компактном варианте и получил `pong`

<img width="1374" height="880" alt="image" src="https://github.com/user-attachments/assets/0932727f-c6b5-4687-9bb0-dbe6f6a4f652" />

# Задача 2: Написать плейбуки

1. Написать плейбук, который создает системного пользователя с именем appuser с домашней директорией (/home/appuser) и оболочкой /bin/bash



2. Написать плейбук, который копирует публичный SSH-ключ с управляющей машины (files/appuser.pub) в файл authorized_keys пользователя appuser на удаленных узлах (/home/appuser/.ssh/authorized_keys). Убедиться, что у директории .ssh правильные права (700), а у файла authorized_keys - права (600).

3. Написать плейбук, который копирует шаблон файла mod с управляющей машины (templates/motd.j2) на удаленные узлы в /etc/motd. Использовать переменную {{ inventory_hostname }} в шаблоне, чтобы в файле motd отображалось имя хоста. Шаблон (templates/motd.j2)

4. Написать плейбук, который проверит, установлен ли git на удаленных узлах и склонирует репозиторий https://gitlab.com/devops201206/it-mtb-blog в директорию /var/www/simple-blog

5. Написать плейбук для сбора системной информации об управляемых узлах размер оперативной памятиразмер диска, смонтированного в версия ОС
