# Program2</br></br>
## Описание работы программы</br></br>
Выделение памяти для массива элементов char.</br>
char * c = (char * ) calloc(100, sizeof(char));</br></br>
Открытие файла foo.txt для чтения(+создания).</br>
int fd = open("foo.txt", O_RDONLY | O_CREAT);</br></br>
Вывод значения дескриптора файла</br> 
printf("fd = %d/n", fd);.</br> </br>
Приложение прочтёт файл, запишет в переменную sz количество.</br>
sz = read(fd, c, 10);</br></br>
Закрытие файла</br>
if (close(fd) < 0)</br>
{</br>
perror("close file error:");</br>
exit(1);</br>
}</br></br>
