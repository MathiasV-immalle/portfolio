# Oefening 5.8: Wisselkoers euro - dollar / dollar - euro method

```
using System;

public class Program
{
    private static double EuroEquivalent(double dollar)
    {
        double centjes = dollar * 0.91;
        return centjes;
    }

    private static double DollarEquivalent(double euro)
    {
        double wissel = euro * 1.0986;
        return wissel;
    }
    public static void Main()
    {
        double dollar = 4000.01;
        double euro = EuroEquivalent(dollar);
        Console.WriteLine("{0} dollar is gelijk aan {1} euro", dollar, euro);

        Console.WriteLine(" ");

        double euro2 = 3640.01;
        double dollar2 = DollarEquivalent(euro2);
        Console.WriteLine("{0} euro is gelijk aan {1} dollar", euro2, dollar2);
    }
}
```
