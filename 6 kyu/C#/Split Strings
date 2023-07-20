# CodeWars C# Solutions

---

## Split Strings


**Definition**

Complete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

Examples:

* 'abc' =>  ['ab', 'c_']

* 'abcdef' => ['ab', 'cd', 'ef']

---

### Solution

```c#
using System;
using System.Collections.Generic;
public class SplitString
{
  public static string[] Solution(string str)
  {
    if (str.Length % 2 != 0)str += "_";
    List<string> subStrings = new List<string>();
    for (int i = 0; i < str.Length; i += 2)subStrings.Add(str.Substring(i, 2));
    return subStrings.ToArray();
  }
}
```

---


[See on CodeWars.com](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001/solutions/csharp?filter=me&sort=best_practice&invalids=false)
