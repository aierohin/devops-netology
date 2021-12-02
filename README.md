# Домашнее задание к занятию "5.5. Оркестрация кластером Docker контейнеров на примере Docker Swarm"  
  
## Обязательные задания  
  
1.   	
	В режиме replication сервис будет запущен только на workers. В режиме global сервис будет запущен на всех нодах кластера.  
	Используется алгоритм Raft для выбора лидера в кластере.  
	Overlay сеть - это абстрактная сеть, построенная на физической(underlay) сети. Пример - VXLAN.   

2.	```bash
	[centos@node01 ~]$ sudo docker node ls  
	ID                            HOSTNAME             STATUS    AVAILABILITY   MANAGER STATUS   ENGINE VERSION
	kjz4jr5k5kv6u8lozgtc8iael *   node01.netology.yc   Ready     Active         Leader           20.10.11
	g9lfp7jejge249fyngxtyo6vi     node02.netology.yc   Ready     Active         Reachable        20.10.11
	vqm1ai9kbt50z7tf4mfxtoklz     node03.netology.yc   Ready     Active         Reachable        20.10.11
	svt0lomrvn9mm9b74lkbuulov     node04.netology.yc   Ready     Active                          20.10.11
	q30pev2etun5c9iwz4qsap20c     node05.netology.yc   Ready     Active                          20.10.11
	yt97mvuf7z7e1y9tolo8orvn6     node06.netology.yc   Ready     Active                          20.10.11
	```
3.	```bash
	[centos@node01 ~]$ sudo docker service ls
	ID             NAME                                MODE         REPLICAS   IMAGE                                          PORTS
	926b6gc47elp   swarm_monitoring_alertmanager       replicated   1/1        stefanprodan/swarmprom-alertmanager:v0.14.0    
	sgklx51p51r3   swarm_monitoring_caddy              replicated   1/1        stefanprodan/caddy:latest                      *:3000->3000/tcp, *:9090->9090/tcp, *:9093-	 9094->9093-9094/tcp
	k8mbw2ctsm70   swarm_monitoring_cadvisor           global       6/6        google/cadvisor:latest                         
	9xfmxnvloa6p   swarm_monitoring_dockerd-exporter   global       6/6        stefanprodan/caddy:latest                      
	zmtj974fah0b   swarm_monitoring_grafana            replicated   1/1        stefanprodan/swarmprom-grafana:5.3.4           
	ub7irievd9lj   swarm_monitoring_node-exporter      global       6/6        stefanprodan/swarmprom-node-exporter:v0.16.0   
	yxpcmu5oazhm   swarm_monitoring_prometheus         replicated   1/1        stefanprodan/swarmprom-prometheus:v2.5.0       
	b1eh4csvo3j8   swarm_monitoring_unsee              replicated   1/1        cloudflare/unsee:v0.8.0                
	```
