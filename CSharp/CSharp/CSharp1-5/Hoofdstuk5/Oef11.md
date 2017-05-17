# Oefening 5.11: Tijd in uren-minuten-seconden naar seconden method

```C#
using System;

public class Program
{
    private static int TijdInSec(int a, int b, int c)
    {
        int Seconden = a * 3600 + b * 60 + c;
        return Seconden;
    }

    public static void Main()
    {
        int Seconden = TijdInSec(1, 1, 2);
        Console.WriteLine(Seconden);
    }
}
```
