# Oefening 2.2: Visibility-property

##XAML

```C#
<Window x:Class="Oef2._2Visibility.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:Oef2._2Visibility"
        mc:Ignorable="d"
        Title="MainWindow" Height="350" Width="525">
    <Grid>
        <Button x:Name="button" Content="Visible" HorizontalAlignment="Left" Margin="10,35,0,0" VerticalAlignment="Top" Width="75" Click="button_Click"/>
        <Button x:Name="button1" Content="Invisible" HorizontalAlignment="Left" Margin="10,10,0,0" VerticalAlignment="Top" Width="75" Click="button1_Click"/>
        <Label x:Name="label" Content="Geel" HorizontalAlignment="Left" Margin="111,17,0,0" VerticalAlignment="Top" Background="Yellow"/>

    </Grid>
</Window>
```

#### Dit maakt hetgeen deze afbeelding weergeeft.

![afbeelding](Hoofdstuk2Oef2/1.png)

## Eventhandlers

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

namespace Oef2._2Visibility
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

        private void button_Click(object sender, RoutedEventArgs e)
        {
            label.Visibility = Visibility.Visible;
        }

        private void button1_Click(object sender, RoutedEventArgs e)
        {
            label.Visibility = Visibility.Collapsed;
        }
    }
}
```

#### Deze code zorgt voor het effect dat deze afbeeldingen weergeven indien:

##### De Visibility-knop wordt ingedrukt

![Visibility](Hoofdstuk2Oef2/2.png)

##### De Invisibility-knop wordt ingedrukt

![Invisibility](Hoofdstuk2Oef2/3.png)
