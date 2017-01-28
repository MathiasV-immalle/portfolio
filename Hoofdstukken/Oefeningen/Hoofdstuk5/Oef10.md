# Oefening 5.10: Opp. cirkel method

```C#
using System;

public class Program
{
    private static double OppCirkel(double r)
    {
        double opp = r * r * Math.PI;
        return opp;
    }

    public static void Main()
    {
        double opp = OppCirkel(1.25);
        Console.WriteLine(opp);
    }
}
```
