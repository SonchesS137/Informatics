### Лабораторная 1

### Задача

Модифицируйте файл `script.bash` так, чтобы при его запуске в терминале в виде

```
bash script.bash Vasya Pupkin
```

Вывод был

`Welcome, Vasya Pupkin`

*Hint:* Скрипт должен работать для любых имен, даже если это Benedict Timothy Carlton Cumberbatch.

### Решение

1. Открываем терминал Mac OS.

2. При попытке использовать код из задачи, понимаем, что надо в настройках терминала указать открытие Shell с помощью "bash".

  ![Снимок экрана 2024-09-20 в 17 22 33](https://github.com/user-attachments/assets/d2ae9ebb-5c82-44fb-b5fe-02bc5838d9ed)

3. Перезапускаем терминал и вводим представленный в лабораторной работе код.

4. Замечаем, что

  ```
     gedit script.bash
  ```

не работает для нашего терминала и устанавливаем "nano" :

  ```
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

   ![Снимок экрана 2024-09-20 в 17 32 37](https://github.com/user-attachments/assets/61152ad4-ce55-490e-9468-a4f135a8dee8)

  ```
     brew update
  ```

  ```
     brew install nano
  ```

  ```
     nano --version
  ```

  Если терминал выдал версию, смело работаем дальше.

  ![Снимок экрана 2024-09-20 в 17 36 05](https://github.com/user-attachments/assets/8f6e4969-2431-40f1-b950-c483eb9aeb57)

5. Изучив https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#OTHERTYPESV узнаем про специальные типы переменных и редактируем код:

  ![Снимок экрана 2024-09-20 в 17 55 39](https://github.com/user-attachments/assets/c8aeae46-39eb-4d45-b18b-92ed39a34480)

Нам нужны все аргументы, чтобы выводить имена различной длины и состоящие из нескольких слов, именно поэтому воспользовались 

  ```
    $@
  ```

6. Закрываем редактор и проверяем
   
  ![Снимок экрана 2024-09-20 в 18 06 59](https://github.com/user-attachments/assets/ad9a3c44-1e61-43c3-ab9a-7f59000d641d)
