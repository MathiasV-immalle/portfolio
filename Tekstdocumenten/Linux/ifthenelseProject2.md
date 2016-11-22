# Oefening: Bereken verkoopprijs met kortingen
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
            Console.WriteLine(BerekenVerkoopprijs(65.00));
            Console.WriteLine(BerekenVerkoopprijs(36.00));
            Console.WriteLine(BerekenVerkoopprijs(48.00));
            Console.WriteLine(BerekenVerkoopprijs(85.00));

        }
        static double BerekenVerkoopprijs(double inkoopprijs)
        {
            double verkoopprijs = inkoopprijs * 2;
            if (verkoopprijs > 40 && verkoopprijs < 80)
            {
                verkoopprijs = verkoopprijs * 0.80;
            }
            else if (verkoopprijs > 80)
            {
                verkoopprijs = verkoopprijs * 0.70;
            }
            return verkoopprijs;
        }
    }
}
```
