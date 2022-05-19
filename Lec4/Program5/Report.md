# Program5</br></br>
## Описание работы программы</br></br>
Программа обрабатывает сигнал, полученный от пользователя.</br>
Глобальная переменная-счётчик counter: </br>
int counter = 0;</br></br>
Обрабатывающие функции handler1.</br>
void handler1(int sig)</br>
{</br>
  counter++;</br>
  printf("counter = %d\n", counter);</br>
  /* Flushes the printed string to stdout */</br>
  fflush(stdout);</br>
  kill(pid, SIGUSR1);</br>
}</br></br>
handler2 </br>
void handler2(int sig)</br>
{</br>
  counter += 3;</br>
  printf("counter = %d\n", counter);</br>
  exit(0);</br>
}</br>
