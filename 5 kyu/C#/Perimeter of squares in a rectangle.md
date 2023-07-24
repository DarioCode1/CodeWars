# CodeWars C# Solutions

---

## Perimeter of squares in a rectangle


**Definition**

The drawing shows 6 squares the sides of which have a length of 1, 1, 2, 3, 5, 8. It's easy to see that the sum of the perimeters of these squares is : 4 * (1 + 1 + 2 + 3 + 5 + 8) = 4 * 20 = 80 

Could you give the sum of the perimeters of all the squares in a rectangle when there are n + 1 squares disposed in the same manner as in the drawing:

![image](https://github.com/DarioCode1/CodeWars/assets/118449641/9bb4109a-d6b8-4bb7-8136-361cc01a09f4)

alternative text

Hint:
See Fibonacci sequence

Ref:
http://oeis.org/A000045

The function perimeter has for parameter n where n + 1 is the number of squares (they are numbered from 0 to n) and returns the total perimeter of all the squares.

perimeter(5)  should return 80

perimeter(7)  should return 216

---

### Solution


```c#
using System;
using System.Numerics;

public class SumFct
{
  public static BigInteger perimeter(BigInteger n) 
  {
    int size = (int)n+2;
    BigInteger sum = 0;
    BigInteger[] fibonacciNumbers = new BigInteger[size];
    if (n >= 1) fibonacciNumbers[0] = 0;
    if (n >= 2) fibonacciNumbers[1] = 1;
    for (int i = 2; i < size; i++) fibonacciNumbers[i] = fibonacciNumbers[i - 1] + fibonacciNumbers[i - 2];
    for (int i = 0; i < fibonacciNumbers.Length; i++) sum += fibonacciNumbers[i];
    return sum * 4;
  }
}
```

---


[See on CodeWars.com](https://www.codewars.com/kata/559a28007caad2ac4e000083/solutions/csharp?filter=me&sort=best_practice&invalids=false)
