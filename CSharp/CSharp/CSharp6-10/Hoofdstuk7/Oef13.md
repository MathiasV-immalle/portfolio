# Oefening: Bereken btw met tarieven

### De XAML-code:
```
<Window x:Class="BtwTariefBerekenen_Wpf.MainWindow" xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml" xmlns:d="http://schemas.microsoft.com/expression/blend/2008" xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006" xmlns:local="clr-namespace:BtwTariefBerekenen_Wpf" mc:Ignorable="d" Title="MainWindow" Height="220.947" Width="241.781">
    <Grid>
        <TextBlock x:Name="Netto" HorizontalAlignment="Left" Margin="10,10,0,0" TextWrapping="Wrap" Text="Netto prijs:" VerticalAlignment="Top" Width="64"/>
        <TextBox x:Name="NettoBedrag" HorizontalAlignment="Left" Height="16" Margin="79,10,0,0" TextWrapping="Wrap" Text="" VerticalAlignment="Top" Width="114"/>
        <CheckBox x:Name="VerlaagdTarief" Content="Verlaagd tarief" HorizontalAlignment="Left" VerticalAlignment="Top" Margin="79,41,0,0"/>
        <TextBlock x:Name="BTW" HorizontalAlignment="Left" Margin="10,76,0,0" TextWrapping="Wrap" Text="BTW:" VerticalAlignment="Top" Width="64"/>
        <TextBlock x:Name="BTWBedrag" HorizontalAlignment="Left" Margin="79,76,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="114" Background="#FFCDCDCD"/>
        <TextBlock x:Name="Totaal" HorizontalAlignment="Left" Margin="10,113,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="64"><Run Text="Totaal"/><Run Text=":"/></TextBlock>
        <TextBlock x:Name="TotaalBedrag" HorizontalAlignment="Left" Margin="79,113,0,0" TextWrapping="Wrap" VerticalAlignment="Top" Width="114" Background="#FFCDCDCD"/>
        <Button x:Name="Bereken" Content="Bereken" HorizontalAlignment="Left" VerticalAlignment="Top" Width="77" Margin="116,141,0,0" Click="Bereken_Click"/>

    </Grid>
</Window>
```

### De Eventhandlers:

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
using System.Drawing;
namespace BtwTariefBerekenen_Wpf
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }
        private void Bereken_Click(object sender, RoutedEventArgs e)
        {
            double netto = Convert.ToDouble(NettoBedrag.Text);
            double btw;
            double totaal;

            if (VerlaagdTarief.IsChecked == true)
            {
                btw = netto * 0.06;
                totaal = netto + btw;
            }
            else
            {
                btw = netto * 0.21;
                totaal = netto + btw;
            }
            BTWBedrag.Text = Convert.ToString(btw);
            TotaalBedrag.Text = Convert.ToString(totaal);
        }
    }
}
```
