# Oefening: Switch case

``` C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace SwitchCaseOefening
{
    class Program
    {
        public static string ScoreNaarWaardering(int score)
        {
            string weergegevenScore = "";
            switch (score)
            {
                case 1:
                case 2:
                case 3:
                case 4:
                case 5:
                    weergegevenScore = "onvoldoende";
                    break;
                case 6:
                case 7:
                    weergegevenScore = "voldoende";
                    break;
                case 8:
                    weergegevenScore = "goed";
                    break;
                case 9:
                    weergegevenScore = "zeer goed";
                    break;
                case 10:
                    weergegevenScore = "prima";
                    break;
            }
            Console.WriteLine("Mathias heeft een {0} op zijn test, daarom heeft de leerkracht '{1}' op zijn test geschreven.", score, weergegevenScore);
            return weergegevenScore;
        }
        static void Main(string[] args)
        {
            ScoreNaarWaardering(7);
        }
    }
}
```
