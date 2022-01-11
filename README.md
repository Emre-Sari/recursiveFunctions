# recursiveFunctions
recursive function solutions in java
### The method that finds how many digits the entered number has recursively;
### Girilen sayının kaç basamaklı olduğunu rekürsif şekilde bulan method;
```java
public class finddigitnumber_recurive {

    static int counter = 0;

    public static void main(String[] args) {
        System.out.println(count(334));
    }

    public static int count(int sayi) {
        if (sayi <= 0) {
            return counter;
        } else {
            counter += 1;
            return count(sayi / 10);
        }
    }
}
```
### The method that finds the recursive sum of the elements of the entered number sequence;
### Girilen sayı dizisinin elamanlarını rekürsif şekilde toplamını bulan method;
```java
public class totalofarray_recursive {

    static int total = 0;

    public static void main(String[] args) {
        int array[] = {3, 7, 1, -43, 54};
        int result = sum(array, 0);
        System.out.println(result);
    }

    public static int sum(int[] array, int indis) {
        if (indis == array.length) {
            return total;
        } else {
            total += array[indis];
            return sum(array, indis + 1);
        }
    }
}
```
### The method that finds the Fibonacci number in the entered number value recursively;
### Girilen sayı değerindeki fibonacci sayısını rekürsif şekilde bulan method;
```java
public class fibonacci_recursive {

    static long a = 1, b = 1, c = 0;

    public static void main(String[] args) {
        System.out.println(fibonacci(100, 2));
    }

    public static long fibonacci(int sayi, int indis) {
        if (indis == sayi) {
            return c;
        } else {
            c = a + b;
            a = b;
            b = c;
            return fibonacci(sayi, indis + 1);
        }
    }
}
```
### The method that writes the entered string in reverse recursive way;
### Girilen Stringi tersten rekürsif şekilde yazan method;
```java
public class writeinreverse_recursive {

    static String reverse = "";

    public static void main(String[] args) {
        String name = "emre";
        System.out.println(write(name, name.length() - 1));
    }

    public static String write(String str, int indis) {
        if (indis < 0) {
            return reverse;
        } else {
            reverse += str.charAt(indis);
            return write(str, indis - 1);
        }
    }
}
```
### Recursive method that finds how many 'a' and 'A' characters are in the entered String;
### Girilen String içinde kaç adet 'a' ve 'A' karakteri olduğunu rekürsif şekilde bulan method;
```java
public class howmanythereisA_recursive {

    static int counter = 0;

    public static void main(String[] args) {
        int found = count("amaArea", 0);
        System.out.println(found);
    }

    public static int count(String str, int indis) {
        if (indis == str.length()) {
            return counter;
        } else {
            if (str.charAt(indis) == 'a' || str.charAt(indis) == 'A') {
                counter += 1;
                return count(str, indis + 1);
            }
            return count(str, indis + 1);
        }
    }
}
```
### The method that recursively finds the largest integer in the entered array;
### Girilen dizideki en büyük tamsayıyı rekürsif şekilde bulan method; 
```java
public static void main(String[] args) {
        int array[] = {3, -44, 22, 4, 33, -5, 77};
        System.out.println(find(array[0], 0, array));
    }
    public static int find(int enb, int indis, int[] array) {
        if (indis == array.length) {
            return enb;
        } else {
            if (enb < array[indis]) {
                enb = array[indis];
                return find(enb, indis + 1, array);
            }
            return find(enb, indis + 1, array);
        }
    }
 

