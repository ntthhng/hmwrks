# Program7</br></br>
## Описание работы программы </br></br>
Создание дескриптора и канала с правами доступа для всех.</br>
int fd; </br>
  int len;</br>
  char buf[BUFSIZE];</br>
    if (mkfifo(NAMEDPIPE_NAME, 0777))</br>
 { </br>
    perror("mkfifo");</br>
    return 1;</br>
  }</br>
</br></br>
Запуск бесконечного цикла,в котором приложение прослушивает его.</br>
do {</br>
    memset(buf, '\0', BUFSIZE);</br>
    if ((len = read(fd, buf, BUFSIZE - 1)) <= 0) </br>
    {</br>
      perror("read error");</br>
      close(fd);</br>
      remove(NAMEDPIPE_NAME);</br>
      return 0;</br>
    }</br>
    printf("Incomming message (%d): %s\n", len, buf);</br>
  } while (1);</br></br>
Производится вывод текста и количества символов, если программа получила сообщение</br></br>
if ((len = read(fd, buf, BUFSIZE - 1)) <= 0)</br>
