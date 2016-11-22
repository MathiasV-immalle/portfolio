# Oefening: RaadHetGetal-Game

```
using System;

namespace ConsoleApplication
{
    public class Program
    {
        public static void Main(string[] args)
        {
            Random rndGen = new Random();
            int g = rndGen.Next(0, 100);
            int gok = 100;
            int aantalBeurten = 0;

            while(gok != g) {
                Console.Write("Raad het getal: ");
                string invoer = Console.ReadLine();
                gok = Convert.ToInt32(invoer);
                aantalBeurten++;

                if(gok < g) {
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.WriteLine("Het getal is groter!");
                    Console.ResetColor();
                } else { if(gok > g)
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.WriteLine("Het getal is kleiner!");
                    Console.ResetColor();
                } 
                if(gok == g) { 
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.WriteLine("Proficiat, u heeft het getal {0} gevonden in {1} beurten!", g, aantalBeurten);
                    Console.ResetColor();   
                }
            }
        }
    }
}
```
