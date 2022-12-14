- приглашение ```minishell > ```
- история команд
- запуск бинарных файлов
- обработка одинарных кавычек (все мета-символы внутри кавычек игнорируются)
- обработка двойных кавычек (все мета-символы внутри кавычек игнорируются, за исключением "$")
- перенаправления входящих/исходящих потоков
  - ```<``` - перенаправление входящего потока из файла
  - ```<<``` - подается ограничитель, после чего идет чтение из стандартного ввода до тех пор, пока не встретится ограничитель
  - ```>``` - перенаправление исходящего потока в файл (в режиме перезаписи файла)
  - ```>>``` - перенаправление исходящего потока в файл (в режиме добавления в конец файла)
- перенаправление потоков с помощью пайпов "|"
- переменные окружения заменяются на их значение (```$PWD```, ```$HOME```, ...)
- ```$?``` - статус выполнения предыдущей команды
- обработка сигналов
  - ```Ctrl+C``` - отображает приглашение с новой строки
  - ```Ctrl+D``` - завершает работу оболочки
  - ```Ctrl+\``` - игнорируется
- реализованы следующие built-in'ы:
  - ```echo``` с флагом ```-n```
  - ```cd``` с относительным и абсолютным путем, без пути или с "~"
  - ```pwd``` без флагов
  - ```export``` без флагов
  - ```unset``` без флагов
  - ```env```  без флагов или аргументов
  - ```exit``` без флагов
