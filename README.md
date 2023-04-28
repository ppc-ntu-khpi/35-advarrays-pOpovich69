## Завдання №5
### Обчислити суму елементів матриці розміром N x M

### клас Calc
```java
import java.util.Random;
import java.util.stream.IntStream;

public class Calc {
    final private int N = 3;
    final private int M = 3;

    public void SumOfArray(){
        int[][] myArray = RandomNumbers(new int[N][M]);
        ArrayOutput(myArray);
        int sum = 0;
        for (int i = 0; i < myArray.length; i++){
            sum += IntStream.of(myArray[i]).sum();
        }
        System.out.print("Sum of array = " + sum);
    }
    private int[][] RandomNumbers(int[][] arr){
        Random random = new Random();
        int min = 1;
        int max = 100;
        for (int i = 0; i < arr[0].length; i++){
            for (int j = 0; j < arr[1].length; j++){
                arr[i][j] = random.nextInt(min, max);
            }
        }
        return arr;
    }
    private void ArrayOutput(int[][] arr){
        System.out.println("Array");
        for (int i = 0; i < arr[0].length; i++){
            for (int j = 0; j < arr[1].length; j++){
                System.out.print(arr[i][j] + " ");
            }
            System.out.print("\n");
        }
    }
}
```
### клас Main
```java 
import java.util.Arrays;

public class Main {

    public static void main(String[] args) {
        Calc calc = new Calc();
        calc.SumOfArray();
    }
}
```

### Результат роботи програми 
<img src="https://github.com/ppc-ntu-khpi/35-advarrays-pOpovich69/blob/master/img/1.png">
