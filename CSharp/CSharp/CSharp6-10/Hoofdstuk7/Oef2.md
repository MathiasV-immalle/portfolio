# Oefening 7.2: Getallen sorteren
### Met gebruik van sliders, if-else

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace Oef7._2Sorteren
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();

            SG1.Minimum = 0;
            SG1.Maximum = 10;

            SG2.Minimum = 0;
            SG2.Maximum = 10;

            SG3.Minimum = 0;
            SG3.Maximum = 10;

            LG1.Content = Convert.ToString(SG1.Value);
            LG2.Content = Convert.ToString(SG2.Value);
            LG3.Content = Convert.ToString(SG3.Value);
        }

        private void SG1_ValueChanged(object sender, RoutedPropertyChangedEventArgs<double> e)
        {
            int sg1 = Convert.ToInt32(SG1.Value);
            LG1.Content = Convert.ToString(sg1);
        }

        private void SG2_ValueChanged(object sender, RoutedPropertyChangedEventArgs<double> e)
        {
            int sg2 = Convert.ToInt32(SG2.Value);
            LG2.Content = Convert.ToString(sg2);
        }

        private void SG3_ValueChanged(object sender, RoutedPropertyChangedEventArgs<double> e)
        {
            int sg3 = Convert.ToInt32(SG3.Value);
            LG3.Content = Convert.ToString(sg3);
        }

        private void B_Click(object sender, RoutedEventArgs e)
        {
            if (SG1.Value > SG2.Value && SG2.Value > SG3.Value) // SG1 groter dan SG2 + SG2 groter dan SG3 -> 'SG1 > SG2 > SG3'
            {
                int LB1a = Convert.ToInt32(SG1.Value);
                int LB1b = Convert.ToInt32(SG2.Value);
                int LB1c = Convert.ToInt32(SG3.Value);
                LB.Content = LB1c + " " + LB1b + " " + LB1a;
            }
            else if (SG1.Value > SG3.Value && SG3.Value > SG2.Value) // SG1 groter dan SG3 + SG3 groter dan SG2 -> 'SG1 > SG3 > SG2'
            {
                int LB1a = Convert.ToInt32(SG1.Value);
                int LB1b = Convert.ToInt32(SG2.Value);
                int LB1c = Convert.ToInt32(SG3.Value);
                LB.Content = LB1b + " " + LB1c + " " + LB1a;
            }
            else if (SG3.Value > SG2.Value && SG2.Value > SG1.Value) // SG3 groter dan SG2 + SG2 groter dan SG1 --> SG3 > SG2 > SG1
            {
                int LB1a = Convert.ToInt32(SG1.Value);
                int LB1b = Convert.ToInt32(SG2.Value);
                int LB1c = Convert.ToInt32(SG3.Value);
                LB.Content = LB1a + " " + LB1b + " " + LB1c;
            }
            else if (SG3.Value > SG1.Value && SG1.Value > SG3.Value) // SG3 groter dan SG1 + SG1 groter dan SG2 --> SG3 > SG1 > SG2
            {
                int LB1a = Convert.ToInt32(SG1.Value);
                int LB1b = Convert.ToInt32(SG2.Value);
                int LB1c = Convert.ToInt32(SG3.Value);
                LB.Content = LB1b + " " + LB1a + " " + LB1c;
            }
            else if (SG2.Value > SG3.Value && SG3.Value > SG1.Value) // SG2 groter dan SG3 + SG3 groter dan SG1 --> SG2 > SG3 > SG1
            {
                int LB1a = Convert.ToInt32(SG1.Value);
                int LB1b = Convert.ToInt32(SG2.Value);
                int LB1c = Convert.ToInt32(SG3.Value);
                LB.Content = LB1a + " " + LB1c + " " + LB1b;
            }
            else // overig: SG2 groter dan SG1 + SG1 groter dan SG3 --> SG2 > SG1 > SG3
            {
                int LB1a = Convert.ToInt32(SG1.Value);
                int LB1b = Convert.ToInt32(SG2.Value);
                int LB1c = Convert.ToInt32(SG3.Value);
                LB.Content = LB1c + " " + LB1a + " " + LB1b;
            }
        }
    }
}

```
