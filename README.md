1. chdir("/tmp")                           = 0

2. strace -tt -e trace=openat file /bin/bash

14:34:17.360031 openat(AT_FDCWD, "/etc/ld.so.cache", O_RDONLY|O_CLOEXEC) = 3

14:34:17.373264 openat(AT_FDCWD, "/usr/lib/locale/locale-archive", O_RDONLY|O_CLOEXEC) = 3

14:34:17.374005 openat(AT_FDCWD, "/etc/magic", O_RDONLY) = 3

14:34:17.374351 openat(AT_FDCWD, "/usr/share/misc/magic.mgc", O_RDONLY) = 3

14:34:17.374854 openat(AT_FDCWD, "/usr/lib/x86_64-linux-gnu/gconv/gconv-modules.cache", O_RDONLY) = 3

14:34:17.375247 openat(AT_FDCWD, "/bin/bash", O_RDONLY|O_NONBLOCK) = 3


3. $ >название_файла

4. Нет, не занимают. Информация о них будет видна в списке процессов, но это завершенный процесс.

5. ~$ strace -tt -e trace=openat dpkg -L bpfcc-tools | grep sbin/opensnoop

12:25:06.117205 openat(AT_FDCWD, "/etc/ld.so.cache", O_RDONLY|O_CLOEXEC) = 3

12:25:06.117673 openat(AT_FDCWD, "/lib/x86_64-linux-gnu/libselinux.so.1", O_RDONLY|O_CLOEXEC) = 3

12:25:06.118317 openat(AT_FDCWD, "/lib/x86_64-linux-gnu/libc.so.6", O_RDONLY|O_CLOEXEC) = 3

12:25:06.119308 openat(AT_FDCWD, "/lib/x86_64-linux-gnu/libpcre2-8.so.0", O_RDONLY|O_CLOEXEC) = 3

12:25:06.119740 openat(AT_FDCWD, "/lib/x86_64-linux-gnu/libdl.so.2", O_RDONLY|O_CLOEXEC) = 3

12:25:06.120278 openat(AT_FDCWD, "/lib/x86_64-linux-gnu/libpthread.so.0", O_RDONLY|O_CLOEXEC) = 3

12:25:06.122095 openat(AT_FDCWD, "/proc/filesystems", O_RDONLY|O_CLOEXEC) = 3

12:25:06.125731 openat(AT_FDCWD, "/usr/lib/locale/locale-archive", O_RDONLY|O_CLOEXEC) = 3

12:25:06.126180 openat(AT_FDCWD, "/etc/dpkg/dpkg.cfg.d", O_RDONLY|O_NONBLOCK|O_CLOEXEC|O_DIRECTORY) = 3

12:25:06.126479 openat(AT_FDCWD, "/etc/dpkg/dpkg.cfg.d/pkg-config-hook-config", O_RDONLY) = 3

12:25:06.126916 openat(AT_FDCWD, "/etc/dpkg/dpkg.cfg", O_RDONLY) = 3

12:25:06.127298 openat(AT_FDCWD, "/home/artem/.dpkg.cfg", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.131128 openat(AT_FDCWD, "/etc/ld.so.cache", O_RDONLY|O_CLOEXEC) = 3

12:25:06.131468 openat(AT_FDCWD, "/lib/x86_64-linux-gnu/libc.so.6", O_RDONLY|O_CLOEXEC) = 3

12:25:06.132984 openat(AT_FDCWD, "/usr/lib/locale/locale-archive", O_RDONLY|O_CLOEXEC) = 3

12:25:06.136040 openat(AT_FDCWD, "/var/lib/dpkg/arch", O_RDONLY) = 3

12:25:06.136418 openat(AT_FDCWD, "/var/lib/dpkg/status", O_RDONLY) = 3

12:25:06.197741 openat(AT_FDCWD, "/var/lib/dpkg/updates/", O_RDONLY|O_NONBLOCK|O_CLOEXEC|O_DIRECTORY) = 3

12:25:06.198150 openat(AT_FDCWD, "/var/lib/dpkg/triggers/File", O_RDONLY) = 3

12:25:06.198831 openat(AT_FDCWD, "/var/lib/dpkg/triggers/Unincorp", O_RDONLY) = 3

12:25:06.199129 openat(AT_FDCWD, "/var/lib/dpkg/info/format", O_RDONLY) = 4

12:25:06.199483 openat(AT_FDCWD, "/var/lib/dpkg/info/bpfcc-tools.list", O_RDONLY) = 4

12:25:06.200842 openat(AT_FDCWD, "/var/lib/dpkg/diversions", O_RDONLY) = 4
/usr/sbin/opensnoop-bpfcc
12:25:06.201816 openat(AT_FDCWD, "/usr/share/locale/locale.alias", O_RDONLY|O_CLOEXEC) = 5

12:25:06.202303 openat(AT_FDCWD, "/usr/share/locale/en_US.UTF-8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.202519 openat(AT_FDCWD, "/usr/share/locale/en_US.utf8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.202743 openat(AT_FDCWD, "/usr/share/locale/en_US/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.202930 openat(AT_FDCWD, "/usr/share/locale/en.UTF-8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.203159 openat(AT_FDCWD, "/usr/share/locale/en.utf8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.203344 openat(AT_FDCWD, "/usr/share/locale/en/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.203528 openat(AT_FDCWD, "/usr/share/locale-langpack/en_US.UTF-8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.203759 openat(AT_FDCWD, "/usr/share/locale-langpack/en_US.utf8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.203977 openat(AT_FDCWD, "/usr/share/locale-langpack/en_US/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.204183 openat(AT_FDCWD, "/usr/share/locale-langpack/en.UTF-8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.204370 openat(AT_FDCWD, "/usr/share/locale-langpack/en.utf8/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)

12:25:06.204568 openat(AT_FDCWD, "/usr/share/locale-langpack/en/LC_MESSAGES/dpkg.mo", O_RDONLY) = -1 ENOENT (No such file or directory)


6. вызов uname, 

Part of the utsname information is also accessible 

via /proc/sys/kernel/{ostype, hostname, osrelease, version, domainname}

7. Оператор точка с запятой позволяет запускать несколько команд за один раз, и выполнение команды происходит последовательно.
Оператор AND (&&) будет выполнять вторую команду только в том случае, если при выполнении первой команды SUCCEEDS, 
т.е. состояние выхода первой команды равно «0» — программа выполнена успешно. Эта команда очень полезна при проверке 
состояния выполнения последней команды.

set -e и && - аналоги, нет смысла исползовать оба варианта одновременно.

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
