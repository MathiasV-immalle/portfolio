# OpdrachtenSoftware: C# Dotnetfiddles

**Hoofdstuk 4**

- Oefening 4.7: Seconden naar uren, minuten en seconden method
```
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
```

- Oefening 4.9: Geldteruggave (Frisdrankautomaat) method

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

**Hoofdstuk 5**

- Oefening 5.1: ToonNaam method

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

- Oefening 5.8: Wisselkoers euro - dollar / dollar - euro method
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

- Oefening 5.9: Volume kubus method
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

- Oefening 5.10: Opp. cirkel method
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

- Oefening 5.11: Tijd in uren-minuten-seconden naar seconden method
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

