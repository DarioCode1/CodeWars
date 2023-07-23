# CodeWars C# Solutions

---

## Scramblies


**Definition**

Complete the function scramble(str1, str2) that returns true if a portion of str1 characters can be rearranged to match str2, otherwise returns false.

Notes:

Only lower case letters will be used (a-z). No punctuation or digits will be included.
Performance needs to be considered.

Examples:

scramble('rkqodlw', 'world') ==> True

scramble('cedewaraaossoqqyt', 'codewars') ==> True

scramble('katas', 'steak') ==> False

---

### Solution


```c#
using System;
public class Scramblies 
{   
  public static bool Scramble(string str1, string str2) 
    {
      bool result = true;
      if (str2.Length > str1.Length) return false;
      for (int i = 0; i < str2.Length;i++)
        {
        for (int j = 0; j < str1.Length;j++)
          {
          if (str2[i] == str1[j])
            {
            str1 = str1.Remove(j,1);
            break;
          }
          if (j == str1.Length-1) result = false;
        }
      }
      return result;
    }
}
```

---


[See on CodeWars.com](https://www.codewars.com/kata/55c04b4cc56a697bb0000048/solutions/csharp?filter=me&sort=best_practice&invalids=false)
