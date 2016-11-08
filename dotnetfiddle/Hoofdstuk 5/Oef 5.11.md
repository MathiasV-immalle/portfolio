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
# Oefening 5.11: Tijd in uren-minuten-seconden naar seconden method

```
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
>>>>>>> ce858986e601af1367bbabf2aec4fcb47a6c94e7
