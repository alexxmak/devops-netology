1. команда cd отличается от остальных (небашевских) команд тем, что встроена в оболочку bash. Т.е. не представляет собой отдельный файл (нарушается директива все есть файл, (но сам баш при этом файл)). Сделано это именно так, потому что в оболочке реализованы базовые команды взаимодействия с ОС, если бы их не было, мы бы получили систему с которой ничего нельзя сделать, даже накатить пакеты с нужными командами.

2.
два вывода ответ одинаков
vagrant@vagrant:~$ grep -c test ./cd1

2

vagrant@vagrant:~$ grep test ./cd1 | wc -l

2

3.
![image](https://user-images.githubusercontent.com/44917492/143400167-8cc5ea9a-5fb6-4063-bbb9-a3fbad29ef98.png)
Стандартный /sbin/init читает конфигурационный файл /etc/inittab, стартует систему и управляет системой используя несколько «уровней исполнения» (runlevels). Программа /sbin/init (также init) координирует оставшуюся часть процесса загрузки и выполняет настройку окружения пользователя.

4. ps -ef > /dev/pts/1

5. ls -la >in 1>out 

6.
![image](https://user-images.githubusercontent.com/44917492/143400298-51ad08a5-3c80-41cd-bb20-a2dad09512f5.png)

![image](https://user-images.githubusercontent.com/44917492/143400335-2a4dd360-12e9-4b6c-9bae-a3373b5a2583.png)

7.bash 5>&1 - Создаст дескриптор с 5 и перенатправит вывод
echo netology > /proc/$$/fd/5 - выведет в дескриптор 5

8. ls -l ./cd1 5>&2 2>&1 1>&5 |grep denied -c 

9.теже переменные окружения, что и в printenv и env

10./proc/<PID>/cmdline - полный путь до исполняемого файла процесса [PID]  (строка 231)
/proc/<PID>/exe - содержит ссылку до файла запущенного для процесса [PID], 
                        cat выведет содержимое запущенного файла, 
                        запуск этого файла,  запустит еще одну копию самого файла  (строка 285)
  
11.
  ![image](https://user-images.githubusercontent.com/44917492/143400621-143d0be6-0d27-438a-8b27-23f0b0b1b235.png)

12.По умолчанию, когда вы запускаете команду на удаленном компьютере с помощью ssh, TTY не выделяется для удаленного сеанса. Это позволяет передавать двоичные данные и т. Д. Без необходимости работать с причудами TTY. Это среда, предусмотренная для команды, выполняемой на computerone.

Однако, когда вы запускаете ssh без удаленной команды, он выделяет TTY, потому что вы, скорее всего, будете запускать сеанс оболочки. Это ожидается ssh otheruser@computertwo.comкомандой, но из-за предыдущего объяснения для этой команды нет доступного TTY.
![image](https://user-images.githubusercontent.com/44917492/143400702-9643180f-0bf2-4a1e-8800-eda851bd1381.png)

13.установил, при первых запусках ругался на права, 10-patrace.conf,после установки заначения  kernel.yama.ptrace_scope = 0 все равно не работал и не перехватывал, пока не перезапустил машину, после запуска процесс успешно перехватился и остался работать после закрытия терминала

14.команда tee делает вывод одновременно и в файл, указаный в качестве параметра, и в stdout, так как tee запущена из под sudo то то она имеет права на запись в файл
 






