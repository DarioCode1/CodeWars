# CodeWars C# Solutions

---

## Find the unique number


**Definition**

There is an array with some numbers. All numbers are equal except for one. Try to find it!

findUniq([ 1, 1, 1, 2, 1, 1 ]) === 2

findUniq([ 0, 0, 0.55, 0, 0 ]) === 0.55

It’s guaranteed that array contains at least 3 numbers.

The tests contain some very huge arrays, so think about performance.

---

### Solution


```c#
using System.Collections.Generic;
using System.Linq;

public class Kata
{
  public static int GetUnique(IEnumerable<int> numbers)
  {
    List<int> numbersList = numbers.ToList();
    if ((numbersList[0] != numbersList[1]) && (numbersList[0] != numbersList[2])) return numbersList[0];
    for (int i = 1; i < numbersList.Count-1;i++)
      {
      if ((numbersList[i] != numbersList[i-1]) && (numbersList[i] != numbersList[i+1])) return numbersList[i];
    }
    return numbersList[numbersList.Count-1];
  }
}
```

---


[See on CodeWars.com](https://www.codewars.com/kata/585d7d5adb20cf33cb000235/solutions/csharp?filter=me&sort=best_practice&invalids=false)
