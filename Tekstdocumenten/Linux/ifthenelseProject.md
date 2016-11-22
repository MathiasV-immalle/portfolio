# Oefening: Weekloon berekenen met overuren 
### (oefening op if-then-else projecten)

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
            Console.WriteLine(BerekenWeekloon(14.00, 25, 1.35));
            Console.WriteLine(BerekenWeekloon(14.00, 45, 1.35));
        }

        static double BerekenWeekloon(double uurloon, int aantalUurGewerkt, double extraPercentage)
        {
            double weekloon = 0;
            if (aantalUurGewerkt <= 38)
            {
                weekloon = uurloon * aantalUurGewerkt;
                //Console.WriteLine("Deze week heeft u {0} verdient door {1} uur te werken.", weekloon, aantalUurGewerkt);
            }
            else
            {
                double extraUren = aantalUurGewerkt - 38;
                double extraBetaald = extraUren * uurloon * extraPercentage;
                weekloon = 38 * uurloon + extraBetaald;
                //Console.WriteLine("Deze week heeft u {0} verdient door {1} uur te werken.", weekloon, aantalUurGewerkt);
            }
            return weekloon;
        }
    }
}
```
