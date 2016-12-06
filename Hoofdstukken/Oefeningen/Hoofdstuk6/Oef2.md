# Oefening 6.2: Knop drukken = +1 (Cookieclicker) 

## De XAML-code
```C#
<Window x:Class="hoofdstuk6Oef2.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:hoofdstuk6Oef2"
        mc:Ignorable="d"
        Title="MainWindow" Height="350" Width="525">
    <Grid>
        <Label x:Name="label" Content="0" HorizontalAlignment="Left" VerticalAlignment="Top" Margin="80,67,0,0"/>
        <Button x:Name="button" Content="Add" HorizontalAlignment="Left" VerticalAlignment="Top" Width="75" Margin="150,70,0,0" Click="button_Click"/>

    </Grid>
</Window>
```
## De Eventhandlers 

## Versie 1: Zoals de opdracht het vraagt

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

namespace hoofdstuk6Oef2
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        int getal = 0;

        public MainWindow()
        {
            InitializeComponent();
            
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            getal = getal + 1;
            label.Content = getal;
    }
    }
}
```
## Versie 2: Makkelijke CookieClicker-uitbreiding
##### (Dezelfde XAML-code als versie 1)

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

namespace hoofdstuk6Oef2
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        int getal = 0;

        public MainWindow()
        {
            InitializeComponent();

        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            if (getal < 50)
            {
                getal = getal + 1;
                label.Content = getal;
            }
            else if (getal < 100 && getal >= 50)
            {
                getal = getal + 2;
                label.Content = getal;
            }
            else if (getal < 200 && getal >= 100)
            {
                getal = getal + 4;
                label.Content = getal;
            }
            else if (getal < 500 && getal >= 200)
            {
                getal = getal + 10;
                label.Content = getal;
            }
            else if (getal < 1000 && getal >= 500)
            {
                getal = getal + 25;
                label.Content = getal;
            }
        }
    }
}
```
## Versie 3: Moeilijkere CookieClicker-uitbreiding

[CookieClicker](https://github.com/MathiasV-immalle/CookieClicker)

## De XAML-code
```C#
<Window x:Class="hoofdstuk6Oef2.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:hoofdstuk6Oef2"
        mc:Ignorable="d"
        Title="MainWindow" Height="350" Width="525">
    <Grid>
        <Canvas Background="LightBlue">
            <Button x:Name="EnterShopButton" Background="CornflowerBlue" Content="Enter Shop" Canvas.Left="265" Canvas.Top="36" Width="242" Click="EnterShopButton_Click"/>
            <Button x:Name="Grandma" Content="Grandma" Canvas.Left="265" Canvas.Top="61" Width="85" MouseEnter="Grandma_MouseEnter" MouseLeave="Grandma_MouseLeave" Click="Grandma_Click"/>
            <Label x:Name="GrandmaLabelCosts" Foreground="Red" Content="cost: 50c" Canvas.Left="355" Canvas.Top="58" Width="76"/>
            <Label x:Name="GrandmaLabelPlus" Foreground="Green" Content="+2C/click" Canvas.Left="431" Canvas.Top="58" Width="76"/>
            <Label x:Name="GrandmaLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="58"/>
            <Label x:Name="GrandmaLevelLabel2" Content="0" HorizontalAlignment="Left" VerticalAlignment="Top" Width="37" Canvas.Left="228" Canvas.Top="59"/>
            <Button x:Name="NOven" Content="New Oven" HorizontalAlignment="Left" VerticalAlignment="Top" Width="85" Canvas.Left="265" Canvas.Top="85" Click="NOven_Click" MouseEnter="NOven_MouseEnter" MouseLeave="NOven_MouseLeave"/>
            <Label x:Name="NewOvenLabelCosts" Foreground="Red" Content="cost: 200c" Canvas.Left="355" Canvas.Top="82" Width="76"/>
            <Label x:Name="NewOvenLabelPlus" Foreground="Green" Content="+10C/click" Canvas.Left="431" Canvas.Top="82" Width="76"/>
            <Label x:Name="NewOvenLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="82"/>
            <Label x:Name="NewOvenLevelLabel2" Content="0" HorizontalAlignment="Left" VerticalAlignment="Top" Width="37" Canvas.Left="228" Canvas.Top="82"/>
            <Button x:Name="XOven" Content="Second Oven" Canvas.Left="265" Canvas.Top="110" Width="85" Click="XOven_Click" MouseEnter="XOven_MouseEnter" MouseLeave="XOven_MouseLeave"/>
            <Label x:Name="SecondOvenLabelCosts" Foreground="Red" Content="cost: 500c" Canvas.Left="355" Canvas.Top="107" Width="76"/>
            <Label x:Name="SecondOvenLabelPlus" Foreground="Green" Content="+25C/click" Canvas.Left="431" Canvas.Top="107" Width="76"/>
            <Label x:Name="SecondOvenLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="107"/>
            <Label x:Name="SecondOvenLevelLabel2" Content="0" HorizontalAlignment="Left" VerticalAlignment="Top" Width="37" Canvas.Left="228" Canvas.Top="107"/>
            <Button x:Name="SpaceCookie" Content="Space Cookie" Canvas.Left="265" Canvas.Top="135" Width="85" Click="SpaceCookie_Click" MouseEnter="SpaceCookie_MouseEnter" MouseLeave="SpaceCookie_MouseLeave"/>
            <Label x:Name="SpaceCookieLabelCosts" Foreground="Red" Content="cost: 1000c" Canvas.Left="355" Canvas.Top="132" Width="76"/>
            <Label x:Name="SpaceCookieLabelPlus" Foreground="Green" Content="+50C/click" Canvas.Left="431" Canvas.Top="132" Width="76"/>
            <Label x:Name="SpaceCookieLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="132"/>
            <Label x:Name="SpaceCookieLevelLabel2" Content="0" HorizontalAlignment="Left" VerticalAlignment="Top" Width="37" Canvas.Left="228" Canvas.Top="132"/>
            <Button x:Name="LeaveShopButton" Background="CornflowerBlue" Content="Leave Shop" HorizontalAlignment="Left" VerticalAlignment="Top" Width="242" Canvas.Left="265" Canvas.Top="235" Click="LeaveShopButton_Click"/>
            <Label x:Name="KoekjesPerClick" Content="1 koekje(s) per Click" Canvas.Left="38" Canvas.Top="100"/>
            <Button x:Name="Bakerie" Content="Bakerie" Canvas.Left="265" Canvas.Top="160" Width="85" Click="Bakerie_Click" MouseEnter="Bakerie_MouseEnter" MouseLeave="Bakerie_MouseLeave"/>
            <Label x:Name="BakerieLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="157" Width="34"/>
            <Label x:Name="BakerieLevelLabel2" Content="0" Canvas.Left="228" Canvas.Top="157" Width="37"/>
            <Label x:Name="BakerieLabelCosts" Foreground="Red" Content="cost: 3000c" Canvas.Left="355" Canvas.Top="157" Width="76"/>
            <Label x:Name="BakerieLabelPlus" Foreground="Green" Content="+75C/click" Canvas.Left="431" Canvas.Top="157" Width="76"/>
            <Button x:Name="CookiePlanet" Content="Cookie Planet" Canvas.Left="265" Canvas.Top="185" Width="85" Click="CookiePlanet_Click" MouseEnter="CookiePlanet_MouseEnter" MouseLeave="CookiePlanet_MouseLeave"/>
            <Label x:Name="CookiePlanetLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="182" Width="34"/>
            <Label x:Name="CookiePlanetLevelLabel2" Content="0" Canvas.Left="228" Canvas.Top="182" Width="37"/>
            <Label x:Name="CookiePlanetLabelCosts" Foreground="Red" Content="cost: 5000c" Canvas.Left="355" Canvas.Top="182" Width="76"/>
            <Label x:Name="CookiePlanetLabelPlus" Foreground="Green" Content="+100C/click" Canvas.Left="431" Canvas.Top="182" Width="76"/>
            <Button x:Name="Cookieversium" Content="Cookieversium" Canvas.Left="265" Canvas.Top="210" Width="85" Click="Cookieversium_Click" MouseEnter="Cookieversium_MouseEnter" MouseLeave="Cookieversium_MouseLeave"/>
            <Label x:Name="CookieversiumLevelLabel" Content="level" Canvas.Left="194" Canvas.Top="207" Width="34"/>
            <Label x:Name="CookieversiumLevelLabel2" Content="0" Canvas.Left="228" Canvas.Top="207" Width="37"/>
            <Label x:Name="CookieversiumLabelCosts" Foreground="Red" Content="cost: 10000c" Canvas.Left="355" Canvas.Top="207" Width="76"/>
            <Label x:Name="CookieversiumLabelPlus" Foreground="Green" Content="+150C/click" Canvas.Left="431" Canvas.Top="207" Width="76"/>
            <Button x:Name="SpaceCookieTransformer" Content="Space Mode" Canvas.Left="10" Canvas.Top="289" Width="75" Click="SpaceCookieTransformer_Click"/>
            <Button x:Name="NormalCookieTransformer" Content="Earth Mode" Canvas.Left="111" Canvas.Top="289" Width="75" Click="NormalCookieTransformer_Click"/>
        </Canvas>

        <Label x:Name="AantalCookies" Content="0" HorizontalAlignment="Left" VerticalAlignment="Top" Margin="47,36,0,0" Width="212"/>
        <Ellipse x:Name="Cookie" Fill="SandyBrown" HorizontalAlignment="Left" Height="100" Stroke="SaddleBrown" VerticalAlignment="Top" Width="100" Margin="47,148,0,0" MouseEnter="Cookie_MouseEnter" MouseLeftButtonDown="Cookie_MouseLeftButtonDown" MouseLeave="Cookie_MouseLeave"/>
        <Ellipse x:Name="Chocolate1" Fill="SaddleBrown" HorizontalAlignment="Left" Height="23" Margin="76,210,0,0" Stroke="SandyBrown" VerticalAlignment="Top" Width="23" MouseLeftButtonDown="Cookie_MouseLeftButtonDown" MouseEnter="Cookie_MouseEnter" MouseLeave="Cookie_MouseLeave"/>
        <Ellipse x:Name="Chocolate2" Fill="SaddleBrown" HorizontalAlignment="Left" Height="39" Margin="60,166,0,0" Stroke="SandyBrown" VerticalAlignment="Top" Width="39" MouseLeftButtonDown="Cookie_MouseLeftButtonDown" MouseEnter="Cookie_MouseEnter" MouseLeave="Cookie_MouseLeave"/>
        <Ellipse x:Name="Chocolate3" Fill="SaddleBrown" HorizontalAlignment="Left" Height="30" Margin="104,189,0,0" Stroke="SandyBrown" VerticalAlignment="Top" Width="30" MouseLeftButtonDown="Cookie_MouseLeftButtonDown" MouseEnter="Cookie_MouseEnter" MouseLeave="Cookie_MouseLeave"/>
        <Label x:Name="Cookies" Content="Cookies" HorizontalAlignment="Left" Margin="70,67,0,0" VerticalAlignment="Top" Width="57"/>

    </Grid>
</Window>
```
## De Eventhandlers
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

namespace hoofdstuk6Oef2
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        int getal = 0;

        public MainWindow()
        {
            InitializeComponent();
            Grandma.Visibility = Visibility.Hidden;
            NOven.Visibility = Visibility.Hidden;
            XOven.Visibility = Visibility.Hidden;
            SpaceCookie.Visibility = Visibility.Hidden;
            Bakerie.Visibility = Visibility.Hidden;
            CookiePlanet.Visibility = Visibility.Hidden;
            Cookieversium.Visibility = Visibility.Hidden;
            LeaveShopButton.Visibility = Visibility.Hidden;
            GrandmaLabelCosts.Visibility = Visibility.Hidden;
            GrandmaLabelPlus.Visibility = Visibility.Hidden;
            GrandmaLevelLabel.Visibility = Visibility.Hidden;
            GrandmaLevelLabel2.Visibility = Visibility.Hidden;
            NewOvenLevelLabel.Visibility = Visibility.Hidden;
            NewOvenLevelLabel2.Visibility = Visibility.Hidden;
            NewOvenLabelCosts.Visibility = Visibility.Hidden;
            NewOvenLabelPlus.Visibility = Visibility.Hidden;
            SecondOvenLevelLabel.Visibility = Visibility.Hidden;
            SecondOvenLevelLabel2.Visibility = Visibility.Hidden;
            SecondOvenLabelCosts.Visibility = Visibility.Hidden;
            SecondOvenLabelPlus.Visibility = Visibility.Hidden;
            SpaceCookieLevelLabel.Visibility = Visibility.Hidden;
            SpaceCookieLevelLabel2.Visibility = Visibility.Hidden;
            SpaceCookieLabelCosts.Visibility = Visibility.Hidden;
            SpaceCookieLabelPlus.Visibility = Visibility.Hidden;
            SpaceCookieTransformer.Visibility = Visibility.Hidden;
            NormalCookieTransformer.Visibility = Visibility.Hidden;
            BakerieLevelLabel.Visibility = Visibility.Hidden;
            BakerieLevelLabel2.Visibility = Visibility.Hidden;
            BakerieLabelCosts.Visibility = Visibility.Hidden;
            BakerieLabelPlus.Visibility = Visibility.Hidden;
            CookiePlanetLevelLabel.Visibility = Visibility.Hidden;
            CookiePlanetLevelLabel2.Visibility = Visibility.Hidden;
            CookiePlanetLabelCosts.Visibility = Visibility.Hidden;
            CookiePlanetLabelPlus.Visibility = Visibility.Hidden;
            CookieversiumLevelLabel.Visibility = Visibility.Hidden;
            CookieversiumLevelLabel2.Visibility = Visibility.Hidden;
            CookieversiumLabelCosts.Visibility = Visibility.Hidden;
            CookieversiumLabelPlus.Visibility = Visibility.Hidden;

        }

        // Cookie + Click
        //
        //

        private void Cookie_MouseEnter(object sender, MouseEventArgs e)
        {
            Cookie.StrokeThickness = 3;
        }

        private void Cookie_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            getal = getal + 1
            + Convert.ToInt32(GrandmaLevelLabel2.Content) * 2
            + Convert.ToInt32(NewOvenLevelLabel2.Content) * 10
            + Convert.ToInt32(SecondOvenLevelLabel2.Content) * 25
            + Convert.ToInt32(SpaceCookieLevelLabel2.Content) * 50
            + Convert.ToInt32(BakerieLevelLabel2.Content) * 75
            + Convert.ToInt32(CookiePlanetLevelLabel2.Content) * 100
            + Convert.ToInt32(CookieversiumLevelLabel2.Content) * 150
            ;
            AantalCookies.Content = getal;
            KoekjesPerClick.Content = 1
            + Convert.ToInt32(GrandmaLevelLabel2.Content) * 2
            + Convert.ToInt32(NewOvenLevelLabel2.Content) * 10
            + Convert.ToInt32(SecondOvenLevelLabel2.Content) * 25
            + Convert.ToInt32(SpaceCookieLevelLabel2.Content) * 50
            + Convert.ToInt32(BakerieLevelLabel2.Content) * 75
            + Convert.ToInt32(CookiePlanetLevelLabel2.Content) * 100
            + Convert.ToInt32(CookieversiumLevelLabel2.Content) * 150
            + " koekje(s) per Click";
        }

        private void Cookie_MouseLeave(object sender, MouseEventArgs e)
        {
            Cookie.StrokeThickness = 1;
        }

        // Visibility
        //
        //

        private void EnterShopButton_Click(object sender, RoutedEventArgs e)
        {
            EnterShopButton.Content = "Shop";
            Grandma.Visibility = Visibility.Visible;
            NOven.Visibility = Visibility.Visible;
            XOven.Visibility = Visibility.Visible;
            SpaceCookie.Visibility = Visibility.Visible;
            Bakerie.Visibility = Visibility.Visible;
            CookiePlanet.Visibility = Visibility.Visible;
            Cookieversium.Visibility = Visibility.Visible;
            LeaveShopButton.Visibility = Visibility.Visible;
            GrandmaLevelLabel.Visibility = Visibility.Visible;
            GrandmaLevelLabel2.Visibility = Visibility.Visible;
            NewOvenLevelLabel.Visibility = Visibility.Visible;
            NewOvenLevelLabel2.Visibility = Visibility.Visible;
            SecondOvenLevelLabel.Visibility = Visibility.Visible;
            SecondOvenLevelLabel2.Visibility = Visibility.Visible;
            SpaceCookieLevelLabel.Visibility = Visibility.Visible;
            SpaceCookieLevelLabel2.Visibility = Visibility.Visible;
            BakerieLevelLabel.Visibility = Visibility.Visible;
            BakerieLevelLabel2.Visibility = Visibility.Visible;
            CookiePlanetLevelLabel.Visibility = Visibility.Visible;
            CookiePlanetLevelLabel2.Visibility = Visibility.Visible;
            CookieversiumLevelLabel.Visibility = Visibility.Visible;
            CookieversiumLevelLabel2.Visibility = Visibility.Visible;
        }

        private void LeaveShopButton_Click(object sender, RoutedEventArgs e)
        {
            EnterShopButton.Content = "Enter Shop";
            Grandma.Visibility = Visibility.Hidden;
            NOven.Visibility = Visibility.Hidden;
            XOven.Visibility = Visibility.Hidden;
            SpaceCookie.Visibility = Visibility.Hidden;
            Bakerie.Visibility = Visibility.Hidden;
            CookiePlanet.Visibility = Visibility.Hidden;
            Cookieversium.Visibility = Visibility.Hidden;
            LeaveShopButton.Visibility = Visibility.Hidden;
            GrandmaLevelLabel.Visibility = Visibility.Hidden;
            GrandmaLevelLabel2.Visibility = Visibility.Hidden;
            NewOvenLevelLabel.Visibility = Visibility.Hidden;
            NewOvenLevelLabel2.Visibility = Visibility.Hidden;
            SecondOvenLevelLabel.Visibility = Visibility.Hidden;
            SecondOvenLevelLabel2.Visibility = Visibility.Hidden;
            SpaceCookieLevelLabel.Visibility = Visibility.Hidden;
            SpaceCookieLevelLabel2.Visibility = Visibility.Hidden;
            BakerieLevelLabel.Visibility = Visibility.Hidden;
            BakerieLevelLabel2.Visibility = Visibility.Hidden;
            CookiePlanetLevelLabel.Visibility = Visibility.Hidden;
            CookiePlanetLevelLabel2.Visibility = Visibility.Hidden;
            CookieversiumLevelLabel.Visibility = Visibility.Hidden;
            CookieversiumLevelLabel2.Visibility = Visibility.Hidden;
        }

        private void Grandma_MouseEnter(object sender, MouseEventArgs e)
        {
            GrandmaLabelCosts.Visibility = Visibility.Visible;
            GrandmaLabelPlus.Visibility = Visibility.Visible;
        }

        private void Grandma_MouseLeave(object sender, MouseEventArgs e)
        {
            GrandmaLabelCosts.Visibility = Visibility.Hidden;
            GrandmaLabelPlus.Visibility = Visibility.Hidden;
        }
        private void NOven_MouseEnter(object sender, MouseEventArgs e)
        {
            NewOvenLabelCosts.Visibility = Visibility.Visible;
            NewOvenLabelPlus.Visibility = Visibility.Visible;
        }

        private void NOven_MouseLeave(object sender, MouseEventArgs e)
        {
            NewOvenLabelCosts.Visibility = Visibility.Hidden;
            NewOvenLabelPlus.Visibility = Visibility.Hidden;
        }

        private void XOven_MouseEnter(object sender, MouseEventArgs e)
        {
            SecondOvenLabelCosts.Visibility = Visibility.Visible;
            SecondOvenLabelPlus.Visibility = Visibility.Visible;
        }

        private void XOven_MouseLeave(object sender, MouseEventArgs e)
        {
            SecondOvenLabelCosts.Visibility = Visibility.Hidden;
            SecondOvenLabelPlus.Visibility = Visibility.Hidden;
        }

        private void SpaceCookie_MouseEnter(object sender, MouseEventArgs e)
        {
            SpaceCookieLabelCosts.Visibility = Visibility.Visible;
            SpaceCookieLabelPlus.Visibility = Visibility.Visible;
        }

        private void SpaceCookie_MouseLeave(object sender, MouseEventArgs e)
        {
            SpaceCookieLabelCosts.Visibility = Visibility.Hidden;
            SpaceCookieLabelPlus.Visibility = Visibility.Hidden;
        }

        private void CookiePlanet_MouseEnter(object sender, MouseEventArgs e)
        {
            CookiePlanetLabelCosts.Visibility = Visibility.Visible;
            CookiePlanetLabelPlus.Visibility = Visibility.Visible;
        }

        private void CookiePlanet_MouseLeave(object sender, MouseEventArgs e)
        {
            CookiePlanetLabelCosts.Visibility = Visibility.Hidden;
            CookiePlanetLabelPlus.Visibility = Visibility.Hidden;
        }

        private void Cookieversium_MouseEnter(object sender, MouseEventArgs e)
        {
            CookieversiumLabelCosts.Visibility = Visibility.Visible;
            CookieversiumLabelPlus.Visibility = Visibility.Visible;
        }

        private void Cookieversium_MouseLeave(object sender, MouseEventArgs e)
        {
            CookieversiumLabelCosts.Visibility = Visibility.Hidden;
            CookieversiumLabelPlus.Visibility = Visibility.Hidden;
        }


        private void Bakerie_MouseEnter(object sender, MouseEventArgs e)
        {
            BakerieLabelCosts.Visibility = Visibility.Visible;
            BakerieLabelPlus.Visibility = Visibility.Visible;
        }

        private void Bakerie_MouseLeave(object sender, MouseEventArgs e)
        {
            BakerieLabelCosts.Visibility = Visibility.Hidden;
            BakerieLabelPlus.Visibility = Visibility.Hidden;
        }

        // Shop
        //
        //

        private void Grandma_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 50)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 50;
                AantalCookies.Content = getal;
                GrandmaLevelLabel2.Content = Convert.ToInt32(GrandmaLevelLabel2.Content) + 1;
            }
        }

        private void NOven_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 200)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 200;
                AantalCookies.Content = getal;
                NewOvenLevelLabel2.Content = Convert.ToInt32(NewOvenLevelLabel2.Content) + 1;
            }
        }

        private void XOven_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 500)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 500;
                AantalCookies.Content = getal;
                SecondOvenLevelLabel2.Content = Convert.ToInt32(SecondOvenLevelLabel2.Content) + 1;
            }
        }

        private void SpaceCookie_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 1000)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 1000;
                AantalCookies.Content = getal;
                SpaceCookieLevelLabel2.Content = Convert.ToInt32(SpaceCookieLevelLabel2.Content) + 1;
                SpaceCookieTransformer.Visibility = Visibility.Visible;
                NormalCookieTransformer.Visibility = Visibility.Visible;
            }
        }

        private void Bakerie_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 3000)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 3000;
                AantalCookies.Content = getal;
                BakerieLevelLabel2.Content = Convert.ToInt32(BakerieLevelLabel2.Content) + 1;
            }
        }

        private void CookiePlanet_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 5000)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 5000;
                AantalCookies.Content = getal;
                CookiePlanetLevelLabel2.Content = Convert.ToInt32(CookiePlanetLevelLabel2.Content) + 1;
            }
        }

        private void Cookieversium_Click(object sender, RoutedEventArgs e)
        {
            if (Convert.ToInt32(AantalCookies.Content) >= 10000)
            {
                getal = Convert.ToInt32(AantalCookies.Content) - 10000;
                AantalCookies.Content = getal;
                CookieversiumLevelLabel2.Content = Convert.ToInt32(CookieversiumLevelLabel2.Content) + 1;
            }
        }

        private void SpaceCookieTransformer_Click(object sender, RoutedEventArgs e)
        {
            Cookie.Fill = new SolidColorBrush(Colors.Purple);
            Chocolate1.Fill = new SolidColorBrush(Colors.Green);
            Chocolate2.Fill = new SolidColorBrush(Colors.Green);
            Chocolate3.Fill = new SolidColorBrush(Colors.Green);
            Cookie.Stroke = new SolidColorBrush(Colors.Green);
            Chocolate1.Stroke = new SolidColorBrush(Colors.Purple);
            Chocolate2.Stroke = new SolidColorBrush(Colors.Purple);
            Chocolate3.Stroke = new SolidColorBrush(Colors.Purple);
        }

        private void NormalCookieTransformer_Click(object sender, RoutedEventArgs e)
        {
            Cookie.Fill = new SolidColorBrush(Colors.SandyBrown);
            Chocolate1.Fill = new SolidColorBrush(Colors.SaddleBrown);
            Chocolate2.Fill = new SolidColorBrush(Colors.SaddleBrown);
            Chocolate3.Fill = new SolidColorBrush(Colors.SaddleBrown);
            Cookie.Stroke = new SolidColorBrush(Colors.SaddleBrown);
            Chocolate1.Stroke = new SolidColorBrush(Colors.SandyBrown);
            Chocolate2.Stroke = new SolidColorBrush(Colors.SandyBrown);
            Chocolate3.Stroke = new SolidColorBrush(Colors.SandyBrown);
        }
    }
}
```
