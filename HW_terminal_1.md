
5.
![image](https://user-images.githubusercontent.com/44917492/142262505-fa891710-67b1-48a7-9f43-72e4acceb177.png)

8,HISTSIZE=1000
HISTFILESIZE=2000

![image](https://user-images.githubusercontent.com/44917492/142262604-c5f9d979-56ff-48ec-8968-acd9d1558bb4.png)

ignoreboth  -- игнорирование заданных команд в history
Для этого в файл ~/.bashrc добавим строку:
export HISTIGNORE='ls:ps:history*'
выполним source ~/.bashrc


или все вместе : 
cat <<EOT >> ~/.bashrc
export HISTSIZE=10000
export HISTFILESIZE=10000
export HISTCONTROL=ignoreboth:erasedups
PROMPT_COMMAND='history -a'
export HISTIGNORE='ls:ps:history*'
export HISTTIMEFORMAT='%d.%m.%Y %H:%M:%S: '
EOT
source ~/.bashrc
9.
в find {} заменяется каждым именем файла, найденным в выполняемой команде. Одна приятная особенность заключается в том, что это имя файла является строго одним аргументом, независимо от имени файла (даже содержащего встроенные пробелы, табуляции, переводы строк и любые символы

кроме того {} одна из групирующих команд { список ; }
Помещение списка команд между фигурными скобками приводит к тому, что список будет выполняться в текущем контексте оболочки. Подоболочка не создается. Точка с запятой (или новая строка) в следующем списке обязательна.

  10.
  touch -c file{1..100000}
для 300.000 вывалимся за пределы виртуальной памяти  и получим " arg list too long "
логика /dir-with-many-files$ echo * | wc -c
    /dir-with-many-files$ for i in * ; do grep ARG_MAX "$i"; done
мой expr `getconf ARG_MAX` - `env|wc -c` - `env|wc -l` \* 4 - 2048 = 2092865
  
11. тестовая проверка вывода команды. Проверит существует ли дирректория /tmp, ответ 0 считается истиной
  
12 нашел свою ошибку, от которой порядком настрадался) 
  
  дело было в том, что домашний каталог был /home/vagrant , я  этого не учитывал и пытался запихать в /tmp/test
  
**vagrant@vagrant:~/tmp/test$** pwd
  
/home/vagrant/tmp/test
  
**vagrant@vagrant:~/tmp/test$** cp bin/bash /home/vagrant/tmp/test
  
cp: cannot stat 'bin/bash': No such file or directory
  
**vagrant@vagrant:~/tmp/test$** cp /bin/bash /home/vagrant/tmp/test
  
**vagrant@vagrant:~/tmp/test$** PATH=/home/vagrant/tmp/test:$PATH
  
**vagrant@vagrant:~/tmp/test$** type -a bash
  
bash is /home/vagrant/tmp/test/bash
  
bash is /usr/bin/bash
  
bash is /bin/bash
  
vagrant@vagrant:~/tmp/test$ cd $HOME
  
vagrant@vagrant:~$ pwd
  
/home/vagrant
  
  
13.at используется для назначения одноразового задания на заданное время, а команда batch — для назначения одноразовых задач, которые должны выполняться, когда загрузка системы становится меньше 0,8.
  
14.vagrant halt

