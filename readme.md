## ДЗ-01: Обновление ядра системы ##
#### Задание
1. Запустить ВМ c Ubuntu.
2. Обновить ядро ОС на новейшую стабильную версию из mainline-репозитория.
3. Оформить отчет в README-файле в GitHub-репозитории.
#### Выполнено:
##### Установка ОС Ubuntu 24.04.2 LTS
root@u24srv01:~# uname -r  
6.8.0-62-generic

##### Обновление ядра ОС ###
На сайте выбираем последнюю стабильную версию: https://kernel.ubuntu.com/mainline/v6.15/
- root@u24srv01:~/kernel_16# wget https://kernel.ubuntu.com/mainline/v6.15/amd64/linux-headers-6.15.0-061500-generic_6.15.0-061500.202505260036_amd64.deb
- root@u24srv01:~/kernel_16# wget https://kernel.ubuntu.com/mainline/v6.15/amd64/linux-headers-6.15.0-061500_6.15.0-061500.202505260036_all.deb
- root@u24srv01:~/kernel_16# wget https://kernel.ubuntu.com/mainline/v6.15/amd64/linux-image-unsigned-6.15.0-061500-generic_6.15.0-061500.202505260036_amd64.deb
- root@u24srv01:~/kernel_16# wget https://kernel.ubuntu.com/mainline/v6.15/amd64/linux-modules-6.15.0-061500-generic_6.15.0-061500.202505260036_amd64.deb

root@u24srv01:~/kernel_16# dpkg -i *.deb
##### Проверка
root@u24srv01:~/kernel_16# uname -r  
6.13.2-061302-generic
