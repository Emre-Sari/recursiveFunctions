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
}```
