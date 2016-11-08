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
# Oefening 5.10: Opp. cirkel method

```
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
>>>>>>> ce858986e601af1367bbabf2aec4fcb47a6c94e7
