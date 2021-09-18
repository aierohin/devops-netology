1.  - sudo systemctl enable node_exporter  
	- [Unit]  
	Description=Node Exporter Service  
	After=network.target  
	After=remote-fs.target nss-user-lookup.target  

	[Service]  
	User=erohin  
	Group=erohin  
	Type=simple  
	ExecStart=/usr/local/bin/node_exporter  
	ExecReload=/bin/kill -HUP $MAINPID  
	Restart=on-failure  

	[Install]  
	WantedBy=multi-user.target  

2. 	rate(node_cpu_seconds_total{mode="system"}[1m])	  
	node_filesystem_avail_bytes	  
	rate(node_network_receive_bytes_total[1m])  
3. 	cpu  
Total CPU utilization (all cores).  
	load  
Current system load, i.e. the number of processes using CPU or waiting for system resources (usually CPU and disk).   
	disk  
Total Disk I/O, for all physical disks.  
	ram  
System Random Access Memory (i.e. physical memory) usage.  
	swap  
System swap memory usage.   
	network  
Total bandwidth of all physical network interfaces.   

4. Да, можно:   
[   22.288274] 21:03:59.032801 main     VBoxService 6.1.16_Ubuntu r140961 (verbosity: 0) linux.amd64 (Apr 29 2021 15:42:15) release log  
               21:03:  
[   22.288872] 21:03:59.034433 main     OS Product: Linux  
[   22.289499] 21:03:59.034924 main     OS Release: 5.11.0-34-generic  
[   22.290557] 21:03:59.035574 main     OS Version: #36~20.04.1-Ubuntu SMP Fri Aug 27 08:06:32 UTC 2021  
[   22.291970] 21:03:59.036614 main     Executable: /usr/sbin/VBoxService  
               21:03:59.036615 main     Process ID: 754  


5. fs.nr_open = 1048576. Это системное ограничение на открытые файлы.  
   Утилита ulimit возвращает два вида ограничений - hard и soft. Ограничение soft вы можете менять в любую сторону,    
   пока оно не превышает hard. Ограничение hard можно менять только в меньшую сторону от имени обычного пользователя.    
   От имени суперпользователя можно менять оба вида ограничений так, как нужно.   
   -S отображаются soft-ограничения:  
   ulimit -S  

   Чтобы вывести hard, используйте опцию -H:  
   ulimit -H  
   
6. $ nsenter --target 3629 --pid --mount  
root@artem-VirtualBox:/# ps aux  
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND  
root           1  0.0  0.0  16716   580 pts/0    S+   00:14   0:00 sleep 1h  
7. Система зависла, не восстановилась в течение часа.  
