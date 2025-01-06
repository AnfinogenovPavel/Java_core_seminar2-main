# Java Core (семинары)

 ![Java core](https://github.com/AnfinogenovPavel/Java_core_seminar2-main/blob/main/src/main/resources/Java_core.jpg)

## Урок 2. Данные и функции

### Задача 1.

Написать метод, возвращающий количество чётных элементов массива. countEvens([2, 1, 2, 3, 4]) → 3 countEvens([2, 2, 0]) → 3 countEvens([1, 3, 5]) → 0


#### Решение

```java
import java.util.Random;


public class Task1 {
    public static int[] countEvens(int[] arrayOne) {
        Random random = new Random();
        int sum = 0;
        for (int i = 0; i < arrayOne.length; i++) {
            arrayOne[i] = random.nextInt(20);
            System.out.print("[" + arrayOne[i] + "] ");
            if (arrayOne[i] % 2 == 0) sum++;
        }
        System.out.println("\n" + "Количество четных элементов в первом массиве: " + sum);
        return arrayOne;

    }
}
```

---


### Задача 2.

Написать функцию, возвращающую разницу между самым большим и самым маленьким элементами переданного не пустого массива.

#### Решение

```java
import java.util.Random;


public class Task2 {
    public static int[] elementDifference(int[] arrayTwo) {
        Random random = new Random();
        int min = 30, max = 0;
        for (int i = 0; i < arrayTwo.length; i++) {
            arrayTwo[i] = random.nextInt(30);
            System.out.print("[" + arrayTwo[i] + "] ");
            if (arrayTwo[i] > max) {
                max = arrayTwo[i];
            } else if (arrayTwo[i] < min) {
                min = arrayTwo[i];
            }
        }
        int result = max - min;
        System.out.println("\n" + "Разница между самым большим и самым маленьким элементами второго массива: " + result);
        return arrayTwo;

    }
}
```

---


### Задача 3.

Написать функцию, возвращающую истину, если в переданном массиве есть два соседних элемента, с нулевым значением.

#### Решение

```java
import java.util.Random;

public class Task3 {
    public static int[] zeroElement(int[] arrayThree) {
        Random random = new Random();
        boolean elZero = false;
        for (int i = 0; i < arrayThree.length; i++) {
            arrayThree[i] = random.nextInt(2);
            System.out.print("[" + arrayThree[i] + "] ");
        }
        for (int j = 0; j < arrayThree.length; j++) {
            if (arrayThree[j] == 0) {
                if (arrayThree[j + 1] == 0 || arrayThree[j - 1] == 0) {
                    elZero = true;
                }
            }
        }
        System.out.println("\n" + "Наличие в третьем массиве двух соседних элементов с нулевым значением: " + elZero);
        return arrayThree;
    }
}
```

---
