# Домашнее задание к занятию "Применение принципов IaaC в работе с виртуальными машинами"  
  
## Обязательные задания  
  
1. 	Применение паттернов позволяет сделать разработку более эффективной, а также ускоряет подготовку сред CI/CD.  
	Основополагающий принцип IaaC - идемпотентность.  
	
2.	Ansible работает по ssh с оборудованием, нет необходимости устанавливать агентов на оборудование.  
	Push - более надежен так, как позволяет централизованно управлять отправкой конфигураций через управляющий сервер.  

3.	```bash
	artem@artem-VirtualBox:~$ virtualbox -h  
	Oracle VM VirtualBox VM Selector v6.1.26_Ubuntu  
	(C) 2005-2021 Oracle Corporation  
	All rights reserved.  
	
	artem@artem-VirtualBox:~$ vagrant -v  
	Vagrant 2.2.6  
	
	artem@artem-VirtualBox:~$ ansible --version  
	ansible 2.9.6
	```
	
## Необязательные задания
4.	```bash
	artem@artem-VirtualBox:~$ docker -v  
	Docker version 20.10.8, build 3967b7d28e  
	
	artem@artem-VirtualBox:~$ sudo docker ps  
	CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
	```
