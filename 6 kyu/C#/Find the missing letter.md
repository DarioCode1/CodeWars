# CodeWars C# Solutions

---

## Find the missing letter


**Definition**

Write a method that takes an array of consecutive (increasing) letters as input and that returns the missing letter in the array.

You will always get an valid array. And it will be always exactly one letter be missing. The length of the array will always be at least 2.
The array will always contain letters in only one case.

Example:

['a','b','c','d','f'] -> 'e'

['O','Q','R','S'] -> 'P'

(Use the English alphabet with 26 letters!)

---

### Solution


```c#
using System;
public class Kata
{
  public static char FindMissingLetter(char[] array)
  {
    char[] alphabetUpper = new char[26]
        {
            'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M',
            'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'
        };
    char[] alphabetLower = new char[26]
        {
            'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
            'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'
        };
    if (char.IsUpper(array[0]))
      {
      for (int i = 0;i<array.Length;i++)
        {
        if (array[i] != alphabetUpper[Array.IndexOf(alphabetUpper,array[0])+i]) return alphabetUpper[Array.IndexOf(alphabetUpper,array[0])+i];
      }
    }
    else
      {
      for (int i = 0;i<array.Length;i++)
        {
        if (array[i] != alphabetLower[Array.IndexOf(alphabetLower,array[0])+i]) return alphabetLower[Array.IndexOf(alphabetLower,array[0])+i];
      }
    }
   return ' ';
    }
  }
```

---


[See on CodeWars.com](https://www.codewars.com/kata/5839edaa6754d6fec10000a2/solutions/csharp?filter=me&sort=best_practice&invalids=false)
