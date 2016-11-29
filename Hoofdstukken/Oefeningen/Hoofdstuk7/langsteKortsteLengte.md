# Oefening: Langste/Kortste lengte
### Hier berekent men de langste en de kortste lengte van 3 opgegeven lengtes.
```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ifthenelseProjects
{
    class Program
    {
        static void Main(string[] args)
        {
	    Console.WriteLine(KortsteLengte(2.4, 4.7, 3.8));
            Console.WriteLine(LangsteLengte(2.4, 4.7, 3.8));
        }

        static double KortsteLengte(double lengteA, double lengteB, double lengteC)
        {
            double kortsteLengte = 0;
            if (lengteA < lengteB && lengteA < lengteC)
            {
                kortsteLengte = lengteA;
            }
            
            else if (lengteB < lengteA && lengteB < lengteC)
            {
                kortsteLengte = lengteB;
            }
            else if (lengteC < lengteA && lengteC < lengteB)
            {
                kortsteLengte = lengteC;
            }

            return kortsteLengte;
        }

        static double LangsteLengte(double lengteA, double lengteB, double lengteC)
        {
            double langsteLengte = 0;
            if (lengteA > lengteB && lengteA > lengteC)
            {
                langsteLengte = lengteA;
            }

            else if (lengteB > lengteA && lengteB > lengteC)
            {
                langsteLengte = lengteB;
            }
            else if (lengteC > lengteA && lengteC > lengteB)
            {
                langsteLengte = lengteC;
            }

            return langsteLengte;
        }
    }
}

```
