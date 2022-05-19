# Program6</br></br>
## Описание работы программы </br></br>
В программе создается массив файловых дескрипторов.</br>
Проверка корректности ввода. </br>
if (argc != 2)</br>
and</br>
if (pipe(pipefd) == -1)</br></br>
Вызов fork(), проверка полученного PID. Дальше работа родительского процесса.</br>
    close(pipefd[0]);</br>
    write(pipefd[1], argv[1], strlen(argv[1]));</br>
    close(pipefd[1]);</br>
    wait(NULL); </br>
    exit(EXIT_SUCCESS);</br></br>
Дочерний процесс cчитает данные.</br>
if (cpid == 0) </br>
{</br>
    close(pipefd[1]); </br>
    while (read(pipefd[0], & buf, 1) > 0)</br>
      write(STDOUT_FILENO, & buf, 1);</br>
    write(STDOUT_FILENO, "\n", 1);</br>
    close(pipefd[0]);</br>
    _exit(EXIT_SUCCESS);</br></br>
Общение между процессами с помощью общего канала.</br></br>
