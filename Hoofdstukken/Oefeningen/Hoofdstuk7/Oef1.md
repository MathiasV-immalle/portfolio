# Oefening 7.1: Kaart genereren
### Met behulp van if, switch case, random-gatallengenerator

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Oef7._1EenkaartDelen
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Zou u graag een kaart krijgen?");
            string str = Console.ReadLine();

            if (str == "Ja")
            {
                Random rndGen = new Random();
                int s = rndGen.Next(1, 4);
                soortKaart(s);

                Random rndGen2 = new Random();
                int nr = rndGen.Next(1, 13);
                kaartNr(nr);

                Console.WriteLine("U heeft de {0} {1} gekregen.", soortKaart(s), kaartNr(nr));
            }
            else
            {
                Console.WriteLine("Geen probleem, fijne dag verder!");
            }
        }

        public static string soortKaart(int soort)
        {
            string weergegevenSoort = "";
            switch (soort)
            {
                case 1:
                    weergegevenSoort = "harten";
                    break;
                case 2:
                    weergegevenSoort = "ruiten";
                    break;
                case 3:
                    weergegevenSoort = "klaveren";
                    break;
                case 4:
                    weergegevenSoort = "schoppen";
                    break;
            }
            return weergegevenSoort;
        }

        public static string kaartNr(int KaartNummer)
        {
            string weergegevenKaartNr = "";
            switch (KaartNummer)
            {
                case 1:
                    weergegevenKaartNr = "aas";
                    break;
                case 2:
                    weergegevenKaartNr = "2";
                    break;
                case 3:
                    weergegevenKaartNr = "3";
                    break;
                case 4:
                    weergegevenKaartNr = "4";
                    break;
                case 5:
                    weergegevenKaartNr = "5";
                    break;
                case 6:
                    weergegevenKaartNr = "6";
                    break;
                case 7:
                    weergegevenKaartNr = "7";
                    break;
                case 8:
                    weergegevenKaartNr = "8";
                    break;
                case 9:
                    weergegevenKaartNr = "9";
                    break;
                case 10:
                    weergegevenKaartNr = "10";
                    break;
                case 11:
                    weergegevenKaartNr = "boer";
                    break;
                case 12:
                    weergegevenKaartNr = "dame";
                    break;
                case 13:
                    weergegevenKaartNr = "heer";
                    break;
            }
            return weergegevenKaartNr;
        }
    }
}
```
