# recursiveFunctions
recursive function solutions in java
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
### Girilen sayı dizisinin elamanlarını rekürsif şekilde toplamını bulan method;

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




