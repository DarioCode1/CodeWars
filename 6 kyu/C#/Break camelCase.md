# CodeWars C# Solutions

---

## Break camelCase


**Definition**

Complete the solution so that the function will break up camel casing, using a space between words.

Example

"camelCasing"  =>  "camel Casing"
"identifier"   =>  "identifier"
""             =>  ""

---

### Solution


```c#
public class Kata
{
  public static string BreakCamelCase(string str)
  {
    string aux = str.ToLower();
    string result = str;
    int j = 0;
    for (int i = 0;i < aux.Length; i++)
      {
      if (aux[i] != str[i]) result  = result.Substring(0, i+j) + " " + result.Substring(i+j++);
    }
    return result;
  }
}
```

---


[See on CodeWars.com](https://www.codewars.com/kata/5208f99aee097e6552000148/solutions/csharp?filter=me&sort=best_practice&invalids=false)
