# OpdrachtenSoftware: C# Dotnetfiddles

**Hoofdstuk 4**

- [Oefening 4.7: Seconden naar uren, minuten en seconden method](https://github.com/MathiasV-immalle/portfolio/blob/master/dotnetfiddle/Hoofdstuk%204/Oef%204.7.md)

- [Oefening 4.9: Geldteruggave (Frisdrankautomaat) method](https://github.com/MathiasV-immalle/portfolio/blob/master/dotnetfiddle/Hoofdstuk%204/Oef%204.9.md)

**Hoofdstuk 5**

- [Oefening 5.1: ToonNaam method](https://github.com/MathiasV-immalle/portfolio/blob/master/dotnetfiddle/Hoofdstuk%205/Oef%205.1.md)

- [Oefening 5.8: Wisselkoers euro - dollar / dollar - euro method](https://github.com/MathiasV-immalle/portfolio/blob/master/dotnetfiddle/Hoofdstuk%205/Oef%205.8.md)

- [Oefening 5.9: Volume kubus method](https://github.com/MathiasV-immalle/portfolio/blob/master/dotnetfiddle/Hoofdstuk%205/Oef%205.9.md)

- [Oefening 5.10: Opp. cirkel method](https://github.com/MathiasV-immalle/portfolio/blob/master/dotnetfiddle/Hoofdstuk%205/Oef%205.10.md)

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

