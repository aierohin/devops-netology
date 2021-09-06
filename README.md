Ubuntu настроена: на ноутбуке и на виртуалке, на отдельном компе с виндой.
8. HISTFILESIZE, 717 строка мануала.
   ignoreboth является сокращением для игнорирования пробелов(ignorespace) и игнорирования вставок(ignoredups).
   
9. 1. Преобразование скобок, строка 922
   2. ${parameter}, строка 988   

10. touch file{1..100000}

11. [[ -d /tmp ]] - условие, является ли папка директорией. Так как является, то выдает 0, иначе 1.

12. mkdir /tmp/new_path_directory
	sudo cp /bin/bash /usr/local/bin/
	sudo cp /bin/bash /tmp/new_path_directory
	export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin:/tmp/new_path_directory/bash:/tmp/new_path_directory
	
	$ type -a bash
	bash is /usr/local/bin/bash
	bash is /bin/bash
	bash is /tmp/new_path_directory/bash
13. Команда at используется для назначения одноразового задания на заданное время, а команда batch — для назначения одноразовых задач, которые
 должны выполняться, когда загрузка системы становится меньше 0,8.	
