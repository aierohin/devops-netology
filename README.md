1. chdir("/tmp")                           = 0

2. strace -tt -e trace=openat file /bin/bash

14:34:17.360031 openat(AT_FDCWD, "/etc/ld.so.cache", O_RDONLY|O_CLOEXEC) = 3

14:34:17.373264 openat(AT_FDCWD, "/usr/lib/locale/locale-archive", O_RDONLY|O_CLOEXEC) = 3

14:34:17.374005 openat(AT_FDCWD, "/etc/magic", O_RDONLY) = 3

14:34:17.374351 openat(AT_FDCWD, "/usr/share/misc/magic.mgc", O_RDONLY) = 3

14:34:17.374854 openat(AT_FDCWD, "/usr/lib/x86_64-linux-gnu/gconv/gconv-modules.cache", O_RDONLY) = 3

14:34:17.375247 openat(AT_FDCWD, "/bin/bash", O_RDONLY|O_NONBLOCK) = 3


3. $ >название_файла
   Доработка задания:
   Файл для логов приложения, я бы назвал <название_приложения_log>.
   Или я неправильно понял вопрос - "Какое название будет иметь удаленный файл?" ?

4. Нет, не занимают. Информация о них будет видна в списке процессов, но это завершенный процесс.

5. Доработка задания:
   sudo /usr/sbin/opensnoop-bpfcc -d 1
   
   PID    COMM               FD ERR PATH
   
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
8950   glean.dispatche    50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/datareporting/glean/db/data.safe.bin  
5157   marco              22   0 /proc/8950/status  
5157   marco              22   0 /proc/8950/stat  
5157   marco              22   0 /proc/8950/status  
5157   marco              22   0 /proc/8950/stat  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/rx_packets  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/tx_packets  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/rx_bytes  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/tx_bytes  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/rx_errors  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/tx_errors  
5204   mate-netspeed-a    13   0 /sys/class/net/wls1/statistics/collisions  
5204   mate-netspeed-a    13   0 /proc/net/route  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/rx_packets  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/tx_packets  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/rx_bytes  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/tx_bytes  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/rx_errors  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/tx_errors  
5204   mate-netspeed-a    14   0 /sys/class/net/wls1/statistics/collisions  
8950   DOMCacheThread     50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/storage/default/https+++web.telegram.org/cache/morgue/255/{71c60172-3dac-4bd5-bd12-b82d76c848ff}.final  
8950   LS Thread          50   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/webappsstore.sqlite  
8950   LS Thread          63   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/webappsstore.sqlite-wal  
8950   LS Thread          73   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/storage/default/https+++web.telegram.org/ls/data.sqlite-journal  
8950   LS Thread          89   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/storage/default/https+++web.telegram.org/ls/usage-journal  
8950   LS Thread          89   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/storage/default/https+++web.telegram.org/ls/usage  
8950   LS Thread          89   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release/storage/default/https+++web.telegram.org/ls  
8950   LS Thread          89   0 /home/erokhin/.mozilla/firefox/0h0kadk4.default-release  
773    irqbalance          6   0 /proc/interrupts  
773    irqbalance          6   0 /proc/stat  
773    irqbalance          6   0 /proc/irq/24/smp_affinity  
773    irqbalance          6   0 /proc/irq/21/smp_affinity  
773    irqbalance          6   0 /proc/irq/17/smp_affinity  
773    irqbalance          6   0 /proc/irq/29/smp_affinity  
773    irqbalance          6   0 /proc/irq/23/smp_affinity  
773    irqbalance          6   0 /proc/irq/25/smp_affinity  
773    irqbalance          6   0 /proc/irq/22/smp_affinity 
773    irqbalance          6   0 /proc/irq/27/smp_affinity  
773    irqbalance          6   0 /proc/irq/18/smp_affinity  
773    irqbalance          6   0 /proc/irq/20/smp_affinity  
773    irqbalance          6   0 /proc/irq/16/smp_affinity  
773    irqbalance          6   0 /proc/irq/11/smp_affinity  
773    irqbalance          6   0 /proc/irq/19/smp_affinity  
773    irqbalance          6   0 /proc/irq/26/smp_affinity  
773    irqbalance          6   0 /proc/irq/1/smp_affinity  
773    irqbalance          6   0 /proc/irq/8/smp_affinity  
773    irqbalance          6   0 /proc/irq/9/smp_affinity  
773    irqbalance          6   0 /proc/irq/12/smp_affinity  
5157   marco              22   0 /proc/8950/status  
5157   marco              22   0 /proc/8950/stat  



6. вызов uname, 

Part of the utsname information is also accessible 

via /proc/sys/kernel/{ostype, hostname, osrelease, version, domainname}

7. Оператор точка с запятой позволяет запускать несколько команд за один раз, и выполнение команды происходит последовательно.
Оператор AND (&&) будет выполнять вторую команду только в том случае, если при выполнении первой команды SUCCEEDS, 
т.е. состояние выхода первой команды равно «0» — программа выполнена успешно. Эта команда очень полезна при проверке 
состояния выполнения последней команды.  

set -e и && - С параметром -e оболочка завершится только при ненулевом коде возврата простой команды. Если ошибочно завершится одна из команд, разделённых &&, то выхода не произойдёт.    
Доработка задания:
Спасибо за объяснение, смысл теперь ясен.

8. -e  Exit immediately if a command exits with a non-zero status.
 
   -u  Treat unset variables as an error when substituting.
   
   -x  Print commands and their arguments as they are executed.
   
   -o  pipefail     the return value of a pipeline is the status of
                    the last command to exit with a non-zero status,
                    or zero if no command exited with a non-zero status
                    
   set -euxo pipefail С ее помощью, можно значительно повысить безопасность.
   
9. Наиболее часто встречающийся статус у процессов в системе - S.
   
   Дополнительные символы:
   
               <    high-priority (not nice to other users)
               
               N    low-priority (nice to other users)
               
               L    has pages locked into memory (for real-time and custom IO)
               
               s    is a session leader
               
               l    is multi-threaded (using CLONE_THREAD, like NPTL pthreads do)
               
               +    is in the foreground process group
