### Листеренко Ольга Руслановна ###
### БПИ 217 ###
  
### Вариант 29 ###
### Задача ###
Разработать программу, которая ищет в ASCII-строке слова — палиндромы и формирует из них новую строку, в которой слова разделяются пробелами. Слова состоят из букв. Все остальные символы являются разделителями слов.  
    
### Тесты ###
Все программы выдают одинаковый результат и были протестированы на следующих примерах:  
#### 1 тест ####
  
  
##### Результат (одинаковый во всех программах) #####
  

#### 2 тест ####
  
##### Результат (одинаковый во всех программах) #####
  

#### 3 тест ####
  
##### Результат (одинаковый во всех программах) #####
  

#### 4 тест ####
  
##### Результат (одинаковый во всех программах) #####
  
    
### Программа на C ###
Код находится в папке Code_in_C.  
  
### Оптимизированная программа на ассембелере с комментариями ### 
Код находится в папке Assembly_modified.  
   
### Программа на ассембелере от компилятора ### 
Код находится в файле Assembly_from_C.  
Код получен путем компиляции кода на C следующим образом:  
gcc -masm=intel -fno-asynchronous-unwind-tables -fno-jump-tables -fno-stack-protector -fno-exceptions ./file_name.c -S -o ./file_name.s
  
### Информация, подтверждающая выполнение задания на 8 ###
Приведен код на C на оценку 8.  
Добавлены комментарии.  
Удалены из конца кода строки ниже ret, а из начала информация о файле, из которой получили код на ассемблере.  
Убраны лишние макросы, в том числе endbr64.    
Удалены cdqe и nop, добавленные компилятором для дополнения.  
Удалены промежуточные присваивания на подобии:  
<img width="151" alt="image" src="https://user-images.githubusercontent.com/57359954/200162263-9bbf45f8-cef4-4c22-a298-bba1cd8c2154.png">  
<img width="180" alt="image" src="https://user-images.githubusercontent.com/57359954/200162287-fd5b32b1-9454-4762-a81c-19b18b748944.png">  
или  
<img width="206" alt="image" src="https://user-images.githubusercontent.com/57359954/200162943-fcd441b2-3f04-4593-894f-d792313ba688.png">  
<img width="184" alt="image" src="https://user-images.githubusercontent.com/57359954/200162977-5a3a157a-adde-41ab-81ab-32c99dbe74d8.png">  
или  
<img width="204" alt="image" src="https://user-images.githubusercontent.com/57359954/200165522-b875b501-484c-48f3-afde-2f32024b0bb1.png">  
<img width="205" alt="image" src="https://user-images.githubusercontent.com/57359954/200165560-70d15e6e-c221-4955-947d-85e72592cc69.png">  
или  
<img width="229" alt="image" src="https://user-images.githubusercontent.com/57359954/200772055-505ef661-547a-4cee-b09e-61b2be62f3d8.png">  
<img width="230" alt="image" src="https://user-images.githubusercontent.com/57359954/200772189-1ac31128-dd15-45fa-8642-7b107632555c.png">    
Программа протестирована на приведенных тестах. Результаты совпадают с результатами программы на C.  
В программе использованы функции ввода и формирования, вывода, получающие на вход n (число элементов в массивах).  
Использованы локальные переменные n и i.  
Добавлены комментарии о передаче параметров (фактических и формальных).
Программа протестирована на приведенных тестах. Результаты совпадают с результатами программы на C.  
-4[rbp] заменен на регистр r12d. В основной программе и в generate это i.  
-28[rbp] заменен на регистр r13d. В основной программе это choice.  
-48[rbp] заменен на регистр r14. В основной программе это argv.  
myfile[rip] заменен на регистр r12.  
Комментарии об использовании регистров добавлены.  
Программа протестирована на приведенных тестах. Результаты совпадают с результатами программы на C и программы на ассемблере на 5.  
Добавлен файл Task_Registers.s с использованием регистров на оценку 6.
