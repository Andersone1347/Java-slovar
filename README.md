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
# charAt() - поиск по индексу.
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("javaYgeZaibala");
        String rus2 = "javaYgeZaibala";

        System.out.println(rus.charAt(1));
        System.out.print(rus2.charAt(12));
    }
}
//a
//l
```
# compareTo() - в Java сравнивает вызывающий объект с объектом, переданным в качестве параметра, и возвращает в результате выполнения сравнения целое число:    
- положительное, если вызывающий объект больше объекта, переданного в качестве параметра;
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java!");
        String rus2 = "java";
        System.out.println(rus.compareTo(rus2));
    }
}
//1
```
- отрицательное, если вызывающий объект меньше объекта, переданного в качестве параметра;
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "javawe";
        System.out.println(rus.compareTo(rus2));
    }
}
//-2
```
- нуль, если объекты равны.
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "java";
        System.out.println(rus.compareTo(rus2));
    }
}
//0
```
пример c разным регистром
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "JavA";
        System.out.println(rus.compareTo(rus2));
    }
}
//32
```
# concat()- в Java объединяет строки, путем добавления одной строки в конец к другой. 
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "1347";
        int a = 47;
        String s = String.valueOf(a);

        System.out.println(rus.concat(s));
    }
}
//java47
```
 # equals() - метод проверяет два объекта одного происхождения на логическую равность.
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "java";
        int a = 47;
        String s = String.valueOf(a);

        System.out.println(rus.equals(rus2));
        System.out.println(rus.equals(s));
    }
}
//true
//false
```

# hashCode() возвращает числовое значение фиксированной длины для любого объекта.
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "java";
        int a = 47;
        String s = String.valueOf(a);

        System.out.println(rus.hashCode());
        System.out.println(rus2.hashCode());
        System.out.println(s.hashCode());
    }
}
//3254818
//3254818
//1667
```

# indexOf(int ch)- возвращает индекс в данной строке первого вхождения указанного символа. Другими словами, мы получим номер первого вхождения заданного символа, считая слева-направо.
```
public static void main(String[] args) {
   String str = "Diego, where is my money?";
   int value = str.indexOf('e');
   System.out.println(value);
}
//2
```
Если же символ который мы ищем, отсутствует в данной строке, мы получим -1.
```
public static void main(String[] args) {
   String str = "Diego, where is my money?";
   int value = str.indexOf('j');
   System.out.println(value);
}
//-1
```
# isEmpty() - 	Проверяет, пустая ли строка.     
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "";
        int a = 47;
        String s = String.valueOf(a);

        System.out.println(rus.isEmpty());
        System.out.println(rus2.isEmpty());
        System.out.println(s.isEmpty());
    }
}
//false
//true
//false
```

# length () - возвращает длину последовательности символов, представленного этим объектом.
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("java");
        String rus2 = "";
        int a = 47;
        String s = String.valueOf(a);

        System.out.println(rus.length());
        System.out.println(rus2.length());
        System.out.println(s.length());
    }
}
//4
//0
//2
```

# substring() возвращаемое значение заданно подстрокой   
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("lol kek oooooo lol zaiy");
        String rus2 = "";
        int a = 47;
        String s = String.valueOf(a);


            System.out.println(rus.substring(15,22));

    }
}
// lol zai
```

 # valueOf() – возвращает соответствующий числовой объект, содержащий значение переданного аргумента, простыми словами – преобразует в нужный тип данных. Аргумент можно преобразовать в int, double, float и другие типы данных, например, можно преобразовать строку в число. Метод valueOf() в Java является статическим методом.
```
public class Test{ 

   public static void main(String args[]){
      
      Integer x = Integer.valueOf(9);
      Double c = Double.valueOf(5);
      Float a = Float.valueOf("80");               

      Integer b = Integer.valueOf("444",16);

      System.out.println(x); 
      System.out.println(c);
      System.out.println(a);
      System.out.println(b);
   }
}
9
5.0
80.0
1092
```


# toCharArray() – в Java преобразует данную строку в новый массив символов.
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("lol zaiy");
        String rus2 = "";
        int a = 47;
        String s = String.valueOf(a);

        char [] ch = rus.toCharArray();
        for (char elem: ch) {
        System.out.println(elem);
        }
        }
    }
//l
//o
//l
// 
//z
//a
//i
//y
```
# toLowerCase() возвращает строку, преобразованную в нижний регистр.
```
public class Test {

   public static void main(String args[]){
      String Str = new String("Добро пожаловать на ProgLang.su");

      System.out.print("Возвращаемое значение: ");
      System.out.println(Str.toLowerCase());
      
      System.out.print("Возвращаемое значение: ");
      System.out.println(Str.toLowerCase(Locale.ENGLISH));
   }
}
//Возвращаемое значение: добро пожаловать на proglang.su
//Возвращаемое значение: добро пожаловать на proglang.su
```

# trim() возвращает копию данной строки, в которой удаляются начальные и конечные пробелы, или данную строку, если она не имеет начальных или конечных пробелов.
```
import java.io.*;

public class Test {

   public static void main(String args[]){
      String Str = new String("   Добро пожаловать на ProgLang.su   ");

      System.out.print("Возвращаемое значение: ");
      System.out.println(Str.trim());
   }
}
```
//Возвращаемое значение: Добро пожаловать на ProgLang.su

# toUpperCase() возвращает строку, преобразованную в верхний регистр.
```
import java.util.Locale;

public class Test {

   public static void main(String args[]){
      String Str = new String("Добро пожаловать на ProgLang.su");

      System.out.print("Возвращаемое значение: ");
      System.out.println(Str.toUpperCase());
      
      System.out.print("Возвращаемое значение: ");
      System.out.println(Str.toUpperCase(Locale.ENGLISH));
   }
}
// Возвращаемое значение: ДОБРО ПОЖАЛОВАТЬ НА PROGLANG.SU
// Возвращаемое значение: ДОБРО ПОЖАЛОВАТЬ НА PROGLANG.SU

```


# split в Java разделяет строку на подстроки, используя разделитель, который определяется с помощью регулярного выражения. 
```
public  class Ari {
    public static void main(String[] args) {
        String rus = new String("lol kek oooooo lol zaiy lol lo lo ol");
        String rus2 = "";
        int a = 47;
        String s = String.valueOf(a);

        String [] valas = rus.split("lol");
        for (String element: valas){
            System.out.println(element);
        }
    }
}
// kek oooooo 
// zaiy 
// lo lo ol
```

# compareToIgnoreCase() – в Java сравнивает лексически две строки, игнорируя регистр букв.
```
public class Test {

   public static void main(String args[]) {
      String str1 = "Я буду хорошим программистом!";
      String str2 = "Я Буду Хорошим Программистом!";
      String str3 = "Я буду хорошим дворником!";

      int result = str1.compareToIgnoreCase(str2);
      System.out.println(result);
	  
      result = str2.compareToIgnoreCase(str3);
      System.out.println(result);
	 
      result = str3.compareToIgnoreCase(str1);
      System.out.println(result);
   }
}
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

**Инициализация** переменной или массива означает явное (или неявное) установление некоторого значения переменной.


# Сокращённая запись арифметических операторов

Для экономии времени предусмотрена сокращённая запись арифметических операторов.
```
x += y;    // То же самое, что и x = x + y;
x -= y;    // То же самое, что и x = x - y;
x *= y;    // То же самое, что и x = x * y;
x /= y;    // То же самое, что и x = x / y;
x %= y;    // То же самое, что и x = x % y;
```

# System.out.format

Пример: [JavaRush](https://javarush.com/groups/posts/1412-formatiruem-vihvod-chisel-v-java)


##### Stepic

Методы строк

Класс String имеет множество встроенных методов для обработки строк. Разберём некоторые из них.

Общий синтаксис для всех методов выглядит так:

stringName.nameOfMethod();
Здесь метод nameOfMethod применяется к строке stringName и вызывается с помощью круглых скобок. Внутри круглых скобок в некоторых методах должны быть обязательные аргументы, а в некоторых других - нет.

1. Длина строки (количество символов).
```
str.length();      // возвращает длину строки str (количество символов, включая пробелы)

String word = "Java is strong";
int x = word.length();
System.out.println(x); // 14
 ```

2. Сравнение строк.

В Java строки нельзя сравнивать с помощью операторов сравнения, таких как == и !=. Вернее, сравнивать-то можно, но результат Вас удивит ;) Для корректного сравнения строк необходимо использовать специальный метод:

str1.equals(str2); // Сравнивает строки str1 и str2
Этот метод является булевым, то есть возвращает true, если строки равны, и false, если нет.
```
String word1 = "Java";
String word2 = "Python";
System.out.println(word1.equals(word2)); // false

String word3 = "Ja";
String word4 = "va";
boolean result = word1.equals(word3 + word4); 
System.out.println(result); // true
 ```

3. Получение индекса элемента в строке.

Метод indexOf() ищет в строке заданный символ (или строку), и возвращает  индекс его первого вхождения. Если элемент не найден, метод возвращает -1.
```
String word = "abracadabra";
int x = word.indexOf('b');
System.out.println(x); // 1

int y = word.indexOf('Z');
System.out.println(y); // -1
 ```

4. Получение элемента строки по его индексу.

Для этого используется метод charAt():
```
String word = "abracadabra";

char letter_0 = word.charAt(0);
System.out.println(letter_0); // a

char letter_4 = word.charAt(4);
System.out.println(letter_4); // c
```
Обратите внимание - метод возвращает значение типа char, а не String. Индексация, как обычно, начинается с нуля.

 

5. Проверка строки на пустоту.

Метод isEmpty() является весьма полезным инструментом. Он возвращает false, если строка содержит какие-либо элементы (пробел - тоже элемент), и true - если строка пустая, т.е. не содержит ни одного элемента.
```
String str1 = "Hubba Bubba";
String str2 = "   ";
String str3 = "";

boolean value1 = str1.isEmpty(); // false
boolean value2 = str2.isEmpty(); // false
boolean value3 = str3.isEmpty(); // true
 ```

6. Одна строка внутри другой

Чрезвычайно полезный метод contains() проверяет, содержится ли одна строка внутри другой, и возвращает соответствующее логическое значение - true или false.
```
String str1 = "One Two Three";
String str2 = "One";
String str3 = "Four";

boolean value1 = str1.contains(str2); // true
boolean value1 = str1.contains(str3); // false
 
```
7. Преобразование регистров.

Методы  toUpperCase() / toLowerCase() приводят всю строку в верхний и нижний регистр соответственно.
```
String s = "I'll be back";

System.out.println(s.toLowerCase()); // i'll be back
System.out.println(s.toUpperCase()); // I'LL BE BACK
 
```
8. Представление числа в строковом формате.

Иногда полезно работать не с числом, а с его представлением в виде строки. Для этого Java предоставляет метод toString(). Чтобы использовать этот метод, нужно воспользоваться классом - обёрткой Integer. Сделать это можно разными путями.
```
int n = 12345;                      // Это число типа int
System.out.println(n);              // 12345 

String str1 = Integer.toString(n);  // Это строка
System.out.println(str1);           // 12345

Integer num = n;                    // Это число-объект класса Integer
System.out.println(num);            // 12345

String str2 = num.toString();        // Это строка
System.out.println(str2);            // 12345
 
```
На самом деле, метод toString является мощным инструментом, который широко используется, однако мы пока ограничимся небольшой частью его функционала.

 

9. Преобразование строки в число.

Метод, обратный предыдущему - valueOf() преобразует строку в число нужного типа.
```
String str = "12345";
Integer num = Integer.valueOf(str);  // num - объект класса Integer
System.out.println(num);             // 12345

int num1 = num;                      // num1 - переменная типа int
System.out.println(num1);            // 12345
```
Поскольку оба метода (toString() и valueOf()) - это методы класса Integer, то именно с объектами этого класса их и необходимо использовать. Подробнее о типах переменных и их взаимоотношениях мы коснёмся в следующих модулях.

Есть и ещё один, более простой метод преобразования строки в число - parseInt(), также принадлежащий классу Integer.
```
String str = "12345";

int num = Integer.parseInt(str);    //num - переменная типа int
System.out.println(num);            //12345
Если нужно преобразовать строку в число с плавающей точкой, можно использовать соответствующий метод из класса Double.

String str = "12345";

double num = Double.parseDouble(str);    //num - переменная типа double
System.out.println(num);                 //12345.0
 ```

10. Создание подстроки.

Метод substring() возвращает новую строку, которая является подстрокой данной строки. Подстрока начинается с символа, заданного индексом, и продолжается до конца данной строки или до указанного индекса.
```
String str = "Добро пожаловать в мир Java!";

System.out.println(str.substring(6));         //пожаловать в мир Java!

System.out.println(str.substring(6, 15));     //пожаловат
 ```

11. Замена элементов строки.

Несмотря на то, что строки в Java являются неизменяемыми (immutable), всё-таки их можно изменять с помощью специального метода replace(), который может заменить один символ на другой. Этот метод не изменяет строку, а собирает новую по заданным параметрам. Метод принимает два обязательных параметра - символ, подлежащий замене, и символ, на который его нужно заменить.
```
String str = "Добро пожаловать в мир Java!";

System.out.println(str.replace('о', 'А')); //ДАбрА пАжалАвать в мир Java!
Обратите внимание - метод работает с заменой символов (char), о чём говорят одинарные кавычки.
```
 