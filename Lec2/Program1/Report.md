# Program1 <br>
## Описание работы программы <br>

Размер массива, указывается его длина.\
printf("Enter length of array: ");\
scanf("%d", &length);
\
Выделение памяти для массива.\
Функция malloc возвращает NULL в случае, если не удалось выделить память для массива.\
if ((array = (int * ) malloc(length * sizeof(int))) != NULL)\
\
Вывод количества байтов, выделенных для памяти массива.\
printf("Allocated %lu bytes\n", length * sizeof(* array));*\

Программа очистит выделенную для массива память (в случае, если ошибок не произошло).\
if (array != NULL)\
{\
free(array);\
}
