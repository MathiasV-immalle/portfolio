# Oefening 4.2: Cirkel: straal / omtrek / opp + volume bol method

```
using System;
					
public class Program
{
	public static void Main()
	{
		// Inputs
		double straal = 7.5;
		
		// Outputs		
		double omtrek = 2 * Math.PI * straal;
		double oppervlakte = Math.PI * Math.Pow(straal, 2);
		double volume = (4 * Math.PI / 3) * Math.Pow(straal, 3);
		
		// Weergave
		Console.WriteLine("De omtrek van een cirkel met straal" + " " + straal + "=" + " " + omtrek);
		Console.WriteLine("De oppervlakte van een cirkel met straal" + " " + straal + "=" + " " + oppervlakte);
		Console.WriteLine("Het volume van een bol met straal" + " " + straal + "=" + " " + volume);
	}
}
```
