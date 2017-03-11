# Oefening 7.3: Bioscooptarief
### Met gebruik van: extra Window, Listbox, slider
MainWindow: XAML
```C#
<Window x:Class="_7._3_Bioscooptarief.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:_7._3_Bioscooptarief"
        mc:Ignorable="d"
        Title="Poképolis.com" Height="350" Width="525">
    <Grid>
        <Canvas HorizontalAlignment="Left" Height="319" VerticalAlignment="Top" Width="517" Background="Aqua">
            <Button x:Name="StartButton" Content="Start" HorizontalAlignment="Left" Height="27" VerticalAlignment="Top" Width="83" Click="button_Click" Canvas.Left="210" Canvas.Top="171"/>
            <Label x:Name="WelkomsLabel" Background="Aquamarine" FontSize="16" FontFamily="Lucida Bright" Content="Welkom in Poképolis! Klik op Start om te beginnen." HorizontalAlignment="Left" VerticalAlignment="Top" Canvas.Left="47" Canvas.Top="95"/>
        </Canvas>
    </Grid>
</Window>
```
MainWindow: Eventhandlers
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

namespace _7._3_Bioscooptarief
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        ExtraWindow Mainwindow = new ExtraWindow();
        public MainWindow()
        {
            InitializeComponent();
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            Mainwindow.Show();
            this.Close();
        }
    }
}
```
ExtraWindow: XAML
```C#
<Window x:Class="_7._3_Bioscooptarief.ExtraWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:_7._3_Bioscooptarief"
        mc:Ignorable="d"
        Title="Poképolis.com" Height="350" Width="525">

    <Grid>
        <Canvas x:Name="MainCanvas" Background="LightGray" HorizontalAlignment="Left" Height="319" VerticalAlignment="Top" Width="517">
            <ListBox x:Name="AantalListBox" HorizontalAlignment="Left" Height="188" VerticalAlignment="Top" Width="68" Canvas.Left="290" Canvas.Top="44"/>
            <ListBox x:Name="CategorieListbox" HorizontalAlignment="Left" Height="188" VerticalAlignment="Top" Width="68" Canvas.Left="358" Canvas.Top="44"/>
            <ListBox x:Name="PrijsListbox" HorizontalAlignment="Left" Height="188" VerticalAlignment="Top" Width="68" Canvas.Left="426" Canvas.Top="44"/>
            <Button x:Name="VoegToeButton" Content="Voeg toe" HorizontalAlignment="Left" VerticalAlignment="Top" Width="75" Click="VoegToeButton_Click" Canvas.Left="193" Canvas.Top="124"/>
            <Slider x:Name="CategorieSlider" HorizontalAlignment="Left" VerticalAlignment="Top" Width="178" RenderTransformOrigin="0.5,0.5" Canvas.Left="49" Canvas.Top="127">
                <Slider.RenderTransform>
                    <TransformGroup>
                        <ScaleTransform/>
                        <SkewTransform/>
                        <RotateTransform Angle="90"/>
                        <TranslateTransform/>
                    </TransformGroup>
                </Slider.RenderTransform>
            </Slider>
            <Label x:Name="Jaar5MinderLabel" Content="-5" HorizontalAlignment="Left" VerticalAlignment="Top" Canvas.Left="39" Canvas.Top="44"/>
            <Label x:Name="Jaar5tot12Label" Content="5 - 12" HorizontalAlignment="Left" VerticalAlignment="Top" Canvas.Left="39" Canvas.Top="91"/>
            <Label x:Name="Jaar13tot54Label" Content="13 - 54" HorizontalAlignment="Left" VerticalAlignment="Top" Canvas.Left="39" Canvas.Top="137"/>
            <Label x:Name="Jaar55MeerLabel" Content="55+" HorizontalAlignment="Left" VerticalAlignment="Top" Canvas.Left="39" Canvas.Top="184"/>
            <Label x:Name="TotaalPrijsLabel" Content="Totale prijs: € 0,00" HorizontalAlignment="Left" Height="26" VerticalAlignment="Top" Width="202" Canvas.Left="290" Canvas.Top="237"/>
            <Label x:Name="ListboxTitel1" Content="Aantal" Height="31" Canvas.Left="291" Canvas.Top="10" Width="67"/>
            <Label x:Name="ListboxTitel2" Content="Categorie" Height="32" Canvas.Left="354" Canvas.Top="10" Width="72"/>
            <Label x:Name="ListboxTitel3" Content="Prijs" Height="31" Canvas.Left="427" Canvas.Top="10" Width="67"/>
        </Canvas>
        <Canvas x:Name="BetaalCanvas" Background="LightBlue" HorizontalAlignment="Left" Height="88" Margin="0,231,327,0" VerticalAlignment="Top" Width="190">
            <Label x:Name="VraagKlaarLabel" Content="Klik op 'Betalen' als u klaar bent." HorizontalAlignment="Left" VerticalAlignment="Top" Canvas.Left="10" Canvas.Top="10"/>
            <Button x:Name="BetaalKnop" Content="Betalen" HorizontalAlignment="Left" VerticalAlignment="Top" Width="75" Canvas.Left="53" Canvas.Top="41" Click="BetaalKnop_Click"/>
        </Canvas>

    </Grid>
</Window>
```
ExtraWindow: Eventhandlers
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
using System.Windows.Shapes;

namespace _7._3_Bioscooptarief
{
    /// <summary>
    /// Interaction logic for ExtraWindow.xaml
    /// </summary>
    public partial class ExtraWindow : Window
    {
        private int x = 0;
        private string Prijs0 = "€ 0,00";
        private string Prijs1 = "€ 7,50";
        private string Prijs2 = "€ 15,00";
        // private string Prijs3 = "€ 0,00";
        private double TotalePrijs = 0;
        private string WeergegevenTotalePrijs = "";

        public ExtraWindow()
        {
            InitializeComponent();
            CategorieSlider.Maximum = 3;
            CategorieSlider.Minimum = 0;
            CategorieSlider.Interval = 1;
            BetaalKnop.Visibility = Visibility.Hidden;
            VraagKlaarLabel.Visibility = Visibility.Hidden;
        }

        private void VoegToeButton_Click(object sender, RoutedEventArgs e)
        {
            x += 1;
            AantalListBox.Items.Add(x);
            if (CategorieSlider.Value == 0)
            {
                CategorieListbox.Items.Add("-5");
                PrijsListbox.Items.Add(Prijs0);
            }
            else if (CategorieSlider.Value == 1)
            {
                CategorieListbox.Items.Add("5 - 12");
                PrijsListbox.Items.Add(Prijs1);
                TotalePrijs += 7.50;
            }
            else if (CategorieSlider.Value == 2)
            {
                CategorieListbox.Items.Add("13 - 54");
                PrijsListbox.Items.Add(Prijs2);
                TotalePrijs += 15.00;
            }
            else if (CategorieSlider.Value == 3)
            {
                CategorieListbox.Items.Add("55+");
                PrijsListbox.Items.Add(Prijs0);
            }

            if (TotalePrijs == 0)
            {
                WeergegevenTotalePrijs = "Totale prijs: € 0,00";
            }
            else
            {
                WeergegevenTotalePrijs = "Totale prijs: €" + TotalePrijs;
            }
            TotaalPrijsLabel.Content = WeergegevenTotalePrijs;

            BetaalKnop.Visibility = Visibility.Visible;
            VraagKlaarLabel.Visibility = Visibility.Visible;
        }

        private void BetaalKnop_Click(object sender, RoutedEventArgs e)
        {
            // transactie / transaction 
        }
    }
}
```
