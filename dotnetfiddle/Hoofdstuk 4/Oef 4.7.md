# Oefening 4.7: Seconden naar uren, minuten en seconden method

using System;

public class Program
{
    public static void Main()
    {
        int totaalSeconden = 2549;
        int totaalAantalUren = totaalSeconden / 3600;
        int overigeSeconden = totaalSeconden % 3600; 
        int totaalAantalMinuten = overigeSeconden / 60;
        int totaalOverigeSeconden = overigeSeconden % 60;

        Console.WriteLine("2549 seconden = {0} uur, {1} minuten en {2} seconden.", totaalAantalUren, totaalAantalMinuten, totaalOverigeSeconden);   
    }
}
