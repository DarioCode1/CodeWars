# CodeWars C# Solutions

---

## Write Number in Expanded Form


Write Number in Expanded Form
You will be given a number and you will need to return it as a string in Expanded Form. For example:

Kata.ExpandedForm(12); # Should return "10 + 2"

Kata.ExpandedForm(42); # Should return "40 + 2"

Kata.ExpandedForm(70304); # Should return "70000 + 300 + 4"

NOTE: All numbers will be whole numbers greater than 0.
---

### Solution


```c#
using System;
public static class Kata 
{
    public static string ExpandedForm(long num) 
    {
      string str = num.ToString();
      string result = "";
      for (int i = 0;i<str.Length;i++)
        {
        if (str[i]!= '0')
          {
          result += str[i];
          for (int j = 0; j<str.Length-i-1;j++) result += '0';
          result += " + ";
        }
      }
      return result.Substring(0, result.LastIndexOf(" + "));
    }
}
```

---


[See on CodeWars.com](https://www.codewars.com/kata/5842df8ccbd22792a4000245/solutions/csharp?filter=me&sort=best_practice&invalids=false)
