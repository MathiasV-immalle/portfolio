# Oefening 5.9: Volume kubus method

```C#
using System;

public class Program
{
    private static double KubusVolume(double z)
    {
        double volume = z * z * z;
        return volume;

    }

    public static void Main()
    {
        double z = 1.2;
        double volume = KubusVolume(1.2);
        Console.WriteLine("De kubus met straal {0} heeft {1} als volume", z, volume);
    }
}
```
