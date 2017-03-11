# Oefening 7.4 Weddenschap
### Met gebruik van: Klasse, ListBox, ProgressBar, Random
Mainwindow: XAML
```C#
<Window x:Class="_7._4_Weddenschap.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:_7._4_Weddenschap"
        mc:Ignorable="d"
        Title="MainWindow" Height="350" Width="525">
    <Grid>
        <ProgressBar x:Name="ProgressBar" HorizontalAlignment="Left" Height="27" VerticalAlignment="Top" Width="517" Margin="0,270,0,0"/>
        <Label x:Name="ProgressLabel1" Content="Progress" HorizontalAlignment="Left" Margin="230,270,0,0" VerticalAlignment="Top"/>
        <Button x:Name="WerpButton" Content="Werp" HorizontalAlignment="Left" Margin="219,228,0,0" VerticalAlignment="Top" Width="75" Click="WerpButton_Click"/>
        <ListBox x:Name="AantalWorpenListBox" HorizontalAlignment="Left" Height="164" Margin="219,59,0,0" VerticalAlignment="Top" Width="38"/>
        <ListBox x:Name="ScoreListBox" HorizontalAlignment="Left" Height="164" Margin="256,59,0,0" VerticalAlignment="Top" Width="38"/>
        <Label x:Name="Worp" Content="Worp" HorizontalAlignment="Left" Margin="176,56,0,0" VerticalAlignment="Top"/>
    </Grid>
</Window>
```
Mainwindow: Eventhandlers
```C#
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

namespace _7._4_Weddenschap
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        int x = 0;
        int progress = 0;
        string progressie = "";
        Worp worp1 = new Worp();
        Worp worp2 = new Worp();
        Worp worp3 = new Worp();
        int waardeWorp1 = 0;
        int waardeWorp2 = 0;
        int waardeWorp3 = 0;

        public MainWindow()
        {
            InitializeComponent();
            ProgressBar.Minimum = 0;
            ProgressBar.Maximum = 3;
            ProgressBar.Value = 0;
            Worp.Visibility = Visibility.Hidden;
        }

        private void WerpButton_Click(object sender, RoutedEventArgs e)
        {
            x += 1;
            progress += 1;

            if (progress == 1)
            {
                WerpButton.Content = "Werp!";
                waardeWorp1 = worp1.Werp();
                ScoreListBox.Items.Add(waardeWorp1);
                AantalWorpenListBox.Items.Add(x);
                ProgressBar.Value = 1;
                Worp.Visibility = Visibility.Visible;
            }
            else if (progress == 2)
            {
                waardeWorp2 = worp2.Werp();
                ScoreListBox.Items.Add(waardeWorp2);
                AantalWorpenListBox.Items.Add(x);
                ProgressBar.Value = 2;
            }
            else if (progress == 3)
            {
                waardeWorp3 = worp3.Werp();
                ScoreListBox.Items.Add(waardeWorp3);
                AantalWorpenListBox.Items.Add(x);
                ProgressBar.Value = 3;
                WerpButton.Content = "Herstart!";

                if (waardeWorp1 == waardeWorp2
                    &&
                    waardeWorp2 == waardeWorp3
                    &&
                    waardeWorp3 == 6)
                {
                    MessageBox.Show("Proficiat! Speler wint €20!");
                }
                else if (waardeWorp1 == waardeWorp2
                  &&
                  waardeWorp2 == waardeWorp3
                  &&
                  waardeWorp3 != 6)
                {
                    MessageBox.Show("Speler wint €10!");
                }
                else if (waardeWorp2 == waardeWorp1 && waardeWorp1 != waardeWorp3)
                {
                    MessageBox.Show("Speler wint €5!");
                }
                else if (waardeWorp2 == waardeWorp3 && waardeWorp3 != waardeWorp1)
                {
                    MessageBox.Show("Speler wint €5!");
                }
                else if (waardeWorp3 == waardeWorp1 && waardeWorp1 != waardeWorp2)
                {
                    MessageBox.Show("Speler wint €5!");
                }
            }
            else 
            {
                WerpButton.Content = "Werp!";
                AantalWorpenListBox.Items.Clear();
                ScoreListBox.Items.Clear();
                progress = 0;
                x = 0;
                ProgressBar.Value = 0;
                Worp.Visibility = Visibility.Hidden;
            }            
            progressie = "Progress " + progress + "/3";
            ProgressLabel1.Content = progressie;
        }
    }
}
```
Class Worp: 
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _7._4_Weddenschap
{
    class Worp
    {
        Random Random = new Random();
        int r = 0;
        public Worp()
        {
            Werp();
        }

        public int Werp()
        {
            r = Random.Next(1, 7);
            return r;
        }
    }
}
```
- de Random werkt niet 100%. Als iemand het foutje mocht vinden, zet gerust een issue. 
