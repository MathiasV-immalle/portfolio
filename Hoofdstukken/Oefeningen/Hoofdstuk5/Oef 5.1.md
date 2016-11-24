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
