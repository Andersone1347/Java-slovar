# Java-slovar

### Зарезервированные слова в Java


## Примитивные типы
# целые числа   
byte - 8 бит
short - 16 бит   
int - 32 бита, или 4 байт  
long - 64 бита или 8 байт  
---
# числа с плавающей точкой        
float      
double     
# Логический
boolean    
# Символьный
char
--- 
void         

## Циклы и ветвления
if      
else       
switch     
case      
default      
while     
do      
for     
break      
continue     

## Исключения
try
catch
finally
throw
throws

## Области видимости
private
protected
public

## Работа с классами
class         
interface      
enum       
import        
package       
extends     
implements      
static        
final         
abstract         
default          

## Работа с объектами и переменными
new
instanceof
this
super
return
var (начиная с Java 10)

## Многопоточность
synchronized
volatile

## Разное
native
transient
assert
strictfp

## Зарезервированы, но не используются
const
goto

## Не ключевые слова
Константы **true**, **false** и **null** формально не относятся к ключевым словам. Однако, обладают всеми их особенностями. Вы не можете назвать метод **true** или переменную **false**. Компилятор такой код не поймет и компилировать его не будет.


*return* - используют для выполнения явного выхода из метода. Оператор можно использовать в любом месте метода для возврата управления тому объекту, который вызвал данный метод. Таким образом, **return** прекращает выполнение метода, в котором он находится.
```

```




Терминология на примере.
*1*
```
public class Main {
    public static void main(String[] args) {
        Person person1 = new Person();
        person1.name = "валера";
        person1.age = 50;
        person1.speak();
        Person person2 = new Person();
        person2.name = "vova";
        person2.age = 20;
        person1.sayHello();
    }
}
class Person {
    String name;
    int age;
    void speak() {
        for (int i = 0; i < 3; i++) {
            System.out.println("Меня зовут " + name + " Мне " + age + " лет");
        }
    }
    void sayHello() {
        System.out.println("Привет! ");
    }
}
//Меня зовут валера Мне 50 лет
//Меня зовут валера Мне 50 лет
//Меня зовут валера Мне 50 лет
//Привет! 
```
*speak(),void sayHello()* - Свой метод.  *()* -  Параметры метода     
*System.out.println("Привет! ")* - Вывод.   
*class Person{}* - класс.   
*Person person1 = new Person();*  *person1* - Объект класса Person.
class Person {*String name*; *int age*;} - Поля.
*void* - (это тип данных)Ключевое слово **void** указывает на то, что метод ничего не возвращает. Затем идут название метода - **main** и в скобках параметры метода - **String [] args**. И в фигурные скобки заключено тело метода - все действия, которые он выполняет.
### Методы



# contains() – это метод Java, позволяющий проверить, содержит ли String другую подстроку или нет.
```
public class Main {
    public static void main(String args[]) {
        String str1 = "Java string contains If else Example";
        // In If-else statements you can use the contains() method
        if (str1.contains("example")) {
            System.out.println("The Keyword :example: is found in given string");
        } else {
            System.out.println("The Keyword :example: is not found in the string");
        }
    }
}
//The Keyword :example: is not found in the string
//(not потому что, есть только с большой буквы)
```

# parseInt() – в Java используется для получения примитивного типа данных определенной строки, другими словами – преобразует строку в число.
```
public class Main{ 

   public static void main(String args[]){
      int x = Integer.parseInt("9");
      double c = Double.parseDouble("5");
      int b = Integer.parseInt("444",16);

      System.out.println(x);
      System.out.println(c);
      System.out.println(b);
   }
}
//9
//5.0
//1092
```

## Для класса Scanner
# NextLine()         
нужен для получения и чтения данных, написанных пользователем. Этот метод читает и воспроизводит данные до конца строки. Другими словами, он может считывать информацию до тех пор, пока не начнется новая строка или старая не будет разорвана с помощью **\n** или **Enter**.
```
import java.util.Scanner;

public class test {

    public static void main(String[] args) {

        Scanner scanner = new Scanner("Люблю тебя, Петра творенье,\n" +
                "Люблю твой строгий, стройный вид,\n" +
                "Невы державное теченье,\n" +
                "Береговой ее гранит");
        String s = scanner.nextLine();
        System.out.println(s);
    }
}
//Люблю тебя, Петра творенье,
```
```
public class Main {

   public static void main(String[] args) {

       Scanner scanner = new Scanner("Люблю тебя, Петра творенье,\n" +
               "Люблю твой строгий, стройный вид,\n" +
               "Невы державное теченье,\n" +
               "Береговой ее гранит");
       String s = scanner.nextLine();
       System.out.println(s);
       s = scanner.nextLine();
       System.out.println(s);
       s = scanner.nextLine();
       System.out.println(s);
       s = scanner.nextLine();
       System.out.println(s);
   }
}
//Люблю тебя, Петра творенье,
//Люблю твой строгий, стройный вид,
//Невы державное теченье,
//Береговой ее гранит
```
Каждый раз наш сканер будет делать один шаг вперед и считывать следующую строку.      

# nextInt() 
считывает и возвращает введенное число. В нашей программе он используется для того, чтобы присвоить значение переменной number.
```
public class Main {

   public static void main(String[] args) {

       Scanner sc = new Scanner(System.in);
       System.out.println("Введите число:");

       int number = sc.nextInt();

       System.out.println("Спасибо! Вы ввели число " + number);

   }
}
//Введите число:
//9
//Спасибо! Вы ввели число 9
```
# hasNextInt()
```
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.println("Введите число:");
        if (sc.hasNextInt()) {
            int number = sc.nextInt();
            System.out.println("Спасибо! Вы ввели число " + number);
        } else {
            System.out.println("Извините, но это явно не число. Перезапустите программу и попробуйте снова!");
        }
    }
}
//Введите число:
//6+
//Извините, но это явно не число. Перезапустите программу и попробуйте снова!
```

