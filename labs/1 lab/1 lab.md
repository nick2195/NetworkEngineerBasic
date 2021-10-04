## Часть 1 

### Шаг 1

#### a. 
![image](https://user-images.githubusercontent.com/44971394/135821145-d5fe57e9-2764-4c7f-a684-7b9f9888ee5b.png)


#### b.
![image](https://user-images.githubusercontent.com/44971394/135821455-c259a69e-513d-4edb-a8d9-72be10b23f71.png)


*Почему нужно использовать консольное подключение для первоначальной настройки коммутатора? Почему нельзя подключиться к коммутатору через Telnet или SSH?*
**Потому что это самое безопасное и настроенное по умолчанию подключение. Для использование telnet и ssh необходим другой кабель(RJ 45) и знание ip-адреса устройства.**

### Шаг 2

#### a. 
![image](https://user-images.githubusercontent.com/44971394/135821548-80fc1d6a-f77a-46ab-92a7-5c36afb8116c.png)


#### b. 
*Сколько интерфейсов FastEthernet имеется на коммутаторе 2960?*
**24**

*Сколько интерфейсов Gigabit Ethernet имеется на коммутаторе 2960?*
**2**

*Каков диапазон значений, отображаемых в vty-линиях?*
**0-15**

#### с.
*Изучите файл загрузочной конфигурации (startup configuration), который содержится в энергонезависимом ОЗУ (NVRAM).
Почему появляется это сообщение?*


**startup-config is not present
Так как ещё не задана и не перемещена во флеш-память**

#### d.
*Назначен ли IP-адрес сети VLAN 1?*
**Нет, не назначен, не настраивали**

*Какой MAC-адрес имеет SVI? Возможны различные варианты ответов.*
**Думаю, что либо мак адрес устройства(Свича), либо мак адрес сетевой карты**

*Данный интерфейс включен?*
**Нет
interface Vlan1
 no ip address
 shutdown**

#### e.
*Какие выходные данные вы видите?*
**Никаких, только из пункта d**


#### f.
*Какие выходные данные вы видите?*
![image](https://user-images.githubusercontent.com/44971394/135821877-d0ff8937-a0b7-4653-a3a7-86a31eee7b82.png)



#### g.
*Под управлением какой версии ОС Cisco IOS работает коммутатор?*
**15.0(2)SE4 **

*Как называется файл образа системы?*
**flash:c2960-lanbasek9-mz.150-2.SE4.bin**

*Какой базовый MAC-адрес назначен коммутатору?*
**00:17:59:A7:51:80**

#### h.
![image](https://user-images.githubusercontent.com/44971394/135821933-b4572fed-700a-40a7-ad06-a9f753a67f2c.png)


*Интерфейс включен или выключен?*
**Выключен**

*Что нужно сделать, чтобы включить интерфейс?*
**Задать ip. и no shutdown**

*Какой MAC-адрес у интерфейса?*
**0002.4a02.1d06**

*Какие настройки скорости и дуплекса заданы в интерфейсе?*
**100mb/s, full**

#### i.
*Какое имя присвоено сети VLAN 1 по умолчанию?*
****

*Какие порты расположены в сети VLAN 1?*
**Не до конца понял вопрос**
*Активна ли сеть VLAN 1?*
**Нет, пока не прописана команда "no shutdown"**

*К какому типу сетей VLAN принадлежит VLAN по умолчанию?*
**локальные**

#### j.
*Какое имя присвоено образу Cisco IOS?*
![image](https://user-images.githubusercontent.com/44971394/135822063-33476c06-198b-4606-8c4b-3d0e26a2d19b.png)


## Часть 2

### Шаг 1.

#### a. 
![image](https://user-images.githubusercontent.com/44971394/135822098-ab55a633-d6d7-4be3-b514-4914af6ccab2.png)

#### b. 
![image](https://user-images.githubusercontent.com/44971394/135822131-2edea39e-8e5e-46b8-8f13-8fab0515cbf7.png)

#### c.
![image](https://user-images.githubusercontent.com/44971394/135822160-3fd90e92-4e8b-4b1c-88ca-32a1e18b3bc1.png)

 

#### d. 
![image](https://user-images.githubusercontent.com/44971394/135822193-c184a055-03f8-4685-988b-dbe2e097d088.png)

*Для чего нужна команда login?*
**В данном случае она включает доступ к VTY.**



### Шаг 2.
![image](https://user-images.githubusercontent.com/44971394/135822229-755c4c82-23a4-4fb1-b121-974bcdde7ad8.png)



## Часть 3.

### Шаг 1.

#### a.
S1#show run
Building configuration...

Current configuration : 1319 bytes
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname S1
!
enable secret 5 $1$mERr$9cTjUIEqNGurQiFU.ZeCi1
!
!
!
no ip domain-lookup
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
!
interface FastEthernet0/2
!
interface FastEthernet0/3
!
interface FastEthernet0/4
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 ip address 192.168.1.20 255.255.255.0
!
banner motd ^C
Unauthorized access is strictly prohibited. ^C
!
!
!
line con 0
 password 7 0822455D0A16
 logging synchronous
 login
!
line vty 0 4
 password 7 0822455D0A16
 login
line vty 5 15
 password 7 0822455D0A16
 login
!
!
!
!
end

#### b.
*Какова полоса пропускания этого интерфейса?*
**BW 100000 Kbit**

*В каком состоянии находится VLAN 1?*
**Vlan1 is up**

*В каком состоянии находится канальный протокол?*
**line protocol is down**


### Шаг 2.

#### a.
![image](https://user-images.githubusercontent.com/44971394/135822260-63c1effd-d044-4728-bfce-160e717ac670.png)


#### b.
![image](https://user-images.githubusercontent.com/44971394/135822283-9ba49b6f-4848-42df-9e04-dc3c2f5c16f7.png)



### Шаг 3.
![image](https://user-images.githubusercontent.com/44971394/135822305-2c371844-cd09-443e-91fc-5b96ea161fba.png)




## Вопросы для повторения.

*1.Зачем необходимо настраивать пароль VTY для коммутатора?*
**Для ограничения доступа к конфигурациям устройств**

*2.Что нужно сделать, чтобы пароли не отправлялись в незашифрованном виде?*
**S1(config)# service password-encryption**


