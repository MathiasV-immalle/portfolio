<<<<<<< HEAD
# Oefening 5.1: ToonNaam method
```
using System;

public class Program
{
    private static string ToonNaam(string naam)
    {
        naam = "Mathias";
        Console.WriteLine(naam);
        return naam;
    }

    public static void Main()
    {
        // Oplossing 1
        string naam = "Mathias";
        Console.WriteLine("Hello {0}", naam);

        // Oplossing 2
        ToonNaam("Mathias");
    }
}
```
=======
# Oefening 5.9: Volume kubus method

```
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
>>>>>>> ce858986e601af1367bbabf2aec4fcb47a6c94e7
