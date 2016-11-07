# Oefening 4.9: Geldteruggave (Frisdrankautomaat) method
```
using System;

public class Program
{
    public static void Main()
    {
        // Met veel RAM
            // Info
            int amountGiven = 100;
            int itemCost = 45;
            int moneyBack = amountGiven - itemCost;

            // Berekeningen
            int giveEuro = moneyBack / 100;
            moneyBack -= giveEuro * 100;

            int giveCent50 = moneyBack / 50;
            moneyBack -= giveCent50 * 50;

            int giveCent20 = moneyBack / 20;
            moneyBack -= giveCent20 * 20;

            int giveCent10 = moneyBack / 10;
            moneyBack -= giveCent10 * 10;

            int giveCent5 = moneyBack / 5;
            moneyBack -= giveCent5 * 5;

            int giveCent2 = moneyBack / 2;
            moneyBack -= giveCent2 * 2;

            int giveCent1 = moneyBack / 1;
            moneyBack -= giveCent1 * 1;

            // Weergave
            Console.WriteLine("De machine zal ");
            Console.WriteLine(giveEuro + " eurostukken, ");
            Console.WriteLine(giveCent50 + " vijftigcent stukken, ");
            Console.WriteLine(giveCent20 + " twintigcent stukken, ");
            Console.WriteLine(giveCent10 + " tiencent stukken, ");
            Console.WriteLine(giveCent5 + " vijfcent stukken, ");
            Console.WriteLine(giveCent2 + " tweecent stukken, ");
            Console.WriteLine(giveCent1 + " eencent stukken, ");
            Console.WriteLine("teruggeven.");
    }
}
```
