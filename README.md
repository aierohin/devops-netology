# Домашнее задание к занятию "Введение. Экосистема. Архитектура. Жизненный цикл Docker контейнера"  
  
## Обязательные задания  
  
1. 	https://hub.docker.com/repository/docker/aierohin/nginx.  
	
2.	Высоконагруженное монолитное java веб-приложение - физическая машина  
Nodejs веб-приложение - использование Docker контейнеров  
Мобильное приложение c версиями для Android и iOS - использование Docker контейнеров  
Шина данных на базе Apache Kafka - виртуальная машина  
Elasticsearch кластер для реализации логирования продуктивного веб-приложения - три ноды elasticsearch, два logstash и две ноды kibana - использование Docker контейнеров  
Мониторинг-стек на базе Prometheus и Grafana - виртуальная машина  
MongoDB, как основное хранилище данных для java-приложения - физическая машина  
Gitlab сервер для реализации CI/CD процессов и приватный (закрытый) Docker Registry - виртуальная машина    

3.	```bash
	erohin@erohin-VirtualBox:~$ ls data/
	test_debian
	erohin@erohin-VirtualBox:~$ nano data/test_host
	erohin@erohin-VirtualBox:~$ ls data/
	test_debian  test_host
	erohin@erohin-VirtualBox:~$ cat data/test_debian 
	Test file from debian.
	erohin@erohin-VirtualBox:~$ cat data/test_host 
	Test file from host
	erohin@erohin-VirtualBox:~$ sudo docker ps -a
	CONTAINER ID   IMAGE     COMMAND   CREATED         STATUS                          PORTS     NAMES
	b3886c942cd2   debian    "bash"    3 minutes ago   Exited (0) About a minute ago             fervent_blackburn
	erohin@erohin-VirtualBox:~$ sudo docker run -it -v ~/data:/data-container centos bin/bash
	Unable to find image 'centos:latest' locally
	latest: Pulling from library/centos
	a1d0c7532777: Pull complete 
	Digest: sha256:a27fd8080b517143cbbbab9dfb7c8571c40d67d534bbdee55bd6c473f432b177
	Status: Downloaded newer image for centos:latest
	[root@4e27905790ed /]# ls data-container/
	test_debian  test_host
	[root@4e27905790ed /]# cat > data-container/test_centos
	Test file from centos.
	[root@4e27905790ed /]# ls data-container/
	test_centos  test_debian  test_host
	[root@4e27905790ed /]# exit
	exit
	erohin@erohin-VirtualBox:~$ sudo docker ps -a
	CONTAINER ID   IMAGE     COMMAND      CREATED              STATUS                     PORTS     NAMES
	4e27905790ed   centos    "bin/bash"   About a minute ago   Exited (0) 3 seconds ago             pedantic_robinson
	b3886c942cd2   debian    "bash"       5 minutes ago        Exited (0) 3 minutes ago             fervent_blackburn
	erohin@erohin-VirtualBox:~$ ls data/
	test_centos  test_debian  test_host

	```
	
